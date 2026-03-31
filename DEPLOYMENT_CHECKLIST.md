# 🚀 Vitore Static Website - Deployment Checklist

## ✅ Quick Start (5 minutes)

Use this checklist to deploy your free static website to Namecheap.

---

## Step 1: Prepare Files (2 minutes)
- [ ] All files are in `/static-site` folder
- [ ] Folder structure is confirmed:
  ```
  index.html
  blog.html
  privacy.html
  .htaccess
  README.md
  blog/
    ├── diabetes-friendly-eating-egypt.html
    ├── healthy-koshari-recipe-weight-loss.html
    ├── gym-nutrition-guide-egypt.html
    └── ramadan-meal-planning-suhoor-iftar.html
  ```

---

## Step 2: Login to Namecheap (1 minute)
- [ ] Go to https://www.namecheap.com/
- [ ] Click "Sign In" (top right)
- [ ] Enter your credentials
- [ ] Click "My Account" → "Hosting"

---

## Step 3: Upload Files - Choose One Method

### Method A: cPanel File Manager (Easiest)
- [ ] In Hosting Control Panel, click "Manage" next to your hosting
- [ ] Click "cPanel"
- [ ] Scroll down and click "File Manager"
- [ ] Navigate to `public_html` folder
- [ ] Click "Upload" button
- [ ] Select all files from `static-site/` folder
- [ ] Drag & drop or select files
- [ ] Wait for upload to complete ✅

### Method B: FTP Client (More Control)
- [ ] Download FileZilla (free) or WinSCP
- [ ] In Namecheap cPanel, find "FTP Accounts"
- [ ] Create new FTP account or use default
- [ ] Copy FTP credentials:
  - Host: `vitore.org` (your domain)
  - Username: (from FTP account)
  - Password: (from FTP account)
  - Port: 21
- [ ] Open FileZilla and connect
- [ ] Navigate to `public_html` folder on server
- [ ] Drag files from local folder to server
- [ ] Wait for transfer to complete ✅

---

## Step 4: Set Primary Domain (1 minute)
- [ ] In cPanel, find "Main Domain" or "Addon Domains"
- [ ] Ensure `vitore.org` points to the folder where you uploaded files
- [ ] If multiple domains, set vitore.org as primary
- [ ] Click "Save" ✅

---

## Step 5: Enable HTTPS (2 minutes)
- [ ] In cPanel, find "AutoSSL" or "Let's Encrypt"
- [ ] Enable SSL for vitore.org
- [ ] Wait 5-10 minutes for SSL to activate
- [ ] Verify: Visit https://vitore.org in browser ✅

---

## Step 6: Test Website (2 minutes)

Open in browser and test:
- [ ] https://vitore.org - Landing page loads ✅
- [ ] https://vitore.org/blog.html - Blog listing ✅
- [ ] https://vitore.org/privacy.html - Privacy page ✅
- [ ] https://vitore.org/blog/diabetes-friendly-eating-egypt.html - Blog article ✅
- [ ] Theme toggle (sun/moon icon) works ✅
- [ ] "Download on App Store" button works ✅
- [ ] "Get Android Early Access" button works ✅

---

## 🎉 You're Done!

Your website is now live at **https://vitore.org** with:
- ✅ Free hosting on Namecheap
- ✅ No Firebase/Backend needed
- ✅ Dark/Light mode
- ✅ 4 blog articles
- ✅ HTTPS enabled
- ✅ Mobile responsive

---

## 📝 Optional: Fine-Tuning

### Update App Download Links
If you need to change app store links:
1. Open `index.html` 
2. Find: `const iosAppStoreUrl = "https://apps.apple.com/..."`
3. Replace with your app URL
4. Save and re-upload

### Update Statistics
If you want to change user counts:
1. Open `index.html`
2. Find: `animateCounter(stat1, 42, 2000);`
3. Change `42` to your number
4. Save and re-upload

### Add More Blog Articles
1. Create new HTML file in `blog/` folder
2. Copy structure from existing article
3. Add link to `blog.html`
4. Upload files

---

## 🆘 Troubleshooting

### "File not found" or blank page
**Solution:**
- [ ] Check files are in `public_html` folder
- [ ] Verify domain points to correct folder
- [ ] Wait 24 hours for DNS to fully propagate
- [ ] Clear browser cache (Ctrl+F5)

### Links not working
**Solution:**
- [ ] Blog articles should be accessible at `/blog/article-name.html`
- [ ] Check .html extension is correct
- [ ] Verify folder structure matches above

### HTTPS not working
**Solution:**
- [ ] In cPanel, enable AutoSSL or Let's Encrypt
- [ ] Wait 5-10 minutes for certificate activation
- [ ] May need to clear browser cache

### Namecheap FTP Issues
**Solution:**
- [ ] Contact Namecheap support - they respond quickly
- [ ] Provide: domain name, hosting account email
- [ ] Use their "Managed Hosting" → "Help" → "Contact Support"

---

## 📞 Quick Links

- **Namecheap Hosting:** https://www.namecheap.com/hosting/
- **Namecheap Support:** https://www.namecheap.com/support/
- **Domain Settings:** https://www.namecheap.com/myaccount/
- **cPanel Docs:** https://cpanel.net/

---

**Total time:** 10-15 minutes  
**Cost:** FREE (included with Namecheap domain registration)  
**Result:** A fast, modern website with no backend needed! 🚀
