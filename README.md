# Armadale Landing Page Maintenance Guide

This guide will help you maintain and customize the Armadale Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

```html
<!-- Company Name -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Armadale  <!-- Change this text to update company name -->
</a>
```

**Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>  <!-- Update text here -->
    <a href="#benefits">Benefits</a>  <!-- Update text here -->
    <a href="#contact">Contact</a>    <!-- Update text here -->
</div>
```

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-7xl font-bold leading-tight mb-6">
    Building financial clarity in a complex world  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Professional accounting services...  <!-- Subheadline -->
</p>
```

### Tailwind CSS Class Guide
Common classes used throughout:
- Text sizes: `text-xl`, `text-2xl`, `text-4xl`
- Colors: `text-gray-300`, `text-white`
- Spacing: `mb-6`, `py-24`, `px-6`
- Responsive design: `md:text-5xl`, `lg:text-7xl`

To modify styles:
1. Find the element you want to change
2. Locate its class attribute
3. Add or modify Tailwind classes
4. Test on different screen sizes

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://theaccountants.com">Get Started</a>
<!-- Update this URL to your actual service page -->
```

3. Footer Links:
```html
<!-- Services Section -->
<li><a href="#">Business Valuation</a></li>
<li><a href="#">Audit Preparation</a></li>
<li><a href="#">Compliance Monitoring</a></li>

<!-- Company Section -->
<li><a href="#">About Us</a></li>
<li><a href="#">Careers</a></li>
<li><a href="#">Contact</a></li>
```

### How to Update Links
1. Internal Links (same page):
   ```html
   <!-- Format: -->
   <a href="#section-id">Link Text</a>
   ```

2. External Links:
   ```html
   <!-- Format: -->
   <a href="https://full-website-url.com">Link Text</a>
   ```

3. Email Links:
   ```html
   <!-- Update with your email -->
   <a href="mailto:support@example.com">support@example.com</a>
   ```

## Linking Privacy and Terms Pages

### Adding Footer Links
Add these links to the footer's Company section:

```html
<div>
    <h4 class="font-semibold mb-4">Company</h4>
    <ul class="space-y-2 text-gray-400">
        <!-- Existing links -->
        <li><a href="#" class="hover:text-white transition-colors duration-300">About Us</a></li>
        <!-- Add new links below -->
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Policy Pages
1. Create two new files:
   - `privacy.html`
   - `terms.html`
2. Use the same styling classes for consistency
3. Link back to main page:
   ```html
   <a href="index.html">Return to Home</a>
   ```

## Troubleshooting

### Common Issues
1. Broken Links:
   - Check for typos in `href` attributes
   - Verify file names match exactly
   - Ensure files are in the correct directory

2. Styling Problems:
   - Confirm Tailwind CSS is properly loaded
   - Check for missing or mistyped classes
   - Verify responsive classes use correct breakpoints (`md:`, `lg:`)

3. Layout Issues:
   - Check container classes: `container mx-auto px-6`
   - Verify grid classes: `grid grid-cols-1 md:grid-cols-3`
   - Test on different screen sizes

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check browser developer tools (F12) for errors
- Ensure all files are in the correct directory structure

Remember to always test changes across different devices and screen sizes before deploying to production.