# Landing Page Maintenance Guide
## For 101Headshots Corporate Photography Website

This guide provides detailed instructions for maintaining and customizing the 101Headshots landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company logo and navigation menu. To update:

1. **Company Name/Logo**
```html
<!-- Located in header section -->
<span class="text-2xl font-bold text-gray-900">101Headshots</span>
```
- Replace "101Headshots" with your company name
- Adjust text size by changing `text-2xl` to `text-3xl` for larger or `text-xl` for smaller

2. **Navigation Menu Items**
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#services" class="text-gray-600 hover:text-gray-900">Services</a>
    <!-- Additional menu items -->
</div>
```
- Change menu text by updating the text between `<a>` tags
- Modify spacing between items by adjusting `space-x-8`

### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    Shawnee, Kansas Corporate Headshot Photography Services
</h1>
```
- Update heading text between the `<h1>` tags
- Responsive text sizes are set using:
  - `text-4xl`: Mobile devices
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Services Cards
Each service card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8">
    <h3 class="text-xl font-semibold mb-4">Live Feedback</h3>
    <p class="text-gray-600">Instant review and adjustment...</p>
</div>
```
To modify:
1. Change card title between `<h3>` tags
2. Update description text in the `<p>` tag
3. Adjust padding by modifying `p-8`
4. Change shadow intensity using `shadow-lg`, `shadow-xl`, or `shadow-sm`

## Fixing Broken Links

### Current Link Structure
The page contains these types of links:

1. **Navigation Links**
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```
- These are internal page links (anchors)
- The `#` symbol indicates they link to page sections with matching IDs

2. **Booking Links**
```html
<a href="https://www.101headshots.com">Book Now</a>
```
- Replace the URL with your actual booking page link
- Maintain the `https://` prefix for external links

### Updating Links
To update any link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the link text between the tags

Example:
```html
<!-- Before -->
<a href="https://www.101headshots.com">Book Now</a>

<!-- After -->
<a href="https://www.yournewdomain.com/booking">Schedule Session</a>
```

## Linking Privacy and Terms Pages

### Footer Links Section
Located at the bottom of the page:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

### Adding Policy Links
1. Create your policy pages (privacy.html and terms.html)
2. Update the href attributes:
```html
<!-- Replace these placeholder links -->
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Ensure section IDs match exactly:
```html
<!-- Navigation link -->
<a href="#services">Services</a>

<!-- Matching section ID -->
<section id="services">
```

2. **Responsive Design Issues**
- Check responsive class prefixes:
  - `md:` for medium screens
  - `lg:` for large screens
- Example: `class="text-xl md:text-2xl lg:text-3xl"`

3. **Style Inconsistencies**
- Copy existing classes for consistency
- Example for buttons:
```html
class="inline-flex items-center justify-center px-6 py-3 border border-transparent rounded-md shadow-sm text-base font-medium text-white bg-blue-600 hover:bg-blue-700"
```

### Need Help?
- Verify all changes in a development environment first
- Test on multiple screen sizes
- Keep a backup of the original HTML file
- Use browser developer tools (F12) to inspect elements

Remember to test all changes thoroughly before pushing to production. When in doubt, refer back to this guide or consult with a web developer.