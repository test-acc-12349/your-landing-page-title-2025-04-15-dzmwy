# Landing Page Maintenance Guide

This guide will help you maintain and customize your landing page. Follow these detailed instructions to make common updates while preserving the design and functionality.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Legal Pages](#adding-legal-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**: Find this line and replace "Logo" with your company name:
```html
<div class="text-xl font-bold text-gray-800">Logo</div>
```

2. **Navigation Menu Items**: Located in the header's `nav` element:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```
To modify menu items:
- Change the text between `<a>` tags
- Keep the `href` attributes matching your section IDs
- Maintain the existing classes for consistent styling

### Hero Section
The main headline and subtitle are in the first `section` after `<main>`:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight text-gray-900 mb-8">
    Create stunning landing pages in minutes
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Transform your ideas into professional, high-converting landing pages
</p>
```

To modify:
1. Replace the text between the tags
2. Keep the existing classes to maintain responsive design
3. Don't remove the `class` attributes

### Understanding Tailwind Classes
Common classes used in this template:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-[number]`: Adds margin bottom (e.g., `mb-8`, `mb-12`)
- `md:`: Applies styles on medium screens and up
- `hover:`: Applies styles on mouse hover

## Managing Links

### Navigation Links
All navigation links are currently internal anchors. To update:

1. **Internal Links** (current):
```html
<a href="#features">Features</a>
```

2. **External Links** (to modify):
```html
<a href="https://your-domain.com/features">Features</a>
```

### Call-to-Action Buttons
Update the "Get Started" buttons:

```html
<!-- Header CTA -->
<a href="https://sigmaseo.io" class="hidden md:inline-flex items-center px-6 py-2 bg-blue-600">
    Get Started
</a>

<!-- Hero CTA -->
<a href="https://sigmaseo.io" class="inline-flex items-center px-8 py-4">
    Start Creating Now
</a>
```

Replace `https://sigmaseo.io` with your desired URL.

### Footer Links
The footer contains multiple link sections. Update them like this:

```html
<ul class="space-y-2">
    <li><a href="/about">About</a></li>
    <li><a href="/blog">Blog</a></li>
    <li><a href="/careers">Careers</a></li>
</ul>
```

Replace the `href` values with your actual page URLs.

## Adding Legal Pages

### Step 1: Update Footer Legal Links
Locate the legal section in the footer:

```html
<div>
    <h3 class="text-lg font-semibold text-white mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
        <li><a href="/cookies.html" class="hover:text-white transition-colors duration-300">Cookie Policy</a></li>
    </ul>
</div>
```

### Step 2: Create Legal Pages
1. Create new HTML files:
   - `privacy.html`
   - `terms.html`
   - `cookies.html`
2. Use the same header and footer as `index.html`
3. Add your legal content in the `<main>` section

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check that all `href` attributes start with `/`, `#`, or `https://`
   - Verify file names match exactly (case-sensitive)
   - Test all links after updating

2. **Styling Problems**
   - Don't remove existing Tailwind classes
   - Keep responsive classes (starting with `md:` or `lg:`)
   - Maintain the class order as shown in the original code

3. **Layout Issues**
   - Keep the existing container structure:
     ```html
     <div class="container mx-auto px-6">
         <!-- Your content here -->
     </div>
     ```
   - Don't remove structural classes like `grid`, `flex`, or their modifiers

### Getting Help
If you encounter issues:
1. Check the Tailwind CSS documentation
2. Verify all closing tags match opening tags
3. Maintain the existing spacing and indentation
4. Test the page on different screen sizes

Remember to always backup your files before making changes, and test thoroughly after updates.