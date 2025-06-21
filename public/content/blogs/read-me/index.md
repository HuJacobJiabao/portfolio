---
type: "blog"
title: "Read Me"
createTime: "2025-06-19T03:11:30.456Z"
description: "This is the default description for blog."
tags: ["Hello", "world"]
category: "default"
coverImage: "favicon.png"
---

# {{title}}
<div align="center">

# 🍙 Onigiri Press

  <img src="favicon.png" alt="Onigiri Press Logo" style="width: 100px; height: auto; margin: 20px 0;" />
  

  **A Modern, Lightweight Portfolio & Blog Framework**
  
  *Built with React, TypeScript, and Vite*
</div>
  
  <div style="display: flex; flex-wrap: wrap; gap: 4px; justify-content: center; align-items: center;">
    <a href="https://www.npmjs.com/package/onigiri-press" style="display: inline-block; width: auto !important; height: auto !important; line-height: 1;">
      <img src="https://badge.fury.io/js/onigiri-press.svg" alt="npm version" style="display: inline-block; width: auto !important; height: 20px; vertical-align: middle; margin: 0 !important;" />
    </a>
    <a href="https://opensource.org/licenses/MIT" style="display: inline-block; width: auto !important; height: auto !important; line-height: 1;">
      <img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT" style="display: inline-block; width: auto !important; height: 20px; vertical-align: middle; margin: 0 !important;" />
    </a>
    <a href="https://www.typescriptlang.org/" style="display: inline-block; width: auto !important; height: auto !important; line-height: 1;">
      <img src="https://img.shields.io/badge/TypeScript-Ready-blue.svg" alt="TypeScript" style="display: inline-block; width: auto !important; height: 20px; vertical-align: middle; margin: 0 !important;" />
    </a>
    <a href="https://reactjs.org/" style="display: inline-block; width: auto !important; height: auto !important; line-height: 1;">
      <img src="https://img.shields.io/badge/React-19+-61dafb.svg" alt="React" style="display: inline-block; width: auto !important; height: 20px; vertical-align: middle; margin: 0 !important;" />
    </a>
    <a href="https://vitejs.dev/" style="display: inline-block; width: auto !important; height: auto !important; line-height: 1;">
      <img src="https://img.shields.io/badge/Vite-6+-646CFF.svg?logo=vite&logoColor=white" alt="Vite" style="display: inline-block; width: auto !important; height: 20px; vertical-align: middle; margin: 0 !important;" />
    </a>
    <a href="https://github.com/markdown-it/markdown-it" style="display: inline-block; width: auto !important; height: auto !important; line-height: 1;">
      <img src="https://img.shields.io/badge/Markdown-Support-000000.svg?logo=markdown" alt="Markdown" style="display: inline-block; width: auto !important; height: 20px; vertical-align: middle; margin: 0 !important;" />
    </a>
    <a href="https://github.com/MoePlayer/APlayer" style="display: inline-block; width: auto !important; height: auto !important; line-height: 1;">
      <img src="https://img.shields.io/badge/🎵_Audio_Player-APlayer-FF6B35.svg" alt="Audio" style="display: inline-block; width: auto !important; height: 20px; vertical-align: middle; margin: 0 !important;" />
    </a>
    <a href="https://pages.github.com/" style="display: inline-block; width: auto !important; height: auto !important; line-height: 1;">
      <img src="https://img.shields.io/badge/GitHub_Pages-Deploy-222222.svg?logo=github" alt="GitHub Pages" style="display: inline-block; width: auto !important; height: 20px; vertical-align: middle; margin: 0 !important;" />
    </a>
  </div>


---

## 🍙 What is Onigiri?

**Onigiri** (おにぎり) is a traditional Japanese rice ball - simple, portable, and satisfying. Just like the beloved food that inspired its name, Onigiri Press embodies the Japanese philosophy of simplicity, functionality, and thoughtful design.

Much like how onigiri wraps nutritious ingredients in perfectly seasoned rice, **Onigiri Press** wraps your content, projects, and ideas in a clean, efficient framework that's both beautiful and functional.

## 🚀 What is Onigiri Press?

**Onigiri Press** is a modern, lightweight portfolio and blog framework designed for developers, designers, and content creators who value:

- **Simplicity**: Clean, intuitive design that puts your content first
- **Performance**: Lightning-fast loading with optimized static generation
- **Flexibility**: Easy customization without compromising functionality
- **Developer Experience**: Modern tooling with TypeScript, React, and Vite

### ✨ Key Features

🎨 **Beautiful & Responsive Design**
- Modern, clean interface that works on all devices
- Customizable themes and layouts
- Smooth animations and transitions

📝 **Powerful Content Management**
- Markdown-based content with advanced features
- Support for blogs, projects, and portfolios
- Rich text formatting with syntax highlighting

⚡ **Performance Optimized**
- Static site generation for lightning-fast loading
- Optimized images and assets
- SEO-friendly structure

🛠️ **Developer Friendly**
- TypeScript support out of the box
- Hot reload development server
- Easy deployment to GitHub Pages, Netlify, Vercel

🎵 **Rich Media Support**
- Audio player integration (APlayer/MetingJS)
- Image galleries and carousels
- Video embedding support

📊 **Advanced Features**
- Math equations with KaTeX
- Code syntax highlighting with Prism
- Table of contents generation
- Tag and category filtering

---

## 🚀 Quick Start

### Global Installation

```bash
# Install Onigiri Press globally
npm install -g onigiri-press
```

### Create Your First Project

```bash
# Initialize a new project
ongr init my-awesome-portfolio

# Navigate to your project
cd my-awesome-portfolio

# Install dependencies
npm install

# Start development server
ongr dev
```

Your site will be available at `http://localhost:5173` 🎉

---

## 📖 Usage Guide

### Essential Commands

```bash
# Development
ongr dev              # Start development server
ongr build            # Build for production

# Content Creation
ongr generate blog "My First Post"     # Create a new blog post
ongr g b "Another Post"                # Short form
ongr generate project "Cool App"       # Create a new project
ongr g p "My Project"                  # Short form

# Content Processing
ongr load             # Preprocess content files
ongr l                # Short form

# Deployment
ongr deploy           # Deploy to GitHub Pages
ongr d                # Short form
```

### Content Structure

```
my-portfolio/
├── README.md
├── config.yaml
├── onigiri.config.json
├── package.json
├── public/
│   ├── 404.html
│   ├── content/
│   │   ├── assets/
│   │   │   └── markdown.png
│   │   ├── blogs/
│   │   │   └── markdown-demo/
│   │   │       └── index.md
│   │   └── projects/
│   │       └── sample-project/
│   │           └── index.md
│   ├── data/
│   │   ├── blogs.json
│   │   ├── file-metadata.json
│   │   ├── projects.json
│   │   └── types.ts
│   ├── default_cover.jpg
│   ├── favicon.png
│   └── vite.svg
└── templates/
    ├── blog-template.md
    └── project-template.md
```

---

## ⚙️ Configuration

### Main Configuration (`config.yaml`)

```yaml
# Website configuration
website:
  title: "Your Title"
  titleSeparator: " | "
  favicon: "/favicon.png"
  description: "Portfolio website of Your Name. Customize this description with your own information."

# Background configuration
backgrounds:
  global: "your website background"  # Global background
  hero: "your hero image"   # Hero section background

# Home page configuration
home:
  hero:
    name: "YOUR NAME"
    quote: "Your inspiring quote or tagline here."

  profileCard:
    name: "Your Name"
    title: "Your Job Title"
    subtitle: "Your Subtitle"
    avatar: "favicon.png"

# ...

# Footer configuration
footer:
  copyright: "© yyyy by Your Name. All rights reserved."
  message: "Welcome to my portfolio website!"
```

### Build Configuration (`onigiri.config.json`)

```json
{
  "baseUrl": "/",
  "dev": {
    "port": 5173,
    "open": true
  }
}
```

---

## 📝 Writing Content

### Blog Post Example

```markdown
---
title: "My Amazing Blog Post"
createTime: "2025-06-17T10:00:00.000Z"
category: "Technology"
description: "A comprehensive guide to..."
tags: ["React", "TypeScript", "Web Development"]
coverImage: "./cover.jpg"  <!-- Relative path to public folder -->
---

# My Amazing Blog Post

Your content goes here...

## Features

- Markdown support
- Code highlighting
- Math equations: $E = mc^2$
- And much more!
```

### Project Example

```markdown
---
title: "Awesome Project"
createTime: "2025-06-17T10:00:00.000Z"
category: "Web Development"
description: "A revolutionary web application"
tags: ["React", "Node.js", "MongoDB"]
coverImage: "./screenshot.png"
---

# Awesome Project

Project description and documentation...
```

---

## 🚀 Deployment

### GitHub Pages (Recommended)

1. **Configure your repository**:
  onigiri.config.json
   ```json
   {
     "baseUrl": "/your-repo-name/"
   }
   ```

1. **Build and deploy**:
   ```bash
   ongr build
   ongr deploy
   ```

2. **Enable GitHub Pages**:
   - Go to your repository settings
   - Enable GitHub Pages from the `gh-pages` branch

### Other Platforms

Not available yet, but you can deploy to any static hosting service like Netlify or Vercel by following their documentation.

---

## 🎨 Customization

### Themes and Styling

Onigiri Press uses CSS modules for styling. You can customize:

- Colors and typography in CSS files
- Layout components in React
- Background images and assets
- Component styles and animations

### Advanced Configuration

- Custom Vite plugins
- Additional markdown-it plugins
- Custom React components
- Build optimizations

---

## 🤝 Contributing

Contributions are welcomed! Feel free to open issues or submit pull requests to help improve Onigiri Press.

### Development Setup

```bash
# Clone the repository
git clone https://github.com/HuJacobJiabao/onigiri-press.git

# Install dependencies
npm install

# Start development
npm run dev

# Build for production
npm run build
```

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Inspired by the simplicity and elegance of Japanese design philosophy
- Built with modern web technologies and best practices
- Thanks to all contributors and the open-source community

---

## 📞 Support
- 🐛 [Issue Tracker](https://github.com/HuJacobJiabao/onigiri-press/issues)

---

<div align="center">
  
  **Made with 🍙 and ❤️**
  
  *Onigiri Press - Simple. Beautiful. Functional.*
  
</div>
