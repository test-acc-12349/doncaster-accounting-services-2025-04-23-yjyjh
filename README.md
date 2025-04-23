# Doncaster Accounting Services Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Doncaster Accounting Services landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<!-- Logo Text -->
<div class="text-2xl font-bold text-gray-800">DAS</div>
```
To update the logo text, simply replace "DAS" with your desired text.

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Doncaster accounting services
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">
    Where accounting expertise meets exceptional service
</p>
```
- Replace the h1 text to update your main headline
- Modify the paragraph text to change your subheading

### Tailwind CSS Classes Explained

#### Responsive Design Classes
The landing page uses Tailwind's responsive prefixes:
- `md:` - Applied at medium screens (768px and up)
- `lg:` - Applied at large screens (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Mobile: text-4xl (2.25rem)
- Tablet: text-5xl (3rem)
- Desktop: text-6xl (4rem)

#### Common Class Patterns

1. Spacing Classes:
   - `px-6`: Horizontal padding
   - `py-4`: Vertical padding
   - `mb-6`: Margin bottom
   - `space-x-8`: Horizontal spacing between children

2. Color Classes:
   - `text-gray-900`: Dark gray text
   - `bg-blue-600`: Blue background
   - `hover:bg-blue-700`: Darker blue on hover

3. Layout Classes:
   - `container`: Centers content
   - `mx-auto`: Auto margins horizontally
   - `grid`: Grid layout
   - `flex`: Flexbox layout

## Fixing Broken Links

### Navigation Menu Links
Current navigation links in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Identify the `href` attribute in each `<a>` tag
2. Replace `#services` with your desired destination
3. For internal links (same page), keep the `#` prefix
4. For external links, use the full URL: `https://example.com`

### Call-to-Action Links
Current placeholder links:
```html
<a href="https://theaccountants.com" class="inline-block bg-blue-600...">
```
Replace `https://theaccountants.com` with your actual consultation booking URL.

## Linking Privacy and Terms Pages

### Current Footer Structure
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

1. Create your policy pages:
   ```html
   <!-- privacy.html -->
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <title>Privacy Policy - Doncaster Accounting Services</title>
       <!-- Copy the same head section from index.html -->
   </head>
   <body>
       <!-- Add your privacy policy content here -->
   </body>
   </html>
   ```

2. Update the footer links:
   ```html
   <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
   <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
   ```

## Troubleshooting

### Common Issues

1. Broken Internal Links
   - Ensure section IDs match the href attributes
   - Check for typos in IDs
   - Verify that sections have the correct ID attribute

2. Responsive Design Issues
   - Test on different screen sizes
   - Verify media query prefixes (md:, lg:)
   - Check container widths and padding

3. Style Inconsistencies
   - Maintain consistent color classes
   - Use the same transition classes for similar elements
   - Keep spacing consistent using Tailwind's spacing scale

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML using [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always backup your files before making changes, and test thoroughly across different devices and browsers.