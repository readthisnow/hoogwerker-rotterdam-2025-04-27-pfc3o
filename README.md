# Landing Page Maintenance Guide

This guide will help you maintain and customize the Hoogwerker Rotterdam landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Company Name/Logo**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">Hoogwerker Rotterdam</a>
```
- Replace "Hoogwerker Rotterdam" with your company name
- The `text-2xl` class controls size
- `text-blue-600` controls the blue color

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Voordelen</a>
    <!-- Add or modify menu items here -->
</div>
```
- Each menu item uses the same class structure
- `text-gray-600` is the default color
- `hover:text-blue-600` creates the blue hover effect

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-8">
    Hoogwerker Rotterdam <span class="text-blue-600">| Tijdelijk 10% Korting</span>
</h1>
```
- `text-4xl`, `md:text-5xl`, `lg:text-6xl` control responsive text sizing
- Use `<span>` tags to apply different colors to specific text
- The `mb-8` class adds margin bottom spacing

### Features Section
To modify feature cards:

```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <i class="fas fa-bolt text-4xl text-blue-600 mb-6"></i>
    <h3 class="text-xl font-bold mb-4">Snelle Levering</h3>
    <p class="text-gray-600">Binnen 2 uur op locatie in Rotterdam en omgeving</p>
</div>
```
- Change icons by updating the `fa-bolt` class to any [Font Awesome](https://fontawesome.com/icons) icon
- Modify text within the `<h3>` and `<p>` tags
- Keep the class structure intact for consistent styling

## Managing Links

### Navigation Links
Current internal links in the navigation:

```html
<a href="#features">Voordelen</a>
<a href="#benefits">Diensten</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. The `#` symbol indicates an internal page section
2. Ensure the href matches the corresponding section's ID
3. Example: `href="#features"` links to `<section id="features">`

### Call-to-Action Buttons
Currently pointing to an external site:

```html
<a href="https://hansschuiling.nl" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-full">
    Direct Reserveren
</a>
```
To update:
1. Replace `https://hansschuiling.nl` with your booking URL
2. Test the link thoroughly before deploying

## Adding Privacy and Terms Pages

### Footer Links Setup
Current placeholder links in the footer:

```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Algemene Voorwaarden</a></li>
</ul>
```

To link to new pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the links:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Algemene Voorwaarden</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Verify that section IDs match their href attributes exactly
- IDs are case-sensitive
- Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
- Don't remove `md:` or `lg:` prefixes from classes
- These control how elements appear on different screen sizes
- Example: `md:text-5xl` means "apply text-5xl on medium screens and up"

3. **Icon Not Showing**
- Ensure Font Awesome is properly loaded in the head section
- Check that icon class names are correct
- Example: `fa-bolt` should have the `fas` prefix: `fas fa-bolt`

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct directory
3. Ensure all HTML tags are properly closed
4. Test on multiple browsers and devices

Remember to always make a backup before making significant changes to your code.