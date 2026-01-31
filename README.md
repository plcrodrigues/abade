# WildRoots - Nature Education Website

A beautiful, responsive static website for a nature education organization that takes kids outdoors to learn and grow.

## 🌲 Features

- **Responsive Design** - Works beautifully on all devices
- **Nature-Inspired Aesthetics** - Organic shapes, earth tones, and smooth animations
- **Fast & Lightweight** - Uses Tailwind CSS via CDN, no build step required
- **Accessible** - Semantic HTML and proper contrast ratios
- **Ready for GitHub Pages** - Deploy in minutes

## 🚀 Quick Start

### Local Development

1. Clone this repository
2. Open `index.html` in your browser
3. That's it! No build process needed.

### Deploy to GitHub Pages

#### Method 1: Automatic (Recommended)

1. Push this repository to GitHub
2. Go to **Settings** → **Pages**
3. Under "Source", select **Deploy from a branch**
4. Select `main` branch and `/ (root)` folder
5. Click **Save**
6. Your site will be live at `https://yourusername.github.io/repo-name/`

#### Method 2: GitHub Actions (Optional)

Create `.github/workflows/deploy.yml`:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: .
```

## 📁 File Structure

```
wildroots/
│
├── index.html          # Main website file
└── README.md          # This file
```

## 🎨 Customization

### Colors

Edit the CSS variables in the `<style>` section of `index.html`:

```css
:root {
    --forest-deep: #1a3a2e;    /* Dark green */
    --moss-green: #4a7c59;     /* Medium green */
    --sun-gold: #f4a261;       /* Warm orange */
    --earth-brown: #8b4513;    /* Brown */
    --sky-blue: #a8dadc;       /* Light blue */
    --cream: #faf8f3;          /* Off-white background */
}
```

### Content

Simply edit the HTML content within the sections:
- **Hero Section** - Main headline and call-to-action
- **About Section** - Organization information and statistics
- **Programs Section** - Your programs/activities
- **Testimonials** - Parent/participant quotes
- **Contact Form** - Inquiry form (note: you'll need to add backend handling)

### Fonts

The site uses Google Fonts:
- **Crimson Pro** - Serif for headings
- **DM Sans** - Sans-serif for body text

To change fonts, update the Google Fonts link and CSS font-family declarations.

## 📧 Contact Form Setup

The contact form is currently frontend-only. To make it functional, you can:

1. **Formspree** - Free form handling
   - Add `action="https://formspree.io/f/YOUR_FORM_ID"` to the `<form>` tag
   
2. **Netlify Forms** - If deploying to Netlify
   - Add `netlify` attribute to the `<form>` tag
   
3. **Google Forms** - Embed or link to a Google Form
   
4. **Custom Backend** - Create your own API endpoint

## 🌐 Custom Domain

To use a custom domain with GitHub Pages:

1. Add a `CNAME` file to your repository with your domain name
2. Configure your DNS provider to point to GitHub Pages
3. Update GitHub Pages settings with your custom domain

## 🔧 Future Enhancements

Want to add more features? Consider:

- **Image Gallery** - Add photos from your programs
- **Blog/News Section** - Share updates and stories
- **Registration System** - Online signup with payment
- **Calendar Integration** - Show upcoming events
- **Migration to Vite** - For optimized builds and better development experience

## 📝 License

Free to use and modify for your organization!

## 🙏 Support

Built with ❤️ for organizations connecting kids with nature.

For questions or issues, feel free to open an issue on GitHub.
