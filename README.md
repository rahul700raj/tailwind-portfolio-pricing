# 💼 Portfolio & Pricing Website - Tailwind CSS

A complete multi-section portfolio website with SaaS pricing table, dark mode toggle, and responsive design built with Tailwind CSS.

![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

## 🎯 Key Features

### Pricing Table
- **Gradient Cards**: `bg-gradient-to-r from-indigo-500 to-purple-500`
- **3 Pricing Tiers**: Basic, Pro (Featured), Enterprise
- **Hover Effects**: `hover:scale-105 transition-all`
- **Featured Plan**: Highlighted with gradient background

### Portfolio Sections
- **Hero Section**: Eye-catching introduction with gradient text
- **About**: Personal introduction and background
- **Skills**: Interactive skill cards with hover effects
- **Projects**: Featured work with gradient headers
- **Contact Form**: Fully styled contact form

### Dark Mode
- **Toggle Button**: Persistent theme switching
- **Dark Classes**: `dark:bg-gray-900 dark:text-white`
- **LocalStorage**: Saves user preference
- **Smooth Transitions**: `transition-colors duration-300`

### Additional Features
- **Sticky Navigation**: Fixed navbar with backdrop blur
- **Smooth Scrolling**: Anchor link navigation
- **Responsive Design**: Mobile-first approach
- **Gradient Animations**: Pulsing effects on hero section

## ⚙️ Tech Stack

- **HTML5**: Semantic markup
- **Tailwind CSS**: Utility-first styling (CDN)
- **JavaScript**: Dark mode toggle & smooth scroll
- **LocalStorage**: Theme persistence

## 📚 Learning Outcomes

✅ Apply custom sizes, gradients, and transitions  
✅ Build multi-section responsive pages  
✅ Implement theme switching with dark mode  
✅ Create pricing tables with featured plans  
✅ Master hover effects and animations  
✅ Build contact forms with Tailwind  
✅ Implement sticky navigation  
✅ Use gradient backgrounds effectively

## 🚀 Installation & Setup

### Clone Repository

```bash
git clone https://github.com/rahul700raj/tailwind-portfolio-pricing.git
cd tailwind-portfolio-pricing
```

### Run Locally

Simply open `index.html` in your browser or use a local server:

```bash
# Python
python -m http.server 8000

# Node.js
npx serve

# Or double-click index.html
```

## 📱 Sections Overview

### 1. Navigation Bar
- Fixed position with backdrop blur
- Smooth scroll navigation
- Dark mode toggle button
- Responsive menu (desktop)

### 2. Hero Section
```html
<h1 class="text-5xl md:text-6xl font-bold">
  Hi, I'm <span class="bg-gradient-to-r from-indigo-500 to-purple-500 
                      bg-clip-text text-transparent">Rahul Mishra</span>
</h1>
```

### 3. About Section
- Clean layout with centered content
- Alternating background colors
- Readable typography

### 4. Skills Section
- Grid layout: `grid-cols-2 md:grid-cols-3 lg:grid-cols-4`
- Hover scale effects
- Icon-based cards

### 5. Projects Section
- 3-column responsive grid
- Gradient project headers
- Tag system for technologies
- Call-to-action links

### 6. Pricing Section
```html
<!-- Featured Plan with Gradient -->
<div class="bg-gradient-to-r from-indigo-500 to-purple-500 
            rounded-2xl shadow-2xl p-8 
            transform scale-105 hover:scale-110">
  <!-- Pricing content -->
</div>
```

**Features:**
- 3 pricing tiers
- Featured plan with gradient
- Checkmark icons for features
- Different CTA buttons per plan

### 7. Contact Form
- Styled input fields
- Focus states with ring
- Gradient submit button
- Dark mode support

### 8. Footer
- Social media links
- Copyright information
- Consistent styling

## 🎨 Tailwind Utilities Used

### Gradients
```html
bg-gradient-to-r from-indigo-500 to-purple-500
bg-gradient-to-br from-blue-500 to-cyan-500
bg-clip-text text-transparent
```

### Dark Mode
```html
dark:bg-gray-900 dark:text-white
dark:bg-gray-800 dark:border-gray-700
```

### Hover Effects
```html
hover:scale-105 transition-all
hover:shadow-xl transition-shadow
hover:bg-indigo-500 hover:text-white
```

### Responsive Design
```html
grid-cols-1 md:grid-cols-2 lg:grid-cols-3
text-5xl md:text-6xl
flex-col md:flex-row
```

### Spacing & Layout
```html
py-20 px-4
space-y-4 gap-6
container mx-auto max-w-6xl
```

## 🌙 Dark Mode Implementation

### HTML Setup
```html
<html lang="en" class="scroll-smooth">
```

### Tailwind Config
```javascript
tailwind.config = {
    darkMode: 'class',
    theme: {
        extend: {
            colors: {
                primary: '#6366F1',
                secondary: '#8B5CF6',
            }
        }
    }
}
```

### JavaScript Toggle
```javascript
function toggleDarkMode() {
    const html = document.documentElement;
    const isDark = html.classList.contains('dark');
    
    if (isDark) {
        html.classList.remove('dark');
        localStorage.setItem('theme', 'light');
    } else {
        html.classList.add('dark');
        localStorage.setItem('theme', 'dark');
    }
}
```

## 📂 Project Structure

```
tailwind-portfolio-pricing/
│
├── index.html          # Main portfolio website
├── README.md          # Documentation
└── DEPLOYMENT.md      # Deployment guide
```

## 🎓 Advanced Concepts Covered

1. **Custom Tailwind Config**: Extended color palette
2. **Dark Mode**: Class-based theme switching
3. **LocalStorage**: Persistent user preferences
4. **Smooth Scrolling**: Enhanced UX
5. **Gradient Backgrounds**: Multiple gradient types
6. **Transform & Scale**: Hover animations
7. **Backdrop Blur**: Modern glass effect
8. **Responsive Grids**: Complex layouts

## 🌟 Customization Tips

### Change Color Scheme
```javascript
tailwind.config = {
    theme: {
        extend: {
            colors: {
                primary: '#YOUR_COLOR',
                secondary: '#YOUR_COLOR',
            }
        }
    }
}
```

### Modify Pricing Plans
Edit the pricing section HTML to add/remove features or change prices.

### Add More Sections
Follow the existing section structure and add new content blocks.

## 📖 Resources

- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Tailwind Dark Mode Guide](https://tailwindcss.com/docs/dark-mode)
- [Tailwind Gradient Generator](https://hypercolor.dev/)
- [Heroicons](https://heroicons.com/) - For additional icons

## 🚀 Deployment

### GitHub Pages
1. Go to repository settings
2. Navigate to Pages
3. Select `main` branch
4. Save and wait for deployment

**Live URL**: `https://rahul700raj.github.io/tailwind-portfolio-pricing/`

### Alternative Platforms
- **Netlify**: Drag & drop deployment
- **Vercel**: `vercel` command
- **Surge**: `surge` command

## 🤝 Contributing

Feel free to fork and submit pull requests!

## 📄 License

MIT License - Open source and free to use

## 👨‍💻 Author

**Rahul Mishra**  
Created as a learning project for Tailwind CSS

---

**Built with ❤️ using Tailwind CSS**