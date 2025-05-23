

# 儿童学习网站主题设计文档

## 🎯 目标

构建一个能激发儿童学习兴趣、记录学习成长的轻量化个人网站系统。该系统支持以下特性：

- 每日学习记录（卡片形式展示）
    
- 习惯追踪、错题本、学习笔记归档
    
- 自定义可视化模板，增强参与感（如每日可选 Pokémon 形象）
    
- 成就系统和经验值反馈，建立正向激励
    

---

## 🏗️ 结构设计

### 1. 模板结构（layout）

采用 TypeScript 实现的 `text/template` 机制，支持 `{{ define }}` 与 `{{ template }}`，将布局职责与内容展示分离。

```
layout/
├── home.html           # 首页模板
├── page.html           # 一般内容页模板
└── template/           # 可复用的布局组件
    ├── header.html     # 页眉（导航）
    ├── footer.html     # 页脚
    ├── sidebar.html    # 可选边栏（未启用）
    └── card.html       # 学习卡片模板
```

### 2. 内容结构（content）

标准化内容目录，方便规则式处理与站点生成。

```
content/
├── habits/     # 学习习惯追踪（如每日打卡）
├── notes/      # 笔记内容（各学科）
├── mistakes/   # 错题集（按日期归档）
├── badges/     # 勋章记录（成就系统）
```

---

### 3. 页面定义（page）

```
page/
├── index.md         # 首页内容
├── profile.md       # 个人档案
└── dashboard.md     # 学习看板页
```

每个页面可定义其使用的 `layout`：

```markdown
---
title: 学习面板
layout: page
---

{{< daily-task xp="20" done="true" >}}

{{< badge name="坚持7天打卡" icon="🔥" >}}

{{< mistake title="数学 - 分数加减法错误" date="2025-05-20" >}}
```

---

## ⚙️ 样式与布局机制

- 页面由主模板（如 `home.html` 或 `page.html`）构建整体结构
    
- `template/` 中的 header/footer/card 等组件通过 `{{ template }}` 引入
    
- 所有内容通过 `shortcode` 组件化，增强灵活性与扩展性
    

---

## 🏆 成就系统（规划中）

右上角展示：

- 当前经验值（XP）进度条
    
- 获得的勋章列表
    
- 学习 streak 等激励元素
    

所有数值都可从页面中的 shortcode 中动态统计得出，增强反馈感。

---

## ✅ 开发优势

- 🌱 **轻量可控**：无依赖构建，适合低年龄段使用
    
- ⚡ **模板复用**：通过模板抽象，支持未来自由扩展
    
- 🧩 **内容组件化**：shortcode 内容即插即用，灵活强大
    
- 👦 **参与感强**：每日选择卡片、获得成就，增强主动性
    

---

如果你需要，我也可以帮你将这套架构转成实际代码模板，或为你编写页面生成器。是否需要继续生成一个默认主题预览页？