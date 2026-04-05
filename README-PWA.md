# 🃏 Penak PWA - Installation Guide

Your Penak Score Tracker is now a **Progressive Web App (PWA)**! Users can install it like a native app on their phones.

## 📦 What You Need

You now have these files:
1. **penak-pwa.html** - Main app (updated with PWA support)
2. **manifest.json** - App configuration
3. **service-worker.js** - Offline support & caching
4. **icon-192.png** - App icon (you need to create this)
5. **icon-512.png** - App icon (you need to create this)

---

## 🚀 Deployment Steps

### Step 1: Create App Icons
Follow instructions in `ICON-INSTRUCTIONS.md` to create:
- icon-192.png (192x192 pixels)
- icon-512.png (512x512 pixels)

### Step 2: Upload Files
Upload all files to your web hosting:

**Option A: GitHub Pages (FREE)**
1. Create GitHub account (github.com)
2. Create new repository
3. Upload all 5 files
4. Enable GitHub Pages in Settings
5. Your app URL: `https://yourusername.github.io/repository-name/`

**Option B: Netlify (FREE)**
1. Go to netlify.com
2. Drag & drop your folder
3. Done! You get a URL like: `https://your-app.netlify.app`

**Option C: Your Own Web Server**
Just upload all files to the same directory:
```
/public_html/penak/
  ├── index.html (rename penak-pwa.html to index.html)
  ├── manifest.json
  ├── service-worker.js
  ├── icon-192.png
  └── icon-512.png
```

### Step 3: Enable HTTPS
⚠️ **IMPORTANT:** PWA requires HTTPS!

- GitHub Pages: ✅ Auto-enabled
- Netlify: ✅ Auto-enabled
- Own server: Get free SSL from Let's Encrypt or Cloudflare

---

## 📱 How Users Install the App

### On Android (Chrome):
1. Open your website
2. After 5 seconds, see install banner
3. Click "نصب" (Install)
4. App appears on home screen!

**OR:**
1. Open website in Chrome
2. Menu (⋮) → "Add to Home screen"
3. Click "Add"

### On iPhone (Safari):
1. Open website in Safari
2. Tap Share button (⬆️)
3. Scroll down → "Add to Home Screen"
4. Tap "Add"

### On Desktop (Chrome/Edge):
1. Open website
2. Look for install icon (⊕) in address bar
3. Click "Install"

---

## ✨ PWA Features You Now Have

### 1. **Installable**
- Appears on home screen like native app
- No browser UI (looks like real app)
- Launches instantly

### 2. **Offline Support**
- Works without internet (cached data)
- Google Sheets data cached automatically
- Can play games offline, syncs later

### 3. **Fast Loading**
- Files cached on first visit
- Subsequent loads are instant
- Smooth animations

### 4. **Auto Updates**
- App checks for new version
- Prompts user to update
- Updates happen automatically

### 5. **Better UX**
- Full screen mode
- Native app feel
- No browser address bar

---

## 🧪 Testing Your PWA

### Test Locally:
1. Install a local web server:
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx http-server
   ```

2. Open: `http://localhost:8000`
3. Install the app from localhost

### Test Online:
1. Upload to GitHub Pages/Netlify
2. Open URL on your phone
3. Try installing the app

### Check PWA Score:
1. Go to: https://www.pwabuilder.com/
2. Enter your URL
3. See PWA score and recommendations

---

## 🔧 Customization

### Change App Colors:
Edit `manifest.json`:
```json
{
  "background_color": "#667eea",  ← Change this
  "theme_color": "#667eea"         ← And this
}
```

### Change App Name:
Edit `manifest.json`:
```json
{
  "name": "Your App Name",
  "short_name": "Short Name"
}
```

### Update Cache Version:
When you update the app, edit `service-worker.js`:
```javascript
const CACHE_NAME = 'penak-v2';  ← Increment version
```

---

## 🐛 Troubleshooting

### Install button doesn't appear:
- ✅ Check HTTPS is enabled
- ✅ Manifest.json is accessible
- ✅ Icons exist (192px and 512px)
- ✅ Service worker registered successfully

### App doesn't work offline:
- ✅ Service worker registered?
- ✅ Check browser console for errors
- ✅ Cache version updated?

### Changes not showing:
- ✅ Hard refresh: Ctrl+Shift+R (Desktop) or clear cache
- ✅ Uninstall and reinstall app
- ✅ Update cache version in service-worker.js

### Check Service Worker:
1. Open DevTools (F12)
2. Go to "Application" tab
3. Click "Service Workers"
4. Should show "activated and running"

---

## 📊 File Sizes

Total app size: ~70KB (very small!)
- HTML: ~68KB
- Manifest: ~0.5KB
- Service Worker: ~3KB
- Icons: ~10KB each (you create these)

**Total download for user:** ~90KB (first visit)
**Subsequent visits:** Instant (cached)

---

## 🎯 Next Steps

1. ✅ Create icons (see ICON-INSTRUCTIONS.md)
2. ✅ Upload all files to hosting
3. ✅ Test on your phone
4. ✅ Share URL with friends
5. ✅ Enjoy your PWA!

---

## 📱 Sharing Your App

Send users this message:
```
🃏 برنامه پینک

برای نصب:
1. باز کن: [YOUR-URL-HERE]
2. روی "نصب" کلیک کن
3. آماده!

کار با برنامه آسان‌تر از وب‌سایت است!
```

---

## 🆘 Need Help?

Common issues and solutions:
- **Icons not showing:** Check file names exactly match (icon-192.png)
- **Can't install:** Must use HTTPS
- **Offline not working:** Clear cache and reload
- **Updates not applying:** Increment cache version

---

## 🎉 Congratulations!

You now have a professional PWA that:
- ✅ Works offline
- ✅ Installs like a native app
- ✅ Loads instantly
- ✅ Updates automatically
- ✅ Looks professional
- ✅ Completely free!

Enjoy! 🚀
