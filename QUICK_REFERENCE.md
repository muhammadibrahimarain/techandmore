# Quick Reference Guide

Fast reference for common changes and updates.

---

## Common Changes

### 1. Update Contact Information

**Phone Number**  
**Find in**: All HTML files  
**Search for**: `+44 7868 362602`  
**Replace with**: Your new number  

**Email Address**  
**Find in**: All HTML files  
**Search for**: `ltd.techandmore@gmail.com`  
**Replace with**: Your new email  

**Location**  
**Find in**: `index.html`  
**Search for**: `London, UK`  
**Replace with**: Your location  

---

### 2. Change Service Names

**Edit**: `index.html` (lines 100-175)

**Find service cards** and update:
```html
<h3 class="service-title">Data Solutions</h3>
<h3 class="service-title">AI Services</h3>
<h3 class="service-title">Marketing Services</h3>
<h3 class="service-title">E-commerce Services</h3>
```

---

### 3. Update Hero Title

**Edit**: `index.html` (line 60)

**Change**:
```html
<h1 class="hero-title">Transforming Ideas Into Reality</h1>
```

**To your text**:
```html
<h1 class="hero-title">Your New Tagline Here</h1>
```

---

### 4. Add/Remove Services

**Edit**: `index.html` (lines 99-175)

**To add a 5th service**, copy this template:
```html
<a href="new-service.html" class="service-card">
    <div class="service-icon">
        <i class="fas fa-icon-name"></i>
    </div>
    <h3 class="service-title">New Service</h3>
    <p class="service-description">
        Description of your service.
    </p>
    <ul class="service-features">
        <li><i class="fas fa-check"></i> Feature 1</li>
        <li><i class="fas fa-check"></i> Feature 2</li>
    </ul>
</a>
```

Then update `style.css` services grid:
```css
.services-grid {
    grid-template-columns: repeat(2, 1fr);  /* Keep 2 columns */
    /* Or change to 3 for 3 columns */
}
```

---

### 5. Change Colors

**Quick color change in `style.css`**:

**Black to Dark Grey**:
```css
/* Find line 185 */
.hero {
    background: #000000;  /* Change to #1a1a1a for dark grey */
}
```

**White Buttons to Colored**:
```css
/* Find line 229 */
.hero .btn-primary {
    background: #0066ff;  /* Blue button */
    border: 2px solid #0066ff;
}
```

---

### 6. Replace GIFs

**Homepage**: Edit `index.html` (line 75)
```html
<img src="images/gif4.gif">
<!-- Change to: -->
<img src="images/your-new-gif.gif">
```

**Service Pages**: Edit respective HTML file
- `data-solutions.html` → Change `datagif.gif`
- `ai-services.html` → Change `gifAI.gif`
- `marketing-services.html` → Change `marketing.gif`
- `ecommerce-services.html` → Change `ecommerce2.gif`

**Steps**:
1. Add new GIF to `images/` folder
2. Update HTML file with new filename
3. Refresh browser

---

### 7. Update Company Name

**Find in all files**: `TechAndMore Limited`  
**Replace with**: Your company name  

**Files to update**:
- `index.html`
- `privacy.html`
- `terms.html`
- All service page footers

---

### 8. Adjust Button Spacing

**Reduce space between buttons**:
```css
/* Find in style.css */
.hero-buttons {
    gap: var(--spacing-md);  /* Change to var(--spacing-sm) */
}
```

---

### 9. Change Font Sizes (Quick)

**Make everything bigger**:
```css
/* Multiply all font-sizes by 1.2 */
.hero-title {
    font-size: 4.2rem;  /* Was 3.5rem × 1.2 */
}
```

**Make everything smaller**:
```css
/* Multiply all font-sizes by 0.8 */
.hero-title {
    font-size: 2.8rem;  /* Was 3.5rem × 0.8 */
}
```

---

### 10. Update Social Media Links

**Edit**: `index.html` (lines 332-347)

**Find**:
```html
<a href="https://linkedin.com" target="_blank">
<a href="https://twitter.com" target="_blank">
<a href="https://facebook.com" target="_blank">
```

**Replace with your actual links**:
```html
<a href="https://linkedin.com/company/techandmore" target="_blank">
<a href="https://twitter.com/techandmore" target="_blank">
<a href="https://facebook.com/techandmore" target="_blank">
```

---

## File Locations Quick Reference

| What to Change | File | Approx Line |
|---------------|------|-------------|
| Hero title | `index.html` | 60 |
| Services | `index.html` | 100-175 |
| About text | `index.html` | 185-220 |
| Contact info | `index.html` | 230-290 |
| All colors | `style.css` | 11-55 (variables) |
| Hero styling | `style.css` | 176-249 |
| Button styling | `style.css` | 287-330 |
| Mobile responsive | `style.css` | 913+ |

---

## Search & Replace Tips

### To update across all files:

**Windows**: Use VS Code or Notepad++
1. Open folder in editor
2. Press `Ctrl+Shift+F` (Find in Files)
3. Type old text
4. Type new text
5. Click "Replace All"

**Common replacements**:
- `ltd.techandmore@gmail.com` → Your email
- `+44 7868 362602` → Your phone
- `TechAndMore Limited` → Your company name
- `London, UK` → Your location

---

## Icon Reference (Font Awesome)

**Change service icons**:

Common icons:
- Database: `fa-database`
- Brain/AI: `fa-brain`
- Marketing: `fa-bullhorn`
- Shopping: `fa-shopping-cart`
- Chart: `fa-chart-line`
- Cloud: `fa-cloud`
- Code: `fa-code`
- Rocket: `fa-rocket`

**Find more**: [fontawesome.com/icons](https://fontawesome.com/icons)

**Usage**:
```html
<i class="fas fa-icon-name"></i>
```

---

## Quick Fixes

### Logo Not Clickable?
Add `<a>` tag around logo spans in navbar.

### Buttons Not Visible?
Make sure they have white background or white borders on dark sections.

### Form Not Working?
Check email link in `script.js` (line 160).

### Mobile Menu Not Opening?
Check `script.js` is loaded at bottom of HTML.

---

**For detailed styling help, see `STYLING_GUIDE.md`**  
**For deployment, see `DEPLOYMENT_GUIDE.md`**


