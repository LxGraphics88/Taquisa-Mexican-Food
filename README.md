# Taquisa Mexican Food Website

A beautiful, responsive single-page website for Taquisa Mexican Food restaurant. This website is designed to be easily hosted on GitHub Pages.

## Quick Start - Deploy to GitHub Pages

### Option 1: Using GitHub Website (Easiest)

1. Create a new GitHub repository
2. Upload all files from this folder to the repository
3. Go to **Settings** → **Pages**
4. Under "Source", select **Deploy from a branch**
5. Select the **main** branch and **/ (root)** folder
6. Click **Save**
7. Wait 1-2 minutes, then visit `https://yourusername.github.io/repository-name`

### Option 2: Using Git Command Line

```bash
# Navigate to this folder
cd github-pages-site

# Initialize git repository
git init

# Add all files
git add .

# Create first commit
git commit -m "Initial commit - Taquisa Mexican Food website"

# Create main branch
git branch -M main

# Add your GitHub repository as remote (replace with your repo URL)
git remote add origin https://github.com/yourusername/your-repo-name.git

# Push to GitHub
git push -u origin main
```

Then enable GitHub Pages in your repository settings.

---

## Customization Guide

### Changing Colors

Open `css/styles.css` and find the `:root` section at the top. Here you can easily change the color scheme:

```css
:root {
  /* Primary Colors - Change these to customize your theme */
  --primary: #d97706;          /* Main brand color (orange) */
  --primary-dark: #b45309;     /* Darker shade for hover effects */
  --primary-light: #f59e0b;    /* Lighter shade for accents */
  
  /* Secondary Colors */
  --secondary: #dc2626;        /* Secondary color (red) */
  --accent: #eab308;           /* Accent color (gold) */
  
  /* Background Colors */
  --bg-light: #faf7f5;         /* Page background */
  --bg-card: #f5f0ed;          /* Card backgrounds */
  --bg-dark: #1f1a17;          /* Dark sections */
  
  /* Text Colors */
  --text-primary: #3d3530;     /* Main text color */
  --text-secondary: #6b5c52;   /* Secondary text */
  --text-light: #f5f0ed;       /* Light text on dark bg */
}
```

#### Color Scheme Examples

**Blue Theme:**
```css
--primary: #2563eb;
--primary-dark: #1d4ed8;
--primary-light: #3b82f6;
```

**Green Theme:**
```css
--primary: #059669;
--primary-dark: #047857;
--primary-light: #10b981;
```

**Purple Theme:**
```css
--primary: #7c3aed;
--primary-dark: #6d28d9;
--primary-light: #8b5cf6;
```

---

### Changing Restaurant Information

#### Restaurant Name
In `index.html`, search for "TAQUISA" and replace with your restaurant name:
- Hero section title
- Navigation logo
- Footer logo

#### Contact Information
Find the `contact-section` in `index.html` and update:
- Address
- Phone number
- Hours of operation

#### About Section
Find the `about-section` in `index.html` and update:
- Your restaurant's story
- Years of operation
- Tagline

---

### Changing Menu Items

In `index.html`, find the `menu-grid` section. Each menu item follows this structure:

```html
<div class="menu-card">
  <div class="menu-card-content">
    <div class="menu-card-header">
      <h3 class="menu-item-name">Your Dish Name</h3>
      <span class="menu-item-price">$XX.XX</span>
    </div>
    <p class="menu-item-description">Description of your dish</p>
    <div class="spice-level">
      <!-- Add/remove 🌶️ for spice level -->
      <span class="flame">🌶️</span>
    </div>
  </div>
</div>
```

**To add a new menu item:** Copy and paste this structure inside the `menu-grid` div.

**To remove a menu item:** Delete the entire `menu-card` div.

**To change spice level:** Add or remove `<span class="flame">🌶️</span>` elements.

---

### Changing Images

1. Replace images in the `images/` folder with your own photos
2. Keep the same filenames, OR update the filenames in:
   - `index.html` (gallery and about sections)
   - `css/styles.css` (hero background in `.hero` class)

#### Recommended Image Sizes
- **Hero image:** 1920x1080 pixels (landscape)
- **Gallery images:** 800x600 pixels (landscape)
- **About image:** 800x800 pixels (square or landscape)

---

### Changing Fonts

The website uses Google Fonts. To change fonts:

1. Go to [Google Fonts](https://fonts.google.com/)
2. Select your fonts
3. Copy the `<link>` tag and replace the existing one in `index.html` `<head>`
4. Update the font names in `css/styles.css`:

```css
:root {
  --font-display: 'Your Display Font', sans-serif;    /* For headings */
  --font-heading: 'Your Heading Font', sans-serif;    /* For subheadings */
  --font-body: 'Your Body Font', sans-serif;          /* For regular text */
  --font-accent: 'Your Accent Font', cursive;         /* For special text */
}
```

---

### Adding Social Media Links

In the footer section of `index.html`, find the `social-links` div and update the `href` attributes:

```html
<div class="social-links">
  <a href="https://facebook.com/yourpage" class="social-link">FB</a>
  <a href="https://instagram.com/yourpage" class="social-link">IG</a>
  <a href="https://twitter.com/yourpage" class="social-link">TW</a>
</div>
```

---

### Adding New Sections

To add a new section:

1. Add a navigation link in the `nav-links` list:
```html
<li><a href="#newsection">New Section</a></li>
```

2. Add the section content:
```html
<section id="newsection" class="section">
  <div class="container">
    <div class="section-header">
      <h2 class="section-title">NEW SECTION</h2>
      <div class="section-divider"></div>
      <p class="section-subtitle">Your subtitle here</p>
    </div>
    <!-- Your content here -->
  </div>
</section>
```

---

### Form Functionality

The contact form currently shows an alert message. To make it actually send emails:

1. Use a service like [Formspree](https://formspree.io/), [Netlify Forms](https://www.netlify.com/products/forms/), or [EmailJS](https://www.emailjs.com/)
2. Update the form action or JavaScript as per their instructions

#### Example with Formspree:
```html
<form action="https://formspree.io/f/yourformid" method="POST">
```

---

## File Structure

```
github-pages-site/
├── index.html          # Main HTML file
├── css/
│   └── styles.css      # All styling
├── js/
│   └── script.js       # JavaScript functionality
├── images/
│   ├── mexican_food_tacos_b_219be329.jpg
│   ├── mexican_food_tacos_b_6e9d21fb.jpg
│   └── mexican_food_tacos_b_24a71fc3.jpg
└── README.md           # This file
```

---

## Browser Support

This website works in all modern browsers:
- Chrome (recommended)
- Firefox
- Safari
- Edge

---

## Need Help?

If you run into issues:
1. Check that all files are in the correct folders
2. Make sure image filenames match exactly
3. Clear your browser cache after making changes
4. Check the browser console for JavaScript errors (F12 → Console)

---

## License

Free to use and modify for your restaurant website.

---

**Enjoy your new website! ¡Buen Provecho!** 🌮
