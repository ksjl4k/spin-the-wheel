# 🎡 Spin The Wheel

An interactive spinning wheel web app with customizable segments, built with vanilla JavaScript and optimized for mobile devices.

![Spin The Wheel](https://img.shields.io/badge/version-1.0.0-red)
![License](https://img.shields.io/badge/license-MIT-black)
![JavaScript](https://img.shields.io/badge/javascript-vanilla-yellow)
![Responsive](https://img.shields.io/badge/responsive-mobile%20optimized-brightgreen)

## ✨ Features

- **Interactive Wheel** - Smooth spinning animation with random outcomes
- **Customizable Segments** - Add, remove, and manage wheel segments in real-time
- **Mobile Optimized** - Fully responsive design for all device sizes
- **Modern Aesthetics** - Bold red and black theme with gold accents
- **Zero Dependencies** - Pure vanilla JavaScript, HTML, and CSS
- **High Performance** - Optimized canvas rendering with retina display support
- **Accessibility** - Semantic HTML and keyboard navigation support

## 🚀 Quick Start

### Local Development

**Option 1: Using Python (Built-in)**
```bash
python -m http.server 3000
```

**Option 2: Using Node.js**
```bash
npx http-server -p 3000
```

Then open [http://localhost:3000](http://localhost:3000) in your browser.

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/spin-the-wheel.git
cd spin-the-wheel
```

2. No dependencies to install - it's vanilla JavaScript!

3. Run locally:
```bash
npm run dev
# or
python -m http.server 3000
```

## 📋 Usage

### Adding Segments
1. Type your segment text in the "Add Segment" input field
2. Click the "Add" button or press Enter
3. The wheel automatically updates with the new segment

### Spinning the Wheel
1. Click the "SPIN NOW" button
2. Watch the wheel spin with a smooth animation
3. The result appears in gold text below the wheel

### Removing Segments
1. Find the segment in the "Current Segments" list
2. Click the "Remove" button
3. Wheel minimum: 2 segments

## 🛠 Deployment

### Deploy to Vercel (Recommended)

**Option 1: Using Vercel CLI**
```bash
npm i -g vercel
vercel
```

**Option 2: Using Git (Automatic Deployment)**
1. Push your code to GitHub
2. Go to [vercel.com](https://vercel.com)
3. Click "New Project"
4. Select your GitHub repository
5. Vercel will auto-detect the settings
6. Click "Deploy"

### Deploy to GitHub Pages

1. Push to GitHub:
```bash
git add .
git commit -m "Deploy Spin The Wheel"
git push origin main
```

2. In your GitHub repository:
   - Go to **Settings** → **Pages**
   - Set source to **main** branch
   - Your site will be live at `https://yourusername.github.io/spin-the-wheel`

### Deploy to Netlify

1. Go to [netlify.com](https://netlify.com)
2. Click "New site from Git"
3. Select your GitHub repository
4. Settings:
   - Build command: (leave empty)
   - Publish directory: `.`
5. Click "Deploy"

## 📁 File Structure

```
spin-the-wheel/
├── index.html          # Main application file
├── package.json        # Project metadata & scripts
├── vercel.json         # Vercel deployment config
├── .gitignore          # Git ignore rules
├── README.md           # This file
└── LICENSE             # MIT License
```

## 🎨 Customization

### Change Colors
Edit the CSS variables in the `<style>` section of `index.html`:

```css
:root {
    --primary-red: #dc143c;
    --dark-red: #8b0000;
    --black: #0a0a0a;
    --white: #ffffff;
    --accent-gold: #ffd700;
}
```

### Change Default Segments
Edit the `segments` array in the `<script>` section:

```javascript
let segments = ['Segment 1', 'Segment 2', 'Segment 3'];
```

### Change Spin Duration
Modify the spin animation duration:

```javascript
const spinDuration = 3 + Math.random() * 2; // Change 3-5 seconds
```

## 📊 Browser Support

- Chrome/Edge: ✅ Full support
- Firefox: ✅ Full support
- Safari: ✅ Full support
- Opera: ✅ Full support
- Mobile browsers: ✅ Full support (iOS Safari, Chrome Mobile, Firefox Mobile)

## ⚡ Performance

- **Load Time**: < 50ms
- **No external dependencies**: Zero npm packages
- **Optimized Canvas**: Retina-ready rendering
- **Mobile-Optimized**: Responsive design with touch support
- **File Size**: ~12KB (uncompressed)

## 🔒 Security

This is a client-side only application with no external API calls or data collection. All processing happens locally in your browser.

## 📝 License

MIT © 2024 - Feel free to use this project for personal and commercial purposes.

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 🐛 Bug Reports & Suggestions

Found a bug or have a suggestion? Please [open an issue](https://github.com/yourusername/spin-the-wheel/issues) on GitHub.

## 📞 Support

For questions or support, please reach out or open an issue on GitHub.

## 🙏 Acknowledgments

- Built with vanilla JavaScript, HTML, and CSS
- Inspired by classic spinning wheel games
- Optimized for modern web standards

---

**Made with ❤️ and lots of caffeine ☕**
