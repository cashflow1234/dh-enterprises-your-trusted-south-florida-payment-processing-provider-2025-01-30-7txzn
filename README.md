# DH Enterprises Landing Page Maintenance Guide

This guide will help you maintain and customize the DH Enterprises landing page. It's designed for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. Company Name:
```html
<div class="text-2xl font-bold text-white">DH Enterprises</div>
```
- Replace "DH Enterprises" with your desired company name
- The `text-2xl` class controls size (options: text-sm, text-base, text-lg, text-2xl, text-3xl)

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Your Trusted South Florida Payment Processing Provider
</h1>
```
- Replace the headline text while keeping the HTML tags intact
- The classes `text-4xl`, `md:text-5xl`, and `lg:text-6xl` control responsive text sizing
- Don't remove the `class` attribute or its values

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-900 rounded-xl p-8">
    <div class="text-purple-500 mb-4">
        <i class="fas fa-shield-alt text-4xl"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Security</h3>
    <p class="text-gray-400">State-of-the-art encryption...</p>
</div>
```
To modify:
1. Change the icon by replacing `fa-shield-alt` with any [Font Awesome](https://fontawesome.com/icons) icon name
2. Update the heading text within the `<h3>` tags
3. Modify the description within the `<p>` tags

## Managing Links

### Navigation Menu Links
Located in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white">Benefits</a>
    <a href="#faq" class="text-gray-300 hover:text-white">FAQ</a>
    <a href="#contact" class="text-gray-300 hover:text-white">Contact</a>
</div>
```
To update:
1. The `href="#features"` links to page sections using IDs
2. Ensure section IDs match these links (e.g., `id="features"`)
3. For external links, replace with full URLs (e.g., `href="https://example.com"`)

### Call-to-Action Links
Currently points to a JotForm:
```html
<a href="https://form.jotform.com/250266352834053" class="inline-block bg-gradient-to-r...">
```
To update:
1. Replace the URL with your form or landing page
2. Keep the classes to maintain styling
3. Test the link before deploying

## Adding Privacy and Terms Pages

### Footer Links Setup
Located in the footer section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create new files:
   - Create `privacy.html` in the same directory
   - Create `terms.html` in the same directory

2. Update the links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section IDs match navigation href values
   - Section IDs should be exactly as written in the href (case-sensitive)
   - Example: `href="#features"` links to `id="features"`

2. **Styling Issues**
   - Don't remove classes from elements
   - Keep the `class` attribute even when modifying text
   - Maintain spacing in class names (they're separate classes)

3. **Responsive Design Problems**
   - Classes starting with `md:` or `lg:` control tablet and desktop styling
   - Don't remove these responsive classes
   - Test on different screen sizes after changes

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs) for styling options
- Verify Font Awesome icons at [fontawesome.com](https://fontawesome.com/icons)
- Use browser developer tools (F12) to inspect elements

Remember to always test your changes across different devices and browsers before deploying to production.