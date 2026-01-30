# Tipsy On Life

A modern, responsive website built with MkDocs and Material theme, featuring a blog and contact page.

## Features

- ✨ **Responsive Design**: Works beautifully on desktop, tablet, and mobile
- 🌗 **Light/Dark Mode**: Toggle between themes with automatic preference saving
- ♿ **Accessible**: Built with WCAG standards in mind
- 🎨 **Gradient Theme**: Beautiful gradient color scheme
- 🖼️ **Hero Images**: Eye-catching hero images on every page
- 📝 **Blog**: Easy-to-manage blog with post organization
- 📧 **Contact Page**: Contact form and social media links

## Quick Start

### Prerequisites

- Python 3.x
- pip

### Installation

1. Clone the repository:
```bash
git clone https://github.com/ektakamboj/tipsyonlife.git
cd tipsyonlife
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

### Local Development

Run the development server:
```bash
mkdocs serve
```

The site will be available at `http://127.0.0.1:8000`

### Building

Build the static site:
```bash
mkdocs build
```

The built site will be in the `site/` directory.

## Deployment

### GitHub Pages

This repository is configured to automatically deploy to GitHub Pages when you push to the `main` branch.

**Setup Instructions:**

1. Go to your repository settings
2. Navigate to "Pages" in the left sidebar
3. Under "Build and deployment", select "GitHub Actions" as the source
4. Push to the `main` branch to trigger deployment

The site will be available at: `https://ektakamboj.github.io/tipsyonlife/`

### Azure Static Web Apps (Coming Soon)

Instructions for deploying to Azure Static Web Apps will be added in a future update.

## Project Structure

```
tipsyonlife/
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions workflow
├── docs/
│   ├── assets/
│   │   └── images/            # Hero images
│   ├── blog/
│   │   ├── index.md           # Blog index page
│   │   └── posts/             # Blog posts
│   ├── stylesheets/
│   │   └── extra.css          # Custom CSS
│   ├── index.md               # Home page
│   └── contact.md             # Contact page
├── mkdocs.yml                 # MkDocs configuration
├── requirements.txt           # Python dependencies
└── README.md                  # This file
```

## Adding Blog Posts

1. Create a new markdown file in `docs/blog/posts/`
2. Add your content using Markdown
3. Update `docs/blog/index.md` to include your new post
4. Commit and push - the site will automatically rebuild!

## Customization

### Colors

Edit the gradient colors in `docs/stylesheets/extra.css`:

```css
:root {
  --gradient-start: #667eea;
  --gradient-end: #764ba2;
}
```

### Theme

Modify the theme settings in `mkdocs.yml`:

```yaml
theme:
  palette:
    - scheme: default
      primary: deep purple
      accent: pink
```

### Hero Images

Replace the SVG images in `docs/assets/images/` with your own images.

## Contact Form Setup

The contact form uses Formspree. To activate it:

1. Sign up at [Formspree.io](https://formspree.io)
2. Create a new form
3. Replace `YOUR_FORM_ID` in `docs/contact.md` with your form ID

## License

This project is licensed under the terms specified in the LICENSE file.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Support

For issues or questions, please open an issue on GitHub or use the contact form on the website.
