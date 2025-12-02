# Estes Park Transportation Guide - Denver Sam Subdomain

A focused, user-oriented landing page for Denver Sam's Estes Park car service. This page is designed as a subdomain/subpage of denversam.com, specifically targeting customers looking for reliable transportation from Denver to Estes Park and Rocky Mountain National Park.

## Purpose

This is NOT a standalone tourism site. This is part of Denver Sam's car hire service website, focusing on:
- Estes Park as a destination Sam serves from Denver
- User intent: Finding reliable transportation to Estes Park
- Conversion: Booking rides through denversam.com
- SEO: Ranking for "Denver to Estes Park transportation" keywords

## Features

- **Brand Consistency** - Matches denversam.com design and branding perfectly
- **User-Oriented** - Simple, effective layout focused on user intent (booking transportation)
- **Responsive Design** - Works seamlessly on desktop, tablet, and mobile devices
- **SEO Optimized** - CTR-friendly titles and meta descriptions for transportation keywords
- **Conversion Focused** - All CTAs link to denversam.com booking form
- **Google Analytics** - Integrated tracking with GA4 and Google Tag Manager

## What's Included

### Content Sections

1. **Hero Section** - Clear value proposition: Safe rides to Estes Park from Denver
2. **Why Choose Sam** - Trust-building content from Sam's perspective (first person)
3. **Where I'll Take You** - Specific destinations Sam serves in Estes Park area
4. **What You Can Do** - Activities passengers can enjoy (from driver's perspective)
5. **Best Times to Visit** - Seasonal guide showing year-round service
6. **FAQ Section** - 8 service-specific questions passengers actually ask
7. **Booking CTA** - Direct link to denversam.com booking form
8. **Footer** - Matches denversam.com footer exactly with all links back to main site

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

## Deployment Options

This page can be deployed as:
1. **Subdomain**: estes.denversam.com (recommended)
2. **Subdirectory**: denversam.com/estes
3. **Separate GitHub Pages**: username.github.io/estes (for testing)

### Subdomain Setup (Recommended)

To set up as estes.denversam.com:

1. Deploy to GitHub Pages (see instructions below)
2. In your domain registrar (where you bought denversam.com), add a CNAME record:
   - Type: CNAME
   - Name: estes
   - Value: yourusername.github.io
3. In your GitHub repository settings > Pages, add custom domain: estes.denversam.com
4. Wait for DNS propagation (can take up to 24 hours)

### GitHub Pages Deployment

#### Quick Setup

1. **Create a GitHub Repository**
   - Go to GitHub and create a new repository
   - Name it `estes` or `estes-denversam`

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

**Parent Site**: denversam.com (Denver Sam Car Hire Service)
**Purpose**: Estes Park transportation landing page / subdomain
**Design**: Matches Denver Sam WordPress theme exactly
**Built With**: HTML5, CSS3, JavaScript (ES6+)
**Fonts**: Inter by Rasmus Andersson
**Analytics**: Google Analytics 4 & Google Tag Manager

## Important Links

- **Main Site**: https://denversam.com
- **Booking Form**: https://denversam.com/#booking-form
- **Phone**: (720) 900-5430
- **Email**: info@denversam.com

All "Book Now" CTAs on this page direct to the main denversam.com booking form.

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

**Ready to Deploy?** Follow the GitHub Pages setup instructions above and your subdomain will be live in minutes!

**Part of Denver Sam Car Hire Service** - Professional, reliable transportation throughout Colorado. Visit [denversam.com](https://denversam.com) to learn more or book your ride.
