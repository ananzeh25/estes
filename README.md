# Estes Park, Colorado - Information Guide

A beautiful, responsive static website guide for Estes Park, Colorado. Built with clean HTML, CSS, and JavaScript, perfect for GitHub Pages deployment.

## Features

- **Responsive Design** - Works seamlessly on desktop, tablet, and mobile devices
- **Accessible** - WCAG 2.1 compliant with proper semantic HTML and ARIA labels
- **Fast Loading** - Optimized static site with minimal dependencies
- **SEO Optimized** - Proper meta tags and structured content
- **Google Analytics** - Integrated tracking with GA4 and Google Tag Manager
- **Modern UI** - Clean design matching the Denver Sam WordPress theme aesthetic

## What's Included

### Content Sections

1. **Hero Section** - Welcoming introduction with call-to-action buttons
2. **About Estes Park** - Conversational overview of the town
3. **Hotels** - 6 categories of accommodations
4. **Restaurants** - 6 types of dining options
5. **Attractions** - Must-see destinations and activities
6. **Parks & Natural Areas** - Outdoor recreation spots
7. **Activities** - Adventure opportunities
8. **FAQ Section** - 10 commonly asked questions with detailed answers
9. **Booking CTA** - Call-to-action for planning visits
10. **Footer** - Comprehensive navigation and resources

### Technical Features

- Mobile-friendly hamburger menu
- Smooth scrolling navigation
- Sticky header (desktop only)
- Google Analytics event tracking
- Scroll depth tracking
- External link tracking
- Print-friendly styles
- Reduced motion support for accessibility

## Files Structure

```
estes/
├── index.html          # Main HTML file
├── style.css           # All styling
├── script.js           # JavaScript functionality
├── README.md           # This file
└── .github/
    └── workflows/
        └── static.yml  # GitHub Actions workflow
```

## Google Analytics Setup

The site is pre-configured with the following Google Analytics properties:

- **Account ID**: 273637222
- **Property ID**: 384277476
- **Measurement ID**: G-LLL4VPHMHH
- **Tag ID**: GT-5N2922J

Analytics tracks:
- Page views
- CTA button clicks
- Scroll depth (25%, 50%, 75%, 100%)
- Outbound link clicks

## Local Development

### View Locally

1. Clone or download this repository
2. Open `index.html` in your web browser
3. That's it! No build process or server required.

### Using a Local Server (Recommended)

For a more accurate preview, use a local server:

**Python 3:**
```bash
python -m http.server 8000
```

**Python 2:**
```bash
python -m SimpleHTTPServer 8000
```

**Node.js (http-server):**
```bash
npx http-server
```

Then visit `http://localhost:8000` in your browser.

## GitHub Pages Deployment

### Quick Setup

1. **Create a GitHub Repository**
   - Go to GitHub and create a new repository
   - Name it anything you like (e.g., `estes-park-guide`)

2. **Upload Your Files**
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Estes Park guide"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**
   - Go to your repository Settings
   - Scroll to "Pages" section
   - Under "Source", select "Deploy from a branch"
   - Select branch: `main` and folder: `/ (root)`
   - Click Save

4. **Access Your Site**
   - Your site will be available at: `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`
   - It may take a few minutes for the first deployment

### Using GitHub Actions (Already Configured)

The repository includes a GitHub Actions workflow (`.github/workflows/static.yml`) that automatically deploys your site. This workflow:

- Runs on every push to the `main` branch
- Uses the static site deployment action
- Requires no additional configuration

**To use it:**

1. Make sure the `.github/workflows/static.yml` file is in your repository
2. Go to Settings > Pages
3. Set Source to "GitHub Actions"
4. Push changes to trigger automatic deployment

## Customization Guide

### Update Content

**Edit Text Content:**
- Open `index.html`
- Find the section you want to modify
- Update the text between HTML tags
- Save and refresh

**Add New Cards:**
```html
<article class="category-card">
    <div class="card-icon">YOUR LABEL</div>
    <h3 class="card-title">Your Title</h3>
    <p class="card-description">
        Your description text here (approximately 40 words)
    </p>
</article>
```

### Change Colors

Edit `style.css` and modify these variables:

```css
/* Primary Colors */
#2c3e50  /* Dark blue/slate - main brand color */
#3498db  /* Bright blue - accent color */
#1f2937  /* Dark gray - footer background */
#f8f9fa  /* Light gray - alternate sections */

/* Text Colors */
#333     /* Main text */
#666     /* Secondary text */
#fff     /* White text */
```

### Update Fonts

The site uses **Inter** font family. To change:

1. Edit the Google Fonts link in `index.html`:
```html
<link href="https://fonts.googleapis.com/css2?family=YOUR-FONT:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

2. Update font-family in `style.css`:
```css
body {
    font-family: 'YOUR-FONT', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
}
```

### Modify Navigation

Edit the menu in `index.html`:

**Desktop (header):**
```html
<div class="header-contact">
    <a href="#booking" class="book-now-btn">Book Me Now</a>
</div>
```

**Mobile (hamburger menu):**
```html
<nav>
    <ul role="list">
        <li><a href="#section">Section Name</a></li>
        <!-- Add more items -->
    </ul>
</nav>
```

### Update Analytics

To use different Google Analytics IDs:

1. Open `index.html`
2. Find the `<script>` tag in the `<head>`
3. Replace the IDs:
```javascript
gtag('config', 'G-YOUR-MEASUREMENT-ID');
gtag('config', 'GT-YOUR-TAG-ID');
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Accessibility Features

- Semantic HTML5 elements
- ARIA labels and roles
- Skip to main content link
- Keyboard navigation support
- Focus indicators
- Alt text ready (for images when added)
- Reduced motion support
- High contrast mode support
- Screen reader friendly

## Performance

- No external dependencies (except Google Fonts and Analytics)
- Optimized CSS with minimal bloat
- Efficient JavaScript with event delegation
- Fast initial load time
- Mobile-optimized

## SEO Features

- Semantic HTML structure
- Meta description
- Proper heading hierarchy (h1, h2, h3)
- Descriptive page title
- Alt text support for images
- Mobile-responsive design
- Fast loading speed

## Maintenance

### Regular Updates

1. **Content Updates**: Edit `index.html` directly
2. **Style Changes**: Modify `style.css`
3. **Functionality**: Update `script.js`

### Testing Checklist

- [ ] Test on mobile devices
- [ ] Check all links work
- [ ] Verify mobile menu functions
- [ ] Test on different browsers
- [ ] Validate HTML (https://validator.w3.org/)
- [ ] Check accessibility (https://wave.webaim.org/)
- [ ] Test page speed (https://pagespeed.web.dev/)

## Credits

**Design Based On**: Denver Sam WordPress Theme
**Location**: Estes Park, Colorado
**Built With**: HTML5, CSS3, JavaScript (ES6+)
**Fonts**: Inter by Rasmus Andersson
**Analytics**: Google Analytics 4 & Google Tag Manager

## License

This is a custom website. Modify and use as needed for your purposes.

## Support

For questions or issues:
1. Check this README first
2. Review the code comments in HTML, CSS, and JS files
3. Test in different browsers
4. Verify GitHub Pages settings

## Version History

- **v1.0** (2024) - Initial release
  - Full responsive design
  - Google Analytics integration
  - Comprehensive Estes Park content
  - Mobile menu functionality
  - Accessibility features

---

**Ready to Deploy?** Follow the GitHub Pages setup instructions above and your site will be live in minutes!

Visit [Estes Park Official Site](https://www.estes.org) for more information about this beautiful Colorado mountain town.
