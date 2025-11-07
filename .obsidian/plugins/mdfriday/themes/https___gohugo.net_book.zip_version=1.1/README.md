# MDFriday Portfolio Theme

A modern, clean portfolio theme for Hugo designed specifically for MDFriday users, supporting both organization and personal information display.

## Features

- 🎨 Modern, clean design inspired by Max Böck's portfolio
- 📱 Fully responsive layout
- 🏢 Organization information support
- 👤 Personal author information
- 📝 Blog functionality with posts structure
- 🔍 SEO optimized with microformats
- 🌐 Multi-language support
- ⚡ Fast loading with optimized assets
- 🎯 Accessibility focused
- 📊 Weight-based post ordering
- ⭐ Featured posts support

## Installation

### As a Hugo Module (Recommended)

```bash
hugo mod init github.com/yourusername/yoursite
hugo mod get github.com/mdfriday/foundry/portfolio-theme
```

### As a Git Submodule

```bash
git submodule add https://github.com/mdfriday/foundry.git themes/portfolio
```

### Manual Installation

1. Download the theme
2. Extract to `themes/portfolio` in your Hugo site
3. Add `theme = "portfolio"` to your `config.yaml`

## Configuration

This theme is designed to work with MDFriday's content structure. The main configuration is done in your `index.md` file.

### Content Structure

Your content should be organized as follows:

```
content/
├── index.md          # Homepage with organization and author info
├── about.md          # About page
└── posts/            # Blog posts directory
    ├── 001-post.md
    ├── 002-post.md
    └── ...
```

### Homepage Configuration (index.md)

```yaml
---
title: "Home"

menu:
  nav:
    - title: "Home"
      url: ""
      weight: 1
    - title: "Posts"
      url: "posts"
      weight: 2
    - title: "About"
      url: "about.html"
      weight: 3

author:
  name: "Sun Wei"
  description: "Creator of MDFriday, passionate about Markdown, AI, and knowledge visualization."
  website: "https://sunwei.xyz"
  avatar: "avatar.png"
  contact:
    email: "sunwei@mdfriday.org"
---

{{< hero title="I make websites." >}}
{{< hero_pretitle href="/about/" content="Hello, my name is Sun Wei" >}}
{{< hero_content >}}
I'm a creator and developer of {{< hero_link href="https://mdfriday.com" class="hero__link--codista" text="MDFriday" >}}, a powerful Markdown editor and note-taking app. I also write about AI and knowledge visualization on my {{< hero_link href="/posts" text="blog" >}} and {{< hero_link href="https://github.com/mdfriday" class="hero__link--mastodon" text="GitHub" >}}.
{{< /hero_content >}}
{{< /hero >}}
```

### Post Configuration

```yaml
---
title: "Your Post Title"
date: 2025-10-10
author: "Author Name"
description: "Post description"
feature: true          # Mark as featured post
featured_image: "posts/image.jpg"
weight: 1             # Lower weight = higher priority
tags:
  - "tag1"
  - "tag2"
isStarred: true       # Mark as starred/featured
---

Your post content here...
```

## Content Types

### Blog Posts

Create blog posts in `content/blog/`:

```yaml
---
title: "My Blog Post"
date: 2023-01-01
featured: true
featured_image: "/images/post-image.jpg"
color: "#f5f5f5"
excerpt: "Short description of the post"
tags: ["web", "development"]
---

Your blog content here.
```

### Portfolio Items

Create portfolio items in `content/portfolio/`:

```yaml
---
title: "Project Name"
date: 2023-01-01
featured: true
featured_image: "/images/project-image.jpg"
technologies: ["React", "Node.js", "MongoDB"]
demo_url: "https://demo.example.com"
source_url: "https://github.com/user/project"
excerpt: "Brief project description"
---

Detailed project description and documentation.
```

## Shortcodes

The theme supports Hugo's built-in shortcodes and several custom ones:

### Hero Section

Create a hero section with title and nested content:

```markdown
{{< hero title="I make websites." >}}
{{< hero_pretitle href="/about/" content="Hello, my name is Max" >}}
{{< hero_content >}}
I'm a front-end developer and co-founder of {{< hero_link href="https://www.codista.com" class="hero__link--codista" text="Codista" >}}, a software studio in Vienna. I also write about the web on my {{< hero_link href="/blog" text="blog" >}} and {{< hero_link href="https://front-end.social/@mxbck" class="hero__link--mastodon" text="elsewhere" >}}.
{{< /hero_content >}}
{{< /hero >}}
```

#### Hero Components

- **hero**: Main hero container with optional title
- **hero_pretitle**: Pretitle with optional link
- **hero_content**: Content area supporting markdown and hero_link shortcodes
- **hero_link**: Special links with predefined classes (hero__link, hero__link--codista, hero__link--mastodon)

### YouTube

```markdown
{{< youtube "ZJthWmvUzzc" >}}
```

### Twitter/X

```markdown
{{< x user="DesignReviewed" id="1085870671291310081" >}}
```

### Vimeo

```markdown
{{< vimeo "48912912" >}}
```

### Figure

```markdown
{{< figure src="/images/example.jpg" alt="Example image" caption="Image caption" >}}
```

### Gallery

```markdown
{{< gallery images="/img/1.jpg|Alt text 1|Caption 1,/img/2.jpg|Alt text 2|Caption 2" columns="2" >}}
```

### Alert

```markdown
{{< alert type="info" title="Note" >}}
This is an informational alert.
{{< /alert >}}
```

### Button

```markdown
{{< button href="https://example.com" text="Click me" class="btn btn--primary" target="_blank" >}}
```

### Code Highlight

```markdown
{{< highlight javascript "linenos=table" >}}
console.log("Hello, world!");
{{< /highlight >}}
```

## Customization

### Custom CSS

Add custom styles in `assets/css/custom.css`:

```css
/* Your custom styles */
.custom-class {
  color: #333;
}
```

### Custom JavaScript

Add custom scripts in `assets/js/custom.js`:

```javascript
// Your custom JavaScript
console.log("Custom script loaded");
```

## Menu Configuration

```yaml
menu:
  main:
    - name: "Home"
      url: "/"
      weight: 1
    - name: "Blog"
      url: "/blog/"
      weight: 2
    - name: "Portfolio"
      url: "/portfolio/"
      weight: 3
    - name: "About"
      url: "/about/"
      weight: 4
```

## Multi-language Support

The theme supports multiple languages. Add translations in the `i18n/` folder:

```yaml
# i18n/en.yaml
- id: home.recent_posts
  translation: "Recent Posts"

# i18n/zh.yaml
- id: home.recent_posts
  translation: "最新文章"
```

## Development

To contribute to this theme:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test with the example site
5. Submit a pull request

## License

This theme is released under the MIT License. See [LICENSE](LICENSE) for details.

## Credits

- Based on the Hugo Blog Awesome theme structure
- Inspired by Max Böck's personal website design
- Built with modern web standards and accessibility in mind
