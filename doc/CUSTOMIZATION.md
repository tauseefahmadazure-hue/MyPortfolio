# Portfolio Customization Guide

## Quick Start

1. Open `index.html` in your web browser
2. Edit the text directly in the HTML file
3. Save and refresh your browser to see changes

## Sections to Customize

### 1. Header & Navigation
**File:** index.html (lines 206-217)

Update the portfolio title:
```html
<h1>My Portfolio</h1>  <!-- Change this -->
```

Update navigation links to match your sections.

### 2. Hero Section
**File:** index.html (lines 219-226)

Change the welcome message:
```html
<h2>Welcome to My Portfolio</h2>  <!-- Your headline -->
<p class="subtitle">Creative Developer & Designer</p>  <!-- Your tagline -->
```

### 3. About Section
**File:** index.html (lines 228-251)

Replace the about text with your biography and key highlights.

### 4. Experience Section
**File:** index.html (lines 253-287)

Update with your actual work experience:
- Years/dates
- Job titles
- Company names
- Job descriptions

Format:
```html
<div class="experience-item">
    <div class="experience-dot"></div>
    <div class="experience-year">YYYY - YYYY</div>
    <div class="experience-title">Your Job Title</div>
    <div class="experience-company">Company Name</div>
    <div class="experience-description">Description...</div>
</div>
```

### 5. Featured Projects
**File:** index.html (lines 289-370)

For each project, update:
- Project title
- Project description
- Technologies used (tags)

Add project images:
```html
<div class="project-card-image" style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); background-image: url('path/to/image.jpg'); background-size: cover;">
```

### 6. Services Section
**File:** index.html (lines 372-413)

Update service descriptions with what you offer. Change emoji icons if desired.

### 7. Skills Section
**File:** index.html (lines 415-479)

Add/remove skill items and adjust proficiency bars:
```html
<div class="skill-item">
    <span class="skill-name">Your Skill</span>
    <div class="skill-level">
        <div class="skill-bar" style="width: 85%;"></div>  <!-- Adjust percentage -->
    </div>
</div>
```

### 8. Testimonials
**File:** index.html (lines 481-523)

Add client testimonials with:
- Star rating (1-5 stars)
- Quote
- Author name
- Position/company

### 9. Blog Section
**File:** index.html (lines 525-557)

Update article titles, dates, and excerpts. Add links to full articles.

### 10. Contact Section
**File:** index.html (lines 559-618)

Update contact information:
- Location
- Email address
- Phone number
- Social media links

The contact form automatically validates and provides feedback.

### 11. Footer
**File:** index.html (line 620)

Update copyright year and name.

## Color Customization

### Primary Colors
Search and replace in the `<style>` section:

- **Purple Primary:** `#667eea` → Your color
- **Purple Secondary:** `#764ba2` → Your color
- **Dark Color:** `#2c3e50` → Your color
- **Light Color:** `#f8f9fa` → Your color

### Example: Change to Blue Theme
Replace:
- `#667eea` with `#3498db` (blue)
- `#764ba2` with `#2980b9` (darker blue)

## Adding Images

### Project Images
```html
<div class="project-card-image" 
     style="background: url('images/project1.jpg') center/cover;">
    Project Title
</div>
```

### Team Photo
Add a new section:
```html
<section class="about-photo">
    <img src="images/profile.jpg" alt="Your Name" class="profile-image">
</section>
```

## Font Customization

Change the font family in the body style:
```css
body {
    font-family: 'Your Font Name', sans-serif;
}
```

Popular choices:
- `'Poppins', sans-serif`
- `'Roboto', sans-serif`
- `'Inter', sans-serif`
- `'Playfair Display', serif` (for elegant look)

To use Google Fonts, add to `<head>`:
```html
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
```

## Social Media Links

Update in the contact section:
```html
<a href="https://linkedin.com/in/yourprofile" target="_blank">LinkedIn</a>
<a href="https://github.com/yourprofile" target="_blank">GitHub</a>
<a href="https://twitter.com/yourprofile" target="_blank">Twitter</a>
```

## Contact Form Customization

The form automatically validates and shows success feedback. To integrate with an email service:

1. **Using Formspree:** Change form action:
```html
<form class="contact-form" action="https://formspree.io/f/your-form-id" method="POST">
```

2. **Using Netlify Forms:** Add `netlify` attribute:
```html
<form class="contact-form" name="contact" method="POST" netlify>
```

3. **Using EmailJS:** Add to JavaScript:
```javascript
emailjs.send("service_id", "template_id", form_params)
```

## Mobile Menu Customization

The hamburger menu automatically appears on screens smaller than 768px. To change this breakpoint, find in CSS:
```css
@media (max-width: 768px) {
```

Change `768px` to your preferred width.

## Animation Customization

### Scroll-to-Top Button
- Appears after scrolling 300px
- Change threshold in JavaScript: `if (window.pageYOffset > 300)`

### Scroll Animations
- Duration: 0.6s (change in CSS: `transition: opacity 0.6s ease`)
- Trigger: When 10% of element is visible (change in JavaScript: `threshold: 0.1`)

## Performance Tips

1. **Optimize Images**
   - Use tools like TinyPNG or ImageOptim
   - Maximum image width: 1200px
   - Save as WebP for better compression

2. **Minimize CSS & JS**
   - Use online minifiers before deployment
   - Remove unused code

3. **Lazy Loading Images**
   - Add `loading="lazy"` attribute to images

## Testing Checklist

- [ ] Test all navigation links
- [ ] Test contact form submission
- [ ] Test on mobile devices
- [ ] Test on different browsers
- [ ] Check all external links work
- [ ] Verify all social media links
- [ ] Test scroll-to-top button
- [ ] Test responsive design at different screen sizes

## Deployment

### GitHub Pages (Free)
1. Create a GitHub repository named `username.github.io`
2. Upload `index.html` to the repository
3. Visit `https://username.github.io`

### Netlify (Free)
1. Drag and drop your folder into Netlify
2. Get a live URL instantly

### Custom Domain
1. Purchase domain from registrar (GoDaddy, Namecheap, etc.)
2. Update DNS settings
3. Deploy your portfolio

## Common Issues & Solutions

### Mobile menu doesn't close
- Check JavaScript is enabled
- Ensure HTML IDs match JavaScript selectors

### Smooth scrolling not working
- Browser compatibility - use modern browser
- Check for JavaScript errors in console

### Images not displaying
- Verify image paths are correct
- Use relative paths: `images/photo.jpg`
- Check file permissions

### Form not submitting
- Enable third-party form service (Formspree, Netlify, etc.)
- Check browser console for errors

## Need Help?

1. Check the console (F12) for JavaScript errors
2. Validate HTML at https://validator.w3.org/
3. Test CSS at https://jigsaw.w3.org/css-validator/
4. Review the README.md file

---

**Happy Customizing! 🚀**
