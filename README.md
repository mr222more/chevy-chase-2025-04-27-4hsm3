# Landing Page Maintenance Guide

This guide will help you maintain and customize the Chevy Chase shower glass landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. Company Name:
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-400 to-teal-400 bg-clip-text text-transparent">
    Chevy Chase  <!-- Change this text -->
</a>
```

2. Navigation Menu Items:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Update text here -->
    <a href="#benefits">Benefits</a>  <!-- Update text here -->
    <a href="#contact">Contact</a>    <!-- Update text here -->
</div>
```

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold leading-tight mb-8">
    Custom shower glass for luxury bathroom  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Transform your bathroom...  <!-- Subheadline -->
</p>
```

### Tailwind CSS Class Guide
Common classes used throughout:
- Text sizes: `text-xl`, `text-2xl`, `text-4xl`
- Colors: `text-gray-300`, `bg-gray-900`
- Spacing: `px-6`, `py-4`, `mb-8`
- Responsive prefixes: `md:`, `lg:`

To modify styling:
1. Find the element you want to change
2. Locate its class attribute
3. Add or modify Tailwind classes
4. Keep responsive classes (`md:`, `lg:`) to maintain mobile compatibility

Example:
```html
<!-- Original -->
<p class="text-xl text-gray-400">

<!-- Modified for larger, blue text -->
<p class="text-2xl text-blue-400">
```

## Managing Links

### Current Link Inventory
1. Navigation Menu:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
<a href="http://www.customeuroglass.com">Get Started</a>
```

2. Call-to-Action Buttons:
```html
<a href="http://www.customeuroglass.com">Explore Our Collection</a>
```

3. Contact Information:
```html
<a href="mailto:info@customeuroglass.com">info@customeuroglass.com</a>
```

### Updating Links
To update any link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the text between the tags

Example:
```html
<!-- Original -->
<a href="http://www.customeuroglass.com">Get Started</a>

<!-- Updated -->
<a href="http://www.yournewwebsite.com">Start Now</a>
```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer's Quick Links section:

```html
<div>
    <h3 class="text-xl font-bold mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
        <li><a href="#benefits" class="text-gray-400 hover:text-white transition-colors duration-300">Benefits</a></li>
        <li><a href="#contact" class="text-gray-400 hover:text-white transition-colors duration-300">Contact</a></li>
        <!-- Add these new lines -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Bottom Footer Addition
Alternatively, add a secondary footer section:
```html
<div class="border-t border-gray-800 mt-12 pt-8 text-center text-gray-400">
    <p>&copy; 2023 Chevy Chase. All rights reserved.</p>
    <!-- Add this new paragraph -->
    <p class="mt-4">
        <a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a>
        <span class="mx-2">|</span>
        <a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a>
    </p>
</div>
```

## Troubleshooting

Common Issues and Solutions:

1. Links Not Working
   - Check for correct `href` values
   - Ensure `#` links match section IDs
   - Verify file paths for privacy.html and terms.html

2. Styling Problems
   - Confirm Tailwind CSS is properly loaded
   - Check for typos in class names
   - Verify responsive classes are correctly ordered

3. Layout Issues
   - Maintain the container structure:
     ```html
     <div class="container mx-auto px-6">
         <!-- Content here -->
     </div>
     ```
   - Keep responsive classes intact
   - Don't remove structural classes like `grid` and `flex`

Remember to:
- Test all changes on multiple screen sizes
- Maintain consistent spacing using Tailwind classes
- Keep the gradient styling for headings
- Preserve the responsive design structure

Need more help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).