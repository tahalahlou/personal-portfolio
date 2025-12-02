# Taha Lahlou – Personal Portfolio

[![Hugo Version](https://img.shields.io/static/v1?label=HUGO&message=extended&color=blue&logo=hugo)](https://gohugo.io/)
[![Theme](https://img.shields.io/badge/theme-Hugo%20Noir-blue)](https://github.com/prxshetty/hugo-noir)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Live Site](https://img.shields.io/badge/live%20site-tahalahlou.dev-blue)](https://tahalahlou.dev)

A modern, responsive personal portfolio built with Hugo and the Hugo Noir theme.  
It showcases my experience, projects, tech stack, and ways to get in touch — all in a clean dark-mode–friendly layout.

---

## 🌟 Features

- **Responsive Design** – Optimized for mobile & desktop  
- **Dark & Light Mode** – System-based + manual toggle  
- **Fast Performance** – Hugo static site generation  
- **Minimal Professional Layout** – Clean, readable, simple  
- **Tech Stack Icons** – Quick overview of tools I use  
- **Experience Timeline** – Featuring roles like Amazon SDE Intern  
- **Project Showcase** – Full-stack and AI-focused projects  
- **Local Time Display** – Real-time clock in the header  
- **SEO Optimized** – Meta tags, sitemap, best practices  

---

## 🚀 Live Demo

**https://tahalahlou.dev**

---

## 🛠️ Built With

- **Hugo** — Static site generator  
- **Hugo Noir Theme** — Minimal, dark-mode friendly theme  
- **Tailwind CSS** — Utility-first CSS  
- **Go Modules** — Dependency management  

---

## 📁 Project Structure

```
personal-portfolio/
├── .github/workflows/        # GitHub Actions for automatic deployment to GitHub Pages
│   └── pages.yml             # Build + deploy pipeline
│
├── archetypes/               # Default content templates used by Hugo
│   └── default.md            # Base template for new pages
│
├── content/                  # Main site content (markdown pages)
│   ├── about.md              # About Me page
│   ├── contact.md            # Contact page
│   ├── experience.md         # Experience timeline
│   └── projects.md           # Project showcase
│
├── data/en/                  # Structured TOML data for content sections
│   ├── author.toml           # Author profile, social links, metadata
│   ├── experience.toml       # Work experience entries
│   └── projects.toml         # List of projects, descriptions, tech stack, links
│
├── layouts/                  # Custom layout overrides for Hugo Noir
│   ├── _default/             # Default base templates
│   ├── index.html            # Homepage layout customization
│   └── partials/             # Reusable components (navbar, footer, time display, etc.)
│
├── node_modules/             # Node dependencies (icons, tooling, build helpers)
│
├── portfolio/                # Portfolio-specific assets (images, icons, sections)
│
├── static/                   # Static files served directly (bypasses Hugo processing)
│   ├── images/               # Photos, logos, project screenshots
│   └── assets/               # Additional static files
│
├── themes/hugo-noir/         # Hugo Noir theme (installed as a submodule)
│
├── config.yaml               # Main Hugo site configuration (menus, params, SEO, baseURL)
├── package.json              # Node package config (for icons, optional tooling)
├── package-lock.json         # Node dependency lockfile
├── .gitignore                # Ignored files and folders
└── .DS_Store                 # macOS metadata (ignored in Git)
```

## 🚀 Getting Started

### Prerequisites

- **Hugo Extended** version 0.92.0 or newer
- **Git** for version control
- **Go** 1.18+ (for Hugo)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/personal-portfolio.git
   cd personal-portfolio
   ```

2. **Initialize and update submodules**
   ```bash
   git submodule update --init --recursive
   ```

3. **Install Hugo** (if not already installed)
   ```bash
   # macOS with Homebrew
   brew install hugo
   
   # Or download from https://gohugo.io/installation/
   ```

4. **Run the development server**
   ```bash
   hugo server -D
   ```

5. **Open your browser**
   Navigate to `http://localhost:1313`

## ⚙️ Configuration

### Site Configuration (`hugo.toml`)

The main configuration file contains:
- Site metadata (title, description, base URL)
- Theme settings
- Menu configuration
- Build parameters

### Content Management

#### Adding New Pages
Create new `.md` files in the `content/` directory:

```markdown
---
title: "Page Title"
date: 2023-03-15T10:30:00+05:30
draft: false
layout: "default"
description: "Page description for SEO"
---
```

#### Managing Experience Data
Edit `data/en/experience.toml` to update professional experience:

```toml
[[experience]]
company = "Company Name"
role = "Job Title"
period = "Start Date - End Date"
description = "Role description"
responsibilities = [
    "Responsibility 1",
    "Responsibility 2"
]
```

#### Managing Projects
Edit `data/en/projects.toml` to showcase projects:

```toml
[[projects]]
title = "Project Name"
description = "Project description"
tech = "Technology stack"
image = "/images/projects/project.png"
link = "https://github.com/username/project"
```

## 🎨 Customization

### Theme Modifications
The Hugo Noir theme has been customized with:
- Custom color schemes
- Enhanced typography
- Improved mobile navigation
- Local time display
- Tech stack carousel animations

### Adding Custom Styles
Create `assets/css/custom.css` for additional styling:

```css
/* Your custom CSS here */
.custom-class {
    /* Custom styles */
}
```

### Layout Overrides
To override theme layouts, copy files from `themes/hugo-noir/layouts/` to your site's `layouts/` directory and modify them.

## 📝 Content Guidelines

### Projects
- Provide clear project descriptions
- List all technologies used
- Include links to live demos and source code
- Add high-quality project images

### Experience
- Focus on achievements and impact
- Use action verbs and specific metrics
- Include relevant technologies and tools
- Keep descriptions concise but informative

## 🚀 Deployment

### Automated Deployment
The repository includes a deployment script (`scripts/deploy.sh`) that:
- Syncs the built site to a remote server
- Creates timestamped releases
- Updates the live site atomically
- Maintains deployment history

### Manual Deployment
1. Build the site: `hugo`
2. Upload the `public/` directory to your web server
3. Configure your web server to serve the static files

## 🔧 Development

### Local Development
```bash
# Start development server with live reload
hugo server -D

# Build for production
hugo

# Build with specific environment
hugo --environment production
```

### Adding Dependencies
```bash
# Add Go modules
go mod tidy
go mod download
```

## 📚 Resources

- **[Hugo Documentation](https://gohugo.io/documentation/)** - Official Hugo docs
- **[Hugo Noir Theme](https://github.com/prxshetty/hugo-noir)** - Theme documentation
- **[Tailwind CSS](https://tailwindcss.com/docs)** - CSS framework docs
- **[My Tech Blog](https://blog.michaelforde.com)** - Technical articles and tutorials

## 🤝 Contributing

While this is a personal portfolio, I welcome:
- Bug reports and feature suggestions
- Documentation improvements
- Performance optimizations
- Accessibility enhancements

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **[Pranam Shetty](https://github.com/prxshetty)** - Creator of the Hugo Noir theme
- **[Hugo Team](https://gohugo.io/)** - For the amazing static site generator
- **[Tailwind CSS](https://tailwindcss.com/)** - For the utility-first CSS framework

---

**Built with ❤️ using Hugo and the Hugo Noir theme**
