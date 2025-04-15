# Landing Page Maintenance Guide
## For Computerbril.org

This guide will help you maintain and customize the Computerbril.org landing page. It's written for beginners and provides step-by-step instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the site logo and navigation menu. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold text-blue-600">Computerbril.org</a>
```
- Replace "Computerbril.org" with your desired text
- The `text-blue-600` class controls the blue color
- `text-2xl` controls the size

2. **Navigation Menu Items:**
```html
<div class="hidden lg:flex space-x-8">
    <a href="#voordelen" class="text-gray-600 hover:text-blue-600">Voordelen</a>
    <!-- Other menu items -->
</div>
```
- Replace text between `<a>` tags
- Keep the `href` attributes matching your section IDs
- The `hover:text-blue-600` class creates the blue hover effect

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Wat is beter: een Computerbril of Multifocale bril?
</h1>
```
- Update the heading text while maintaining the HTML structure
- Size classes explain the responsive behavior:
  - `text-4xl`: Default size
  - `sm:text-5xl`: Larger on small screens
  - `lg:text-6xl`: Largest on large screens

## Managing Links

### Internal Links
The page uses anchor links for navigation:

1. **Navigation Menu Links:**
```html
<a href="#voordelen">Voordelen</a>
<a href="#vergelijking">Vergelijking</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
- Ensure the `href` matches the `id` of the target section
- Example: `href="#voordelen"` links to `<section id="voordelen">`

### External Links
The page contains two types of external links:

1. **Main CTA Button:**
```html
<a href="https://computerbril.org" class="inline-flex items-center px-8 py-4">
    Ontdek meer
</a>
```
- Update the `href` to your desired URL
- Keep the class attributes to maintain styling

2. **Email Link in Footer:**
```html
<a href="mailto:info@computerbril.org">
    info@computerbril.org
</a>
```
- Update both the `href` and display text with your email address

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links in the footer:

1. **Add New Column:**
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12">
    <!-- Existing columns -->
    <div>
        <h3 class="text-xl font-semibold text-white mb-4">Legal</h3>
        <ul class="space-y-2">
            <li>
                <a href="/privacy.html" class="hover:text-white transition-colors duration-300">
                    Privacy Policy
                </a>
            </li>
            <li>
                <a href="/terms.html" class="hover:text-white transition-colors duration-300">
                    Terms of Service
                </a>
            </li>
        </ul>
    </div>
</div>
```

2. **Create Matching Files:**
- Create `privacy.html` and `terms.html` in your root directory
- Use the same header and footer as `index.html`
- Maintain consistent styling using Tailwind classes

## Troubleshooting

### Common Issues

1. **Broken Internal Links:**
- Check that section `id` attributes match navigation `href` values
- IDs are case-sensitive
- Remove any spaces in IDs

2. **Responsive Design Issues:**
- Don't remove `sm:`, `md:`, or `lg:` prefixes from classes
- These control how the page looks at different screen sizes
- Test on multiple devices or use browser dev tools

3. **Style Inconsistencies:**
- Keep color classes consistent (e.g., `text-blue-600`)
- Maintain spacing classes (e.g., `mb-4`, `py-24`)
- Use the same transition classes for interactive elements

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify HTML syntax at [W3C Validator](https://validator.w3.org/)
- Test all links before deploying changes

Remember to always backup your files before making changes, and test thoroughly on different devices and browsers.