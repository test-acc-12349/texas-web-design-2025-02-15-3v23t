# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Fixing and Managing Links](#fixing-and-managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. Change the logo text:
```html
<!-- Find this line in the header section -->
<div class="text-2xl font-bold text-gray-800">TWD</div>
```
Simply replace "TWD" with your desired text.

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Texas Web Design
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Best Websites In Texas
</p>
```

- To change text size: modify `text-4xl`, `text-5xl`, or `text-6xl`
- To adjust spacing: modify `mb-6` (margin-bottom) values
- Common sizes: 
  - xs, sm, base, lg, xl, 2xl, 3xl, 4xl, 5xl, 6xl

### Features and Benefits Sections
Each card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-server text-4xl"></i>
    </div>
    <h3 class="text-xl font-semibold text-gray-900 mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included...</p>
</div>
```

To modify:
1. Change icon: Replace `fa-server` with any [Font Awesome](https://fontawesome.com/icons) icon
2. Update title: Modify text in the `<h3>` tag
3. Update description: Modify text in the `<p>` tag

## Fixing and Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900">Contact</a>
</div>
```

To update:
1. Internal links (same page): Use `#section-id`
2. External links: Use full URL (e.g., `https://example.com`)
3. Local pages: Use relative paths (e.g., `about.html`)

### Call-to-Action Buttons
Located in hero and CTA sections:
```html
<a href="https://twd.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Get Started Today
</a>
```

Replace `https://twd.com` with your actual URL.

## Adding Privacy and Terms Pages

### Footer Link Setup
Current footer links structure:
```html
<div>
    <h4 class="text-lg font-semibold mb-6">Legal</h4>
    <ul class="space-y-4 text-gray-400">
        <li><a href="#" class="hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:

1. Create new files:
   - Create `privacy.html`
   - Create `terms.html`

2. Update footer links:
```html
<li><a href="privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check for typos in URLs
   - Ensure file names match exactly
   - Verify file locations in your directory

2. **Styling Problems**
   - Check Tailwind CSS classes for typos
   - Verify class names in [Tailwind documentation](https://tailwindcss.com/docs)
   - Ensure responsive classes (md:, lg:) are correctly ordered

3. **Icons Not Showing**
   - Verify Font Awesome CDN link is present in `<head>`
   - Check icon class names against Font Awesome documentation
   - Ensure internet connection for CDN access

### Best Practices

1. Always test links after updating
2. Maintain consistent spacing using Tailwind's spacing classes
3. Keep backup copies before making major changes
4. Test on multiple devices using responsive design tools

Need more help? Contact support at admin@twd.com

---

Remember to replace all placeholder content (including email addresses and URLs) with your actual information before deploying the site.