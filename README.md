# EagleiO Landing Page Maintenance Guide

This guide will help you maintain and customize the EagleiO landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold text-white hover:text-purple-400">
    EagleiO  <!-- Change this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>  <!-- Change menu text here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold leading-tight mb-8">
    Soar Above Service Hassles with EagleiO  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Transform your service management...  <!-- Subheadline -->
</p>
```

### Tailwind CSS Classes Explained
Common classes used throughout:
- `text-4xl`: Large text size
- `md:text-6xl`: Larger text on medium screens
- `mb-8`: Margin bottom spacing
- `bg-purple-600`: Purple background color
- `hover:bg-purple-700`: Darker purple on hover
- `rounded-full`: Circular corners

To modify styles:
1. Find the element you want to change
2. Look up alternative Tailwind classes at [Tailwind CSS Documentation](https://tailwindcss.com/docs)
3. Replace or add classes within the `class=""` attribute

Example:
```html
<!-- Original button -->
<a href="#" class="px-6 py-2 bg-purple-600 hover:bg-purple-700 rounded-full">

<!-- Modified button (larger, different color) -->
<a href="#" class="px-8 py-3 bg-blue-600 hover:bg-blue-700 rounded-lg">
```

## Managing Links

### Current Link Structure
The page contains these link types:

1. **Navigation Links:**
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```

2. **Call-to-Action Links:**
```html
<a href="https://eagle360.app">Get Started</a>
```

### Updating Links
To update any link:

1. Locate the `<a>` tag
2. Modify the `href` attribute:
   - For internal sections: Use `#section-name`
   - For external pages: Use full URL `https://example.com`
   - For local pages: Use relative path `./page.html`

Example:
```html
<!-- Original -->
<a href="https://eagle360.app">Get Started</a>

<!-- Updated -->
<a href="https://new-domain.com/signup">Get Started</a>
```

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the legal section in the footer:

```html
<div class="space-y-4">
    <h4 class="text-lg font-semibold">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To link to new pages:

1. Create your privacy.html and terms.html files
2. Update the href attributes:

```html
<li><a href="./privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="./terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check for typos in href attributes
   - Verify file paths are correct
   - Ensure external URLs include `https://`

2. **Styling Problems**
   - Confirm Tailwind CSS is properly loaded
   - Check for missing or mistyped class names
   - Verify responsive classes use correct breakpoints (sm:, md:, lg:)

3. **Layout Issues**
   - Check container classes are present
   - Verify grid column settings
   - Ensure responsive classes are properly nested

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct directory
3. Test links in multiple browsers
4. Ensure all HTML tags are properly closed

Remember to always back up your files before making changes, and test your updates in multiple browsers to ensure consistency.