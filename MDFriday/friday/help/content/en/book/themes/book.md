
# Theme Book

The "Book" theme is specifically designed for books, documents, tutorials, or long-form content. It offers a clean layout and an easy-to-navigate structure, providing a great reading experience for users. It also supports multiple languages.

**What is it suitable for?**

- **Online E-books** – Ideal for publishing novels, technical books, tutorials, and other long-form content, with chapter navigation and search functionality.
- **Technical Documentation Websites** – Perfect for developers writing API documentation, project documentation, user manuals, etc., with a clear directory structure for easy navigation.
- **Knowledge Bases & Wikis** – Used to build internal knowledge bases, FAQ pages, or documentation centers for open-source projects, making collaboration and information storage easy.
- **Personal Blogs** – Great for writing columns, academic articles, or personal study notes, with a simple interface that enhances readability.
- **Study Notes & Course Materials** – Can be used to organize and publish study notes and course handouts, presenting knowledge in a structured way.
- **Open Source Project Documentation** – Ideal for hosting documentation for GitHub open-source projects, with Hugo’s static features providing fast website generation.
- **Product Manuals & User Guides** – Used by businesses or individuals to create product instructions, helping users understand product features and operations.
- **Internal Training Materials** – Can be used by companies or organizations to create internal training documentation, facilitating online learning and reference for employees.
- **Project Roadmaps & Planning Documents** – Suitable for recording product development plans and team goals, making it easy to maintain and update over time.

**Main Features:**

- **Long-form Content Friendly**: Optimized for displaying long-form content, ensuring users don’t get fatigued while browsing.
- **Multi-level Directory Structure**: Supports multi-level directories and chapters, allowing users to quickly find the sections they are interested in.
- **Responsive Design**: Adapts to desktops, tablets, and mobile devices, ensuring the best browsing experience on any device.
- **Search Functionality**: Built-in search function helps users quickly find the content they need.
- **External Links and Citations Support**: Easy to add external links, references, images, videos, etc., to enhance content variety.
- **Multi-language Support**: Built-in multilingual features, ideal for creating documents or websites in different languages for global accessibility.

##  Live Demo

- Visit the [Book Theme Demo](https://www.bilibili.com/video/BV1GtcuezEvs/?share_source=copy_web&vd_source=fd436a14aae706a8ed4a8b58b172721d).

## Sample Directory Structure

```plaintext
├─MDFriday
│  │  Untitled Friday Site.md      # Configuration file
│  │
│  └─book
│      │  README.md
│      │
│      └─content
│          ├─en                    # English folder
│          │  │  links.md          # External links
│          │  │  _index.md         # English homepage
│          │  │
│          │  ├─book               # Book directory
│          │  │  ├─example         # Example directory
│          │  │  │  │  hidden.md   # Hidden page example
│          │  │  │  │  _index.md   # Content displayed when clicked
│          │  │  │  │
│          │  │  │  ├─collapsed     # Collapsible directory
│          │  │  │  │  │  _index.md # Content displayed when clicked
│          │  │  │  │  │
│          │  │  │  │  └─3rd-level  # 3rd-level directory
│          │  │  │  │          4th-level.md  # 4th-level directory
│          │  │  │  │          _index.md     # Content displayed when clicked
│          │  │  │  │
│          │  │  │  └─table-of-contents      # Table of contents directory
│          │  │  │          with-toc.md      # (Right side) Displays article table of contents
│          │  │  │          without-toc.md   # (Right side) Hides article table of contents
│          │  │  │          _index.md        # Content displayed when clicked
│          │  │  │
│          │  │  └─shortcodes                # Extensions
│          │  │      │  buttons.md           # Generates buttons
│          │  │      │  columns.md           # Displays in columns
│          │  │      │  details.md           # Collapsible info blocks
│          │  │      │  hints.md             # Inserts hint boxes
│          │  │      │  katex.md             # Renders math formulas
│          │  │      │  mermaid.md           # Renders charts or diagrams
│          │  │      │  tabs.md              # Tabbed interface
│          │  │      │  _index.md            # Index file
│          │  │      │
│          │  │      └─section               # Sub-directory
│          │  │              first-page.md   
│          │  │              second-page.md
│          │  │              _index.md
│          │  │
│          │  └─posts                    # Blog posts    
│          │          creating-a-new-theme.md
│          │          goisforlovers.md
│          │          hugoisforlovers.md
│          │          migrate-from-jekyll.md
│          │          _index.md
│          │
│          └─zh                         # Chinese directory
│                  links.md             # External links
│                  _index.md            # Chinese homepage
```

## How to Use the  Book Theme?

Step-by-step instructions:

1. **Replace the theme**: In the file, modify the `theme` field as shown above to `github.com/mdfriday/theme-book`.

```plaintext
friday-plugin: enabled
site: '0'
theme: github.com/mdfriday/theme-hero
project: empty
defaultLanguage: en
ga: GT-XXXXXXXXX
```

Change the `theme` line to:

```plaintext
theme: github.com/mdfriday/theme-book
```

2. **Download sample files**: Obtain the  Book theme sample files from MDFriday and download them locally.
3. **Modify the files**: Open the sample files and edit text, image links, and document information to fit your website needs.
4. **Preview**:  preview the website to ensure everything displays correctly.
5. **Deploy your site**: If the preview looks good, you can deploy your personal website!

Congratulations, your personal website is now live! You can update the content anytime and share it with your friends. With Friday, creating a website has never been this easy. Give it a try and start building your online space today!
