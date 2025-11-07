---
title: How MDFriday Works?
date: 2025-10-10
author: Sun Wei
description: Guide to MDFriday usage in Obsidian
feature: true
featured_image: "assets/images/featured/analytics.jpg"
weight: 1
tags:
  - MDFriday
---

**MDFriday** — Just Write. MDFriday brings it to life.

## Awesome Theme Story

Awesome is for creators who see through the noise —
those who want their words to speak,
not their design to shout.

Simple. Clean. Deadly precise.
That’s Awesome.

Like *John Wick* - "Yeah, I’m thinking I’m back."

---

## ⚙️ Quick Start

1. Open **Obsidian’s Community Plugins**
2. Search for **Friday** and install
3. Choose a theme from the MDFriday panel
4. Download the theme’s sample notes
5. Right-click a note → **Publish to Web**
6. Click **Preview** to see it live locally

Once previewed, edit the sample notes with your own content —  
and you’ve got your personal site!

You can:
- Export the static site and upload it anywhere
- Or configure cloud settings to **publish directly** with one click


---

## 🧩 Architecture Overview

MDFriday consists of three main parts:

1. **Obsidian Plugin**
    - Provides the editing and theme management interface
    - Supports preview, export, and publishing
    - Lets users install themes and sample notes with one click

2. **Shortcode Rendering Engine**
    - A lightweight Hugo-style templating system
    - Allows embedding of custom visual components (cards, galleries, etc.)
    - Implemented in TypeScript, cross-platform compatible

3. **Build & Publishing System**
    - Converts Markdown + Shortcodes → static HTML site
    - Automatically applies selected theme (Tailwind + template engine)
    - Exports ready-to-host files
    - Optional cloud publishing (Cloudflare / GitHub Pages / custom)

---

## 🧠 Workflow

1. **Write Markdown**  
   Create and edit notes in Obsidian — shortcodes included.

2. **Choose a Theme**  
   Each theme contains templates, sample notes, and style assets.  
   Themes are fully customizable and easy to preview.

3. **Preview & Build**  
   Click **Preview** to see your site locally.  
   MDFriday renders Markdown + Shortcodes + Theme seamlessly.

4. **Publish**
    - Export the static site and upload anywhere
    - Or configure cloud credentials for one-click publishing
    - Includes SEO meta tags and OpenGraph data automatically

---

## 🔧 Tech Stack & Design Principles

| Module | Technology | Design Principle |
|--------|-------------|------------------|
| Editor | Obsidian | Centralized, distraction-free creation |
| Renderer | TypeScript (`text/template` compatible) | Consistency & extensibility |
| Styling | Tailwind CSS | Minimal & themeable |
| Build | Node.js / ESBuild | Fast and modular |
| Deploy | Cloudflare / GitHub Pages / Local | Flexible and user-controlled |

---

## 🪄 Everything Starts with Markdown

MDFriday doesn’t require any new syntax or tools.  
Every site begins with a simple `.md` file.  
Themes define **how it looks**,  
Shortcodes define **how it feels**.

> ✨ TL;DR:  
> **Write Markdown → Render → Build → Publish**  
> No code. No config. No distractions.

---

## 👨‍💻 A Note from the Author

> “MDFriday is built to grow with creators —  
> from a single note to a personal brand site.  
> I want to help you turn your content into digital assets.”
>
> — Sun Wei
