# Styling Guide

Complete guide to customizing colors, fonts, and design elements.

---

## Quick Color Changes

### Open `style.css` and find the `:root` section (lines 11-55)

### Main Colors

```css
:root {
    /* Change these values to customize colors */
    
    /* Backgrounds */
    --bg-white: #ffffff;      /* White sections */
    --bg-dark: #000000;       /* Black sections */
    --bg-gray: #0d0d0d;       /* Dark grey boxes */
    
    /* Text Colors */
    --text-black: #000000;    /* Black text */
    --text-white: #ffffff;    /* White text */
    --text-gray: #999999;     /* Grey text */
    --text-light: #cccccc;    /* Light grey text */
}
```

---

## Common Customizations

### 1. Change Black Sections to Different Color

**Find** (around line 185):
```css
.hero {
    background: #000000;   /* Change this */
}
```

**Example**: Change to dark blue
```css
.hero {
    background: #001f3f;
}
```

---

### 2. Change Button Colors

**Hero buttons** (around line 229):
```css
.hero .btn-primary {
    background: #ffffff;  /* Button background */
    color: #000000;       /* Button text */
    border: 2px solid #ffffff;
}
```

**Example**: Change to blue buttons
```css
.hero .btn-primary {
    background: #0066ff;
    color: #ffffff;
    border: 2px solid #0066ff;
}
```

---

### 3. Change Font Sizes

**Hero title** (around line 200):
```css
.hero-title {
    font-size: 3.5rem;  /* Change this value */
}
```

**Common sizes**:
- Small: `2rem` (32px)
- Medium: `3rem` (48px)
- Large: `4rem` (64px)
- Extra Large: `5rem` (80px)

---

### 4. Change Spacing

**Between sections** (around line 36-40):
```css
:root {
    --spacing-sm: 1rem;   /* 16px */
    --spacing-md: 2rem;   /* 32px */
    --spacing-lg: 4rem;   /* 64px */
    --spacing-xl: 6rem;   /* 96px */
}
```

**To reduce all spacing**, multiply by 0.5:
```css
    --spacing-sm: 0.5rem;
    --spacing-md: 1rem;
    --spacing-lg: 2rem;
    --spacing-xl: 3rem;
```

---

### 5. Change Font Family

**Find** (line 62):
```css
body {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', ...
}
```

**Example**: Use a different Google Font
1. Go to [fonts.google.com](https://fonts.google.com)
2. Select a font (e.g., "Roboto")
3. Copy the `<link>` code
4. Add to `<head>` section in HTML files
5. Update CSS:
```css
body {
    font-family: 'Roboto', sans-serif;
}
```

---

## Section-Specific Styling

### Hero Section (Black Background, White Text)

**Location**: Lines 176-249 in `style.css`

```css
.hero {
    background: #000000;        /* Hero background */
}

.hero-title {
    font-size: 3.5rem;          /* Main title size */
    color: #ffffff;             /* Title color */
}

.hero-description {
    font-size: 1rem;            /* Description size */
    color: #e0e0e0;             /* Description color */
}
```

---

### Services Section (Black Background)

**Location**: Lines 355-458 in `style.css`

```css
.services {
    background: var(--bg-dark);  /* Services background */
}

.service-card {
    background: var(--bg-gray);  /* Card background */
    border: 1px solid var(--border-color);  /* Card border */
}

.service-title {
    color: var(--text-white);    /* Service title color */
}
```

---

### About Section (Black Background)

**Location**: Lines 460-520 in `style.css`

```css
.about {
    background: #000000;         /* About background */
}

.about-content .section-title {
    color: #ffffff;              /* About title color */
}

.about-text {
    color: #cccccc;              /* About text color */
}
```

---

### Contact Section (Black Background)

**Location**: Lines 532-660 in `style.css`

```css
.contact {
    background: var(--bg-dark);  /* Contact background */
}

.contact-form {
    background: var(--bg-gray);  /* Form background */
}
```

---

## Border and Shadow Changes

### Remove All Borders
Search for `border:` in `style.css` and change to:
```css
border: none;
```

### Remove All Shadows
Search for `box-shadow:` and change to:
```css
box-shadow: none;
```

### Add Rounded Corners
```css
border-radius: 10px;  /* Adjust value for more/less rounding */
```

---

## Responsive Design Breakpoints

### Tablet (768px and below)
**Location**: Lines 913-1012 in `style.css`
```css
@media (max-width: 768px) {
    .hero-title {
        font-size: 2.5rem;  /* Smaller on tablet */
    }
}
```

### Mobile (480px and below)
**Location**: Lines 1014-1028 in `style.css`
```css
@media (max-width: 480px) {
    .hero-title {
        font-size: 1.75rem;  /* Even smaller on mobile */
    }
}
```

---

## GIF/Image Customization

### Change GIFs

**Homepage** (`index.html`, line 75):
```html
<img src="images/gif4.gif">
```

**Service Pages**: Edit the respective HTML file
- Data: `images/datagif.gif`
- AI: `images/gifAI.gif`
- Marketing: `images/marketing.gif`
- E-commerce: `images/ecommerce2.gif`

### Change Image Size

In `style.css` (line 260-266):
```css
.hero-animation {
    max-width: 900px;  /* Change this to make larger/smaller */
}
```

---

## Quick Color Schemes

### Option 1: Blue Theme
```css
:root {
    --bg-dark: #001f3f;     /* Navy blue */
    --primary-color: #0066ff; /* Bright blue */
}
```

### Option 2: Purple Theme
```css
:root {
    --bg-dark: #1a0033;     /* Deep purple */
    --primary-color: #9933ff; /* Purple */
}
```

### Option 3: Green Theme
```css
:root {
    --bg-dark: #003311;     /* Dark green */
    --primary-color: #00cc66; /* Green */
}
```

---

## Tips

1. **Test changes**: Refresh browser (Ctrl+F5) to see changes
2. **One change at a time**: Easier to debug if something breaks
3. **Keep backups**: Copy `style.css` before major changes
4. **Browser cache**: Hard refresh (Ctrl+Shift+R) if changes don't appear

---

## Common Issues

### Changes Not Showing?
- Clear browser cache (Ctrl+F5)
- Check file is saved
- Check correct file is being edited

### Layout Broken?
- Check for missing semicolons in CSS
- Validate CSS syntax
- Revert last change

### Colors Look Wrong?
- Use hex color picker online
- Test colors on different screens
- Check contrast for readability

---

**For more help, see `QUICK_REFERENCE.md`**



