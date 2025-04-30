# Landing Page Maintenance Guide

This guide will help you maintain and customize the HK Websites landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Sections Location Guide
The page is divided into these major sections:
```html
<!-- Key sections in order -->
<header> <!-- Navigation bar at top -->
<section class="pt-32..."> <!-- Hero section -->
<section id="features"> <!-- Features section -->
<section id="benefits"> <!-- Benefits section -->
<section id="faq"> <!-- FAQ section -->
<section class="py-24 bg-blue-600"> <!-- CTA section -->
<footer> <!-- Footer section -->
```

### Updating Text Content

#### Company Name
To change the company name that appears in the header:
```html
<!-- Located in the header section -->
<a href="/" class="text-2xl font-bold text-gray-800">
    HK Websites  <!-- Change this text -->
</a>
```

#### Hero Section Text
To modify the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    Best Websites In Hong Kong  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600">
    Custom Websites For Your Business  <!-- Subheading -->
</p>
```

### Modifying Tailwind CSS Classes

#### Understanding Responsive Classes
The page uses these breakpoint prefixes:
- `md:` - Applied at medium screens (768px and up)
- `lg:` - Applied at large screens (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
<!-- text-4xl: Default size -->
<!-- md:text-5xl: Size on medium screens -->
<!-- lg:text-6xl: Size on large screens -->
```

#### Common Style Classes
- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
- Colors: `text-gray-900`, `bg-blue-600`, `text-white`
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom)
- Margins: `mb-4` (margin bottom), `mt-8` (margin top)

## Managing Links

### Navigation Menu Links
Current navigation links are in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update a link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the text between the tags

Example:
```html
<!-- Before -->
<a href="#features">Features</a>

<!-- After -->
<a href="#services">Services</a>
```

### External Links
The page contains these external links that need updating:
```html
<!-- CTA button in hero section -->
<a href="https://sigmaseo.io">Get Started Today</a>

<!-- CTA section button -->
<a href="https://sigmaseo.io">Contact Us Now</a>
```

Replace `https://sigmaseo.io` with your desired URL.

## Adding Privacy and Terms Pages

### Current Footer Links Structure
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Steps to Add Policy Pages

1. Create new HTML files:
   - Create `privacy.html`
   - Create `terms.html`

2. Update the footer links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

3. Ensure consistent styling by copying these classes to new page links:
```html
class="hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section IDs match href attributes
   - Ensure no spaces in IDs
   - IDs should start with letters, not numbers

2. **Responsive Design Issues**
   - Verify all `md:` and `lg:` classes are present
   - Test at different screen sizes
   - Don't remove container classes: `container mx-auto px-6`

3. **Style Problems**
   - Keep the Tailwind CDN link in the header
   - Don't remove class="font-sans antialiased" from body
   - Maintain the existing color scheme classes for consistency

### Need Help?
If you encounter issues:
1. Check the browser console for errors
2. Verify all CDN links are working
3. Ensure all HTML tags are properly closed
4. Compare against the original code provided above

Remember to test all changes across different devices and browsers before deploying to production.