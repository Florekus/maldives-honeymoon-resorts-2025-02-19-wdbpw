# MaldivesMood Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the MaldivesMood landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the brand name and navigation menu:
```html
<div class="text-2xl font-bold text-blue-600">MaldivesMood</div>
```
To update the brand name:
1. Locate this div in the header section
2. Replace "MaldivesMood" with your desired text
3. Adjust text size using Tailwind classes if needed:
   - `text-xl` (smaller)
   - `text-2xl` (current size)
   - `text-3xl` (larger)

### Hero Section
The hero section includes the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white mb-6 leading-tight">
    Maldives Honeymoon Resorts
</h1>
<p class="text-xl md:text-2xl text-white/90 mb-8">
    Your Dream Holiday Awaits in Paradise
</p>
```
To modify:
1. Replace the text between the `<h1>` tags for the main headline
2. Update the paragraph text for the subheading
3. The responsive text sizes are:
   - Mobile: `text-4xl`
   - Tablet: `md:text-5xl`
   - Desktop: `lg:text-6xl`

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition duration-300">
    <i class="fas fa-hotel text-3xl text-blue-600 mb-4"></i>
    <h3 class="text-xl font-semibold mb-4">Luxury Accommodations</h3>
    <p class="text-gray-600">Experience world-class comfort in our premium overwater villas.</p>
</div>
```
To update:
1. Change the icon by replacing `fa-hotel` with any [Font Awesome icon](https://fontawesome.com/icons)
2. Modify the heading text between the `<h3>` tags
3. Update the description in the paragraph tags

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition duration-300">Contact</a>
</div>
```
To update:
1. For internal links (same page sections):
   - Keep the `#` prefix
   - Ensure the ID matches your section (e.g., `href="#features"` links to `<section id="features">`)
2. For external links:
   - Replace the `href` value with the full URL
   - Example: `href="https://example.com/page"`

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition duration-300">
        <i class="fab fa-facebook"></i>
    </a>
    <!-- Similar structure for Instagram and Twitter -->
</div>
```
To update:
1. Replace the `#` in `href="#"` with your social media profile URLs
2. Ensure all social links open in a new tab by adding `target="_blank"`

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:
```html
<!-- Add this before the copyright notice -->
<div class="border-t border-gray-800 mt-8 pt-8 text-center">
    <div class="flex justify-center space-x-6 mb-4">
        <a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">
            Privacy Policy
        </a>
        <a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">
            Terms of Service
        </a>
    </div>
</div>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Verify that section IDs match the href values
   - Check for typos in both the link and section ID
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Check that you've maintained the responsive classes:
     - `md:` prefix for tablet breakpoint
     - `lg:` prefix for desktop breakpoint
   - Don't remove the `container` class from main sections

3. **Icon Not Displaying**
   - Verify the Font Awesome CSS is properly loaded
   - Check that icon class names are correct
   - Ensure you're using the correct prefix (`fas`, `fab`, etc.)

### Need Help?
If you encounter issues:
1. Check the browser console for errors (F12)
2. Verify all files are in the correct directory
3. Ensure all external resources (Tailwind CSS, Font Awesome) are loading properly

Remember to test all changes across different screen sizes using your browser's developer tools (F12).