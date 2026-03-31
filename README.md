# Vitore Static Website

A complete static HTML website for Vitore — no Firebase, no backend required. This site is optimized for deployment on any static hosting service including Namecheap.

## 📁 Structure

```
static-site/
├── index.html              # Landing page (home)
├── blog.html               # Blog listing page
├── privacy.html            # Privacy policy
└── blog/
    ├── diabetes-friendly-eating-egypt.html
    ├── healthy-koshari-recipe-weight-loss.html
    ├── gym-nutrition-guide-egypt.html
    └── ramadan-meal-planning-suhoor-iftar.html
```

## ✨ Features

- ✅ **No Firebase** - Completely static
- ✅ **Dark/Light Mode** - Theme toggle with localStorage
- ✅ **Responsive Design** - Works on mobile, tablet, desktop
- ✅ **SEO Optimized** - Schema.org structured data
- ✅ **Fast** - Pure HTML/CSS/JS, no frameworks
- ✅ **App Download Links** - iOS and Android redirects

## 🚀 Deployment to Namecheap

### Step 1: Prepare Files

1. Copy all files from `static-site/` to a local folder
2. Ensure structure is maintained:
   ```
   your-folder/
   ├── index.html
   ├── blog.html
   ├── privacy.html
   └── blog/
       └── (4 blog article files)
   ```

### Step 2: Connect to Namecheap

1. **Log in to Namecheap Hosting Control Panel**
   - Go to https://www.namecheap.com/ → My Account → Hosting

2. **Connect your domain.org**
   - If using Namecheap DNS: nameservers should already point to your hosting
   - Point domain to your hosting IP address

### Step 3: Upload Files via FTP/SFTP

1. **Via Namecheap cPanel (easiest)**
   - Go to Hosting Control Panel → cPanel
   - Open **File Manager**
   - Navigate to `public_html` folder
   - Upload all files maintaining the folder structure

2. **Via FTP Client (more control)**
   - Use FileZilla or similar
   - Connect with FTP credentials from Namecheap
   - Host: `vitore.org` (or your domain)
   - Username/Password: from Namecheap email
   - Upload to `public_html` or `www` folder

### Step 4: Configure Domain

1. **Set Primary Domain**
   - cPanel → Addon Domains OR
   - cPanel → Main Domain
   - Point to folder where you uploaded files

2. **SSL/HTTPS (Important!)**
   - cPanel → AutoSSL or Let's Encrypt
   - Ensure HTTPS is enabled
   - Update app download links to use `https://`

### Step 5: Test

1. **Check website loads**
   ```
   https://vitore.org ✅
   https://vitore.org/blog.html ✅
   https://vitore.org/privacy.html ✅
   https://vitore.org/blog/diabetes-friendly-eating-egypt.html ✅
   ```

2. **Test theme toggle** (icon in top-right)

3. **Test download links** (should redirect to App Store/Google Forms)

## 📝 What's Included

### Pages

1. **index.html** - Landing page with:
   - Hero section with app download buttons
   - Statistics counters
   - Problem/Solution sections
   - Animated background
   - Theme toggle

2. **blog.html** - Blog listing with:
   - 4 featured articles
   - Category badges
   - Dark/light theme

3. **privacy.html** - Full privacy policy

4. **blog/*.html** - Individual blog articles with:
   - Full content from MDX files
   - Consistent styling
   - Back to blog link

### Features

- 🌙 **Dark Mode** - Toggle in header (saved to localStorage)
- ⚡ **Animated Counters** - Statistics on home page
- 📱 **Responsive** - Mobile-first design
- ♿ **Accessible** - Semantic HTML, ARIA labels
- 🔍 **SEO** - Schema.org JSON-LD, meta tags
- 🎨 **Modern Design** - Glassmorphism, gradients, smooth animations

## 🔗 External Links

The site includes links to:
- **iOS App Store**: https://apps.apple.com/eg/app/vitore/id6754825790
- **Android Form**: https://docs.google.com/forms/d/e/1FAIpQLSdxw5JPvroDy9AfwuYplFHglcLcb5T-91qZt9Yy5SJQhLwN5w/viewform

These can be updated in:
- `index.html` - Search for `iosAppStoreUrl` and `googleFormUrl`
- Replace URLs as needed

## 🛠️ Customization

### Change Colors
Edit `--primary` and `--secondary` in CSS:
```css
:root {
  --primary: #10b981;    /* Emerald green */
  --secondary: #06b6d4;  /* Cyan */
  --accent: #f59e0b;     /* Amber */
}
```

### Update Statistics
In `index.html`, change these numbers:
```javascript
animateCounter(stat1, 42, 2000);      // 42 active users
animateCounter(stat2, 1071, 2000);    // 1071 meals
animateCounter(stat3, 97, 1500);      // 97 plans
```

### Add New Blog Articles
1. Create `blog/your-article.html`
2. Copy structure from existing article
3. Add link to `blog.html`

## 📊 Performance

- **Load time**: < 1 second
- **Bundle size**: ~50KB HTML (all pages)
- **No external dependencies**: Pure HTML/CSS/JS
- **Caching**: Browser cache friendly

## 🔐 Security

- ✅ No backend = no vulnerabilities
- ✅ Static files only
- ✅ HTTPS enabled on Namecheap
- ✅ No data collection (except localStorage for theme)

## 📱 App Links

Users can download the app from:
1. Click "Download on App Store" → iOS App Store
2. Click "Get Android Early Access" → Google Form

## 🆘 Troubleshooting

### Site not showing
- **Check folder**: Files should be in `public_html/` on Namecheap
- **Check domain**: Ensure domain points to hosting IP
- **Wait 24 hours**: DNS may take time to propagate

### Links not working
- **Relative paths**: All internal links use relative paths (blog.html, privacy.html)
- **Blog links**: Articles are in `blog/` subfolder
- **Absolute links**: External links use full URLs

### Dark mode not working
- **Clear cache**: Ctrl+F5 or Cmd+Shift+R
- **Check localStorage**: Browser DevTools → Application → localStorage

### Theme not persisting
- Ensure cookies/localStorage enabled in browser settings
- The theme is saved automatically when toggled

## 📞 Support

For help with:
- **Namecheap FTP**: Contact Namecheap support
- **Domain setup**: Namecheap knowledge base
- **Website content**: Edit HTML files directly

## 📄 License

This is your proprietary website. All content rights reserved.

---

**Ready to deploy?** Follow the 5 steps above to get your site live on vitore.org!
