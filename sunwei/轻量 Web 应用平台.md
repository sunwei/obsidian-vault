

# 🧠 Markdown Shortcode 驱动的轻量 Web 应用平台

> 用 Markdown + Shortcode 构建无需后端的轻量 Web 应用，实现个性化表达、数据收集、内容发布、互动反馈等核心能力。

---

## 🚀 定位（Positioning）

这是一个**以 Markdown + Shortcode 为基础的轻量 Web 应用平台**，旨在帮助用户快速创建面向「内容表达 + 功能交互」的轻型 Web 应用，覆盖如学习打卡、在线简历、数据表单、内容展示、客户管理等典型使用场景。

---

## 🌟 核心特色（Key Features）

| 能力 | 描述 |
|------|------|
| 🧱 基于 Markdown 内容驱动 | 一切功能皆通过 Markdown 文件定义内容与结构 |
| 🧩 Shortcode 即功能组件 | 每个功能以 shortcode 实现，表达即调用，组合即系统 |
| 🎨 Layout 模板控制外观 | 页面由 layout 模板统一布局，样式与主题分离 |
| 🧘 无需后端、部署灵活 | 前端构建即可部署，支持本地、GitHub Pages、服务器构建 |
| 🔗 可组合、可拆解 | 卡片可独立使用也可组合为页面，页面可构建为站点 |

---

## 🧠 系统架构与目录规范

```

📁 layout/  
├── page.html # 页面主模板  
├── home.html # 首页模板  
└── template/  
├── header.html # 可复用区块  
├── footer.html  
└── components/  
├── card.html # 组件模板（shortcode 逻辑注入点）

📁 content/ # Markdown 内容目录  
📁 page/ # 页面级别 Markdown（站点入口）  
📁 asset/ # 静态资源（图片、音频等）  
📁 shortcode/ # 所有支持的功能卡片

````

### ✨ 设计约定

- 所有 layout 模板使用 Go Text Template 标准（已实现 TypeScript 渲染器）
- 页面文件可通过 YAML Front Matter 指定使用的 layout
- Shortcode 是功能组件，每个 shortcode 拥有自己的模板、输入参数、样式与交互逻辑
- 页面构建通过文件结构与 Front Matter 自动匹配模板，无需手动指定路由逻辑

---

## 🧩 示例场景（Use Cases）

| 场景分类 | 示例 |
|----------|------|
| 👶 儿童成长 | 每日学习打卡卡片、目标达成奖励系统、家庭成员习惯排行榜 |
| ✍️ 内容创作 | 知识卡片集、图文作品集展示页、订阅 CTA 表单 |
| 🧑‍🎓 教育学习 | 错题记录卡片、课程笔记、在线课程销售页、学习路径导航 |
| 💼 个人职业 | 在线简历生成与分享页、项目介绍页、互动联系表单 |
| 🧑‍🤝‍🧑 家庭协作 | 家庭计划看板、值日安排、奖励分配机制 |
| 📇 客户管理 | 客户联系人卡片系统、电脑拨号、发邮件一键操作 |
| 📬 表单系统 | 提交建议、报名收集、反馈收集（支持 Webhook / 邮箱 / CRM） |
| 🧰 通用应用 | QR 名片页、静态站点首页生成器、小团队官网快速搭建 |

---

## 💬 电梯演讲（Elevator Pitch）

> “我们通过 Markdown + Shortcode，重新定义轻量 Web 应用构建方式。无需后端、无需复杂开发，写 Markdown 就能构建一个有交互的功能站点。不论你是老师、学生、创作者还是开发者，都可以用它发布内容、记录成长、管理数据或建立自己的 Web 小工具。”

---

## 🔧 实施步骤（How to Build）

1. 设计主题 layout（页面框架、样式体系）
2. 创建 Shortcode 模板（每种功能一个卡片，支持参数配置）
3. 编写 Markdown 内容（调用 shortcode，实现功能表达）
4. 使用 TS 渲染器构建页面（基于定义的模板与内容）
5. 输出为静态 HTML + 资源文件，发布至任意静态站点托管平台

---

## 💡 核心理念（Philosophy）

- **短代码即功能**：每个功能独立封装、可复用、可组合、可个性化
- **内容即前端**：Markdown 驱动整个前端内容与逻辑
- **轻而不简**：无需重型框架，构建精巧的个性 Web 应用
- **多样性优先**：Shortcode 不追求参数统一，而强调多样性与表达力

---

## 📌 后续可扩展方向

- Shortcode 预设市场（可复用卡片市场）
- 卡片式 CRM / 表单服务（Webhook / 邮件通知）
- 简历 / 作品集发布工具（带自定义域名支持）
- 小朋友成长仪表盘（每日任务、奖励排行榜）
- 知识创作内容库（结合图文、音频、CTA）

---

## 🛠 示例 Shortcode（部分）

```md
{{< study-checkin date="2025-05-20" title="背诵乘法口诀" pokemon="皮卡丘" >}}

{{< goal-achieve title="阅读完成" reward="解锁看动画时间30分钟" >}}

{{< contact-card name="张三" email="z@domain.com" tel="138****8888" >}}

{{< resume-card name="李雷" skills="前端开发, React, Vue" >}}

{{< form-submit endpoint="https://api.mysite.com/save" fields="name,email,message" >}}
````
