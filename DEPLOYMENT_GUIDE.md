# Deployment Guide

How to publish your website online.

---

## Option 1: GitHub Pages (Free & Easy)

### Step 1: Create GitHub Repository
1. Go to [github.com](https://github.com)
2. Click "New repository"
3. Name it: `techandmore-website`
4. Click "Create repository"

### Step 2: Upload Files
1. Click "uploading an existing file"
2. Drag ALL files from `techandmore-landing` folder
3. Click "Commit changes"

### Step 3: Enable GitHub Pages
1. Go to repository Settings
2. Scroll to "Pages" section
3. Source: Select "main" branch
4. Click "Save"
5. Your site will be live at: `yourusername.github.io/techandmore-website`

### Step 4: Custom Domain (Optional)
1. In Pages settings, add: `www.techandmore.co.uk`
2. Update DNS records at your domain registrar:
   - Type: `CNAME`
   - Name: `www`
   - Value: `yourusername.github.io`

---

## Option 2: Netlify (Free, Fastest)

### Step 1: Create Account
1. Go to [netlify.com](https://netlify.com)
2. Sign up (free)

### Step 2: Deploy
1. Click "Add new site" → "Deploy manually"
2. Drag the entire `techandmore-landing` folder
3. Wait 30 seconds
4. Your site is live!

### Step 3: Custom Domain
1. Go to "Domain settings"
2. Click "Add custom domain"
3. Enter: `www.techandmore.co.uk`
4. Follow DNS instructions

**Netlify URL**: `your-site-name.netlify.app`

---

## Option 3: Web Hosting (Traditional)

### Requirements
- Web hosting account (e.g., Hostinger, Bluehost, SiteGround)
- FTP client (e.g., FileZilla)

### Step 1: Get Hosting
1. Purchase hosting plan
2. Get FTP credentials (host, username, password)

### Step 2: Upload Files
1. Open FileZilla (or your FTP client)
2. Connect using your credentials
3. Navigate to `public_html` or `www` folder
4. Upload ALL files from `techandmore-landing`

### Step 3: Point Domain
1. Go to your domain registrar
2. Update DNS A record to point to hosting IP
3. Wait 24-48 hours for propagation

**Your site**: `www.techandmore.co.uk`

---

## Before Deploying - Checklist

### ✅ Content Check
- [ ] All text is correct
- [ ] All images are uploaded
- [ ] Email address is correct: `ltd.techandmore@gmail.com`
- [ ] Phone number is correct: `+44 7868 362602`
- [ ] Company info is accurate

### ✅ Technical Check
- [ ] All links work (test internal navigation)
- [ ] All images load (check `images/` folder)
- [ ] Contact form works
- [ ] Mobile responsive (test in browser dev tools)
- [ ] Cookie popup appears

### ✅ Files Check
- [ ] All HTML files present (7 files)
- [ ] `style.css` present
- [ ] `script.js` present
- [ ] `images/` folder with all GIFs

---

## Testing Your Deployed Site

### 1. Test All Pages
- Homepage loads correctly
- All 4 service pages load
- Privacy and Terms pages load
- E-commerce page loads

### 2. Test Navigation
- Logo clicks return to homepage
- Service cards link to correct pages
- Footer links work
- Navbar links work

### 3. Test Responsive
- Open on mobile phone
- Test on tablet
- Try different browsers

### 4. Test Contact Form
- Try submitting form
- Check email opens correctly

---

## Updating Your Live Site

### GitHub Pages:
1. Edit files locally
2. Upload to GitHub repository
3. Changes appear in 2-5 minutes

### Netlify:
1. Edit files locally
2. Drag updated files to Netlify
3. Changes appear instantly

### Web Hosting:
1. Edit files locally
2. Re-upload via FTP
3. Refresh browser to see changes

---

## Custom Domain Setup

### For `www.techandmore.co.uk`

**DNS Records to Add**:

**GitHub Pages**:
```
Type: CNAME
Name: www
Value: yourusername.github.io
```

**Netlify**:
```
Type: CNAME
Name: www
Value: your-site.netlify.app
```

**Web Hosting**:
```
Type: A
Name: @
Value: [Your hosting IP address]
```

---

## SSL Certificate (HTTPS)

### GitHub Pages:
- Automatic HTTPS
- Enable "Enforce HTTPS" in settings

### Netlify:
- Automatic HTTPS (Let's Encrypt)
- Enabled by default

### Web Hosting:
- Use hosting control panel
- Enable SSL/TLS certificate
- Most hosts offer free Let's Encrypt

---

## Performance Optimization

### Before Deploying:

1. **Optimize Images**
   - Compress GIFs (use ezgif.com)
   - Resize to appropriate dimensions
   - Use WebP format where possible

2. **Minify Files** (Optional)
   - CSS minifier: [cssminifier.com](https://cssminifier.com)
   - JS minifier: [javascript-minifier.com](https://javascript-minifier.com)

3. **Enable Caching**
   - Add to hosting `.htaccess` file
   - Or use Netlify's automatic caching

---

## Troubleshooting

### Site Not Loading?
- Check all files uploaded
- Verify DNS settings
- Wait for DNS propagation (up to 48 hours)

### Images Not Showing?
- Check `images/` folder uploaded
- Verify file names match exactly (case-sensitive)
- Check file paths in HTML

### Styling Looks Wrong?
- Ensure `style.css` uploaded
- Clear browser cache
- Check CSS file permissions

---

## Quick Deployment Comparison

| Method | Cost | Speed | Difficulty | SSL |
|--------|------|-------|------------|-----|
| GitHub Pages | Free | Medium | Easy | Auto |
| Netlify | Free | Fast | Very Easy | Auto |
| Web Hosting | £3-10/mo | Medium | Medium | Manual |

**Recommendation**: Start with **Netlify** for instant deployment, then move to custom hosting if needed.

---

**Need help?** Contact: ltd.techandmore@gmail.com



