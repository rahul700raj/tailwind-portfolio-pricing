# 🚀 Deployment Guide

## GitHub Pages (Recommended)

### Step 1: Enable GitHub Pages

1. Visit: https://github.com/rahul700raj/tailwind-portfolio-pricing/settings/pages
2. Under **Source**, select:
   - Branch: `main`
   - Folder: `/ (root)`
3. Click **Save**

### Step 2: Access Your Live Site

After 1-2 minutes, your site will be live at:

**🌐 https://rahul700raj.github.io/tailwind-portfolio-pricing/**

---

## Alternative Deployment Options

### Option 1: Netlify (Instant)

#### Method A: Drag & Drop
1. Go to [Netlify Drop](https://app.netlify.com/drop)
2. Drag your project folder
3. Get instant live link

#### Method B: Git Integration
1. Sign up at [Netlify](https://netlify.com)
2. Click "New site from Git"
3. Connect your GitHub repository
4. Deploy automatically

### Option 2: Vercel

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
cd tailwind-portfolio-pricing
vercel
```

Follow the prompts and get your live URL instantly!

### Option 3: Surge

```bash
# Install Surge
npm i -g surge

# Deploy
cd tailwind-portfolio-pricing
surge
```

Choose a domain name and deploy!

### Option 4: GitHub Codespaces

1. Open repository in GitHub
2. Click "Code" → "Codespaces"
3. Create new codespace
4. Run: `python -m http.server 8000`
5. Open forwarded port

---

## Custom Domain Setup

### For GitHub Pages

1. Add `CNAME` file to repository:
```bash
echo "yourdomain.com" > CNAME
git add CNAME
git commit -m "Add custom domain"
git push
```

2. Configure DNS:
   - Add A records pointing to GitHub IPs:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153
   - Or add CNAME record: `rahul700raj.github.io`

3. Enable HTTPS in repository settings

---

## Environment-Specific Configuration

### Development
```bash
# Local server
python -m http.server 8000
# or
npx serve
```

### Production
- Minify HTML (optional)
- Optimize images
- Enable caching headers

---

## Continuous Deployment

### GitHub Actions (Auto-deploy)

Create `.github/workflows/deploy.yml`:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./
```

---

## Performance Optimization

### Before Deployment

1. **Optimize Images**: Use WebP format
2. **Minify HTML**: Remove whitespace
3. **Enable Caching**: Set cache headers
4. **CDN**: Tailwind CSS already on CDN

### After Deployment

1. Test on [PageSpeed Insights](https://pagespeed.web.dev/)
2. Check mobile responsiveness
3. Verify dark mode functionality
4. Test all navigation links

---

## Troubleshooting

### Site Not Loading
- Wait 2-3 minutes after enabling Pages
- Check branch is set to `main`
- Verify `index.html` is in root directory

### Dark Mode Not Working
- Clear browser cache
- Check localStorage permissions
- Verify JavaScript is enabled

### Styling Issues
- Ensure Tailwind CDN is loading
- Check browser console for errors
- Verify internet connection

---

## Quick Deploy Checklist

- [ ] Repository is public
- [ ] `index.html` is in root directory
- [ ] All links are relative (not absolute)
- [ ] Images are optimized
- [ ] Dark mode tested
- [ ] Mobile responsive verified
- [ ] GitHub Pages enabled
- [ ] Custom domain configured (optional)

---

## Support

For issues, open a GitHub issue or contact the maintainer.

**Happy Deploying! 🎉**