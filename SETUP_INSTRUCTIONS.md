# Tipsy On Life - Setup Instructions

This document provides step-by-step instructions to complete the setup of your new MkDocs website.

## What Has Been Built

A complete, production-ready website with:

- ✅ **Responsive Design** - Works on all devices
- ✅ **Light & Dark Mode** - Toggle between themes
- ✅ **Accessibility** - WCAG-compliant design
- ✅ **Gradient Theme** - Beautiful purple gradient color scheme
- ✅ **Hero Images** - Eye-catching images on each page
- ✅ **Blog System** - Ready to add posts
- ✅ **Contact Page** - Form and social links
- ✅ **GitHub Actions** - Automatic deployment

## Quick Start (Local Development)

1. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

2. **Run Development Server**
   ```bash
   mkdocs serve
   ```

3. **View Site**
   Open http://127.0.0.1:8000 in your browser

## Deploying to GitHub Pages

### Step 1: Enable GitHub Pages

1. Go to your repository: https://github.com/ektakamboj/tipsyonlife
2. Click **Settings** (top right)
3. Click **Pages** (left sidebar)
4. Under "Build and deployment":
   - Source: **GitHub Actions**
5. Save changes

### Step 2: Merge and Deploy

1. Merge this pull request into the `main` branch
2. GitHub Actions will automatically build and deploy
3. Your site will be live at: `https://ektakamboj.github.io/tipsyonlife/`
4. Initial deployment takes 2-5 minutes

## Configure Contact Form (Important!)

The contact form currently has a placeholder and **will not work** until configured.

### Option 1: Formspree (Recommended)

1. Go to https://formspree.io and sign up (free)
2. Create a new form
3. Copy your form ID
4. Edit `docs/contact.md`, line 14
5. Replace `YOUR_FORM_ID` with your actual form ID
6. Commit and push changes

### Option 2: Alternative Services

You can also use:
- Netlify Forms (if deploying to Netlify)
- Google Forms (embed an iframe)
- Custom backend (if you have one)

## Customization Guide

### Change Colors

Edit `docs/stylesheets/extra.css`, lines 4-7:

```css
:root {
  --gradient-start: #667eea;  /* Change this */
  --gradient-end: #764ba2;    /* And this */
}
```

### Replace Hero Images

Replace these SVG files with your own images:
- `docs/assets/images/hero-home.svg`
- `docs/assets/images/hero-blog.svg`
- `docs/assets/images/hero-contact.svg`

### Update Site Information

Edit `mkdocs.yml`:
- Lines 1-4: Site name, description, author
- Line 119: Add your social media links

### Add Social Media Links

Edit `mkdocs.yml`, lines 114-117:

```yaml
extra:
  social:
    - icon: fontawesome/brands/github
      link: https://github.com/yourusername
    - icon: fontawesome/brands/twitter
      link: https://twitter.com/yourusername
    - icon: fontawesome/brands/linkedin
      link: https://linkedin.com/in/yourusername
```

## Adding Blog Posts

### Create a New Post

1. Create a new file: `docs/blog/posts/my-new-post.md`

2. Add content:
   ```markdown
   # My New Post
   
   *January 30, 2024*
   
   Your content here...
   ```

3. Update `docs/blog/index.md` to list the new post:
   ```markdown
   <div class="blog-card">
     <h3><a href="posts/my-new-post.md">My New Post</a></h3>
     <p><em>January 30, 2024</em></p>
     <p>Brief description...</p>
     <a href="posts/my-new-post.md">Read more →</a>
   </div>
   ```

4. Commit and push - automatic deployment!

## Future Enhancements

Consider adding:
- 📧 Email subscription/newsletter
- 💬 Comments system (Disqus, Utterances)
- 📊 Analytics (Google Analytics)
- 🔍 Enhanced SEO metadata
- 📱 PWA features
- ��️ Image galleries
- 🎨 More page templates

## Troubleshooting

### Build Fails

If `mkdocs build` fails:
1. Check Python version: `python --version` (should be 3.x)
2. Reinstall dependencies: `pip install -r requirements.txt`
3. Check for syntax errors in `.md` files

### Site Not Deploying

1. Check GitHub Actions tab for errors
2. Verify GitHub Pages is enabled (Settings → Pages)
3. Ensure you merged to `main` branch
4. Check repository Settings → Actions → General → Workflow permissions

### Contact Form Not Working

1. Verify you replaced `YOUR_FORM_ID` in `docs/contact.md`
2. Check Formspree dashboard for form status
3. Test the form with a real email

## Support

For issues:
- Check the documentation: https://squidfunk.github.io/mkdocs-material/
- GitHub Issues: https://github.com/ektakamboj/tipsyonlife/issues
- MkDocs Material Discord: https://discord.gg/squidfunk

## Next Steps

1. ✅ Merge this PR
2. ✅ Enable GitHub Pages
3. ✅ Configure contact form
4. ✅ Customize colors and content
5. ✅ Add your first blog post
6. ✅ Share your new website!

Enjoy your new website! 🎉
