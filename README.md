# Photo-Shoot Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Photo-Shoot landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

```html
<!-- Original -->
<div class="text-2xl font-bold">Photo-Shoot</div>

<!-- How to modify -->
<div class="text-2xl font-bold">Your Brand Name</div>
```

**Key Tailwind Classes Explained:**
- `text-2xl`: Sets large text size
- `font-bold`: Makes text bold
- `container mx-auto`: Centers content and sets maximum width
- `px-4`: Adds horizontal padding

### Hero Section
The main banner section contains:

```html
<h1 class="text-4xl md:text-6xl font-bold mb-6">Photo-Shoot</h1>
<p class="text-xl md:text-2xl mb-8">Get the ultimate product photography lightbox</p>
```

**To Modify Text:**
1. Locate the `<h1>` tag for the main heading
2. Change the text between the tags
3. For the subtitle, modify the `<p>` tag content

**Responsive Design Classes:**
- `md:text-6xl`: Larger text on medium screens
- `text-4xl`: Default text size on mobile
- `mb-6`: Margin bottom spacing

### Features Section
Each feature card follows this structure:

```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 text-4xl mb-4">
        <i class="fas fa-usb"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">USB Powered</h3>
    <p class="text-gray-600">Connect to any USB port for consistent, reliable power supply</p>
</div>
```

**To Add/Modify Features:**
1. Copy the entire feature card `div`
2. Change the icon class (`fas fa-usb`)
3. Update the heading and description text
4. Maintain the existing classes for consistent styling

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```

**To Update Links:**
1. Locate the `href` attribute
2. For internal sections, use `#section-id`
3. For external links, use the full URL: `https://example.com`

### Buy Now Button Links
The current Stripe payment link appears multiple times:

```html
<a href="https://buy.stripe.com/14k5mM58ObjBbRK000" class="bg-blue-600 text-white px-6 py-2 rounded-full">Buy Now</a>
```

**To Update Payment Link:**
1. Replace the Stripe URL with your new payment link
2. Maintain the existing classes for consistent styling
3. Update all instances of the buy button throughout the page

## Linking Privacy and Terms Pages

### Footer Policy Links
Current footer policy section:

```html
<div>
    <h4 class="text-xl font-bold mb-4">Policies</h4>
    <ul class="space-y-2 text-gray-400">
        <li>Shipping Policy</li>
        <li>Return Policy</li>
        <li>Privacy Policy</li>
        <li>Terms of Service</li>
    </ul>
</div>
```

**To Add Policy Links:**
1. Modify each `<li>` to include an anchor tag:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

2. Create corresponding HTML files (privacy.html, terms.html) in the same directory
3. Maintain consistent styling by adding the same classes used in other footer links

## Troubleshooting

### Common Issues and Solutions

1. **Broken Responsive Design**
   - Check for `md:` prefixed classes
   - Ensure container classes remain intact
   - Verify the viewport meta tag is present

2. **Misaligned Elements**
   - Check for proper grid classes (`grid-cols-1 md:grid-cols-2`)
   - Verify padding and margin classes
   - Ensure container classes are properly nested

3. **Icon Not Displaying**
   - Verify Font Awesome CDN link in header
   - Check icon class names against Font Awesome documentation
   - Ensure proper icon prefix (`fas`, `fab`, etc.)

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Inspect elements using browser developer tools
- Test responsive design using browser device emulation

Remember to always test changes across different screen sizes and browsers before deploying to production.