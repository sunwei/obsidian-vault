# Friday 插件站点预览设计方案

本设计文档总结了 Friday 插件在 Obsidian 中实现「站点实时预览」的完整思路，包含：

- Shortcode 系统设计
- `mdfriday.md` 配置方案
- 实时预览渲染机制

---

## 📦 一、Shortcode 系统设计

### 1. Shortcode 模块结构

每个 shortcode 以独立目录管理，包含：

```

shortcodes/  
└── image-card/  
├── meta.json ← 描述信息（标签、用途、预览图等）  
├── template.html ← 渲染模板（支持 {{ .Params }}）  
├── example.md ← 示例用法  
└── sync_hash ← 同步版本标记

````

### 2. Shortcode 注册机制

- 插件在预览时解析 `shortcode block`
- 根据 block 中的 shortcode 名称，注册/加载对应 template
- 支持远程拉取并缓存模板

### 3. Shortcode 优先级与主题支持

- 用户选择的主题可覆盖部分 shortcode
- 未定义的 shortcode fallback 到 `base` 主题中的默认实现

```ts
function getShortcodeTemplate(name, theme) {
  if (themeHas(name)) return theme[name]
  return baseTheme[name]
}
````

---

## ⚙️ 二、`mdfriday.md` 配置设计

### 1. 配置文件路径

- 每个项目或站点以**文件夹为单位**
    
- 用户需在该目录下创建一个 `mdfriday.md` 文件
    
- 该文件用于定义渲染主题、首页路径、可见性等信息
    

### 2. 示例配置内容（frontmatter）

```markdown
---
title: 我的学习笔记站点
theme: clean-notes
index: README.md
layout: default
---

欢迎使用 Friday，可视化发布笔记！
```

### 3. 搜索逻辑

- 当渲染某个文件时，从该文件所在目录向上递归查找 `mdfriday.md`
    
- 使用**最靠近**该文件的配置作为渲染依据（类似 Git 或 Hugo 的行为）
    

---

## 🧪 三、实时站点预览设计

### 1. 预览触发机制

- 插件监听 Obsidian 中活跃文件变更
    
- 用户点击「👁 Site Preview」按钮打开右侧预览面板
    

```ts
this.app.workspace.on('active-leaf-change', (leaf) => {
  if (isMarkdownFile(leaf)) {
    const file = leaf.file
    updateSitePreview(file)
  }
})
```

### 2. 渲染流程

1. **查找 mdfriday 配置**：从当前文件目录向上查找 `mdfriday.md`
    
2. **获取主题信息**：从 frontmatter 中读取主题名
    
3. **收集页面数据**：
    
    - Markdown 原文内容
        
    - 用到的 shortcode
        
4. **本地渲染为 HTML**（在 iframe 中展示）：
    
    - 主题模板（如 layout/page.html）
        
    - 加载并组合 shortcode
        
    - 渲染成完整页面结构
        

### 3. 渲染展示 UI（推荐）

采用**右侧 Panel（侧边栏）方式**：

```
+------------------------+-----------------------------+
|      编辑器 (左)       |   站点预览 Panel（右）      |
|  Markdown + Shortcode |   整页渲染 + 主题 + 站点结构 |
+------------------------+-----------------------------+
```

- 保持实时同步
    
- 支持切换文件自动更新预览
    
- 模态框不推荐作为主入口（适合临时预览）
    

---

## 🧩 四、基础主题与主题继承机制

### 1. 基础主题（base）

- 提供**所有支持的 shortcode**
    
- 样式清爽、可读性强
    
- 其它主题可以继承或覆盖 base 中的部分 shortcode
    

### 2. 主题结构示例

```
themes/
├── base/
│   └── shortcodes/
│       ├── image-card.html
│       ├── callout.html
│       └── ...
├── clean-notes/
│   ├── theme.md
│   ├── manifest.json
│   └── shortcodes/
│       └── callout.html (覆盖)
```

### 3. manifest.json（可选）

用于说明主题依赖关系和支持的 shortcodes：

```json
{
  "name": "clean-notes",
  "extends": "base",
  "shortcodes": ["callout", "image-card"]
}
```

---

## ✅ 总结

|模块|目标|实现方式|
|---|---|---|
|Shortcode|可组合、可拓展的渲染单元|每个 shortcode 独立目录 + fallback 机制|
|配置系统|定义每个站点的主题与行为|`mdfriday.md` frontmatter 配置|
|实时预览|所见即所得的整页渲染|右侧 Panel 实时监听并渲染|
|主题管理|用户主题与默认主题的解耦|支持基础主题，按需继承|

