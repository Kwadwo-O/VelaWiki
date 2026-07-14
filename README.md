# VelaWiki

A lightweight Wikipedia client for **Xiaomi Redmi Watch 5** built with Vela Quick App framework. Search Wikipedia articles and explore related links directly on your smartwatch.

## ✨ Features

- 🔍 **Wikipedia Search** - Search for articles with up to 5 character queries
- 🔗 **Linked Articles** - View up to 15 articles linked within your search results
- ⏱️ **Live Time Display** - Current time shown on results page
- 📱 **Redmi Watch 5 Optimized** - 480×480px circular display support
- 🌙 **Dark Theme** - Eye-friendly dark interface perfect for wearables
- ⚡ **Lightweight** - Minimal API payloads optimized for smartwatch connectivity
- 📶 **Offline Error Handling** - Clear error messages and retry functionality

## 🎯 Getting Started

### Prerequisites
- Node.js 8.10+
- Git
- Xiaomi Redmi Watch 5 or Vela emulator

### Installation

```bash
# Clone the repository
git clone https://github.com/Kwadwo-O/VelaWiki.git
cd VelaWiki

# Install dependencies
npm install

# Start development server
npm run start
```

### Build & Release

```bash
# Build the project
npm run build

# Create release bundle
npm run release
```

### Code Linting

```bash
# Lint and fix all .ux and .js files
npm run lint
```

## 🏗️ Project Structure

```
VelaWiki/
├── src/
│   ├── app.ux                 # Global app state
│   ├── manifest.json          # App configuration
│   ├── pages/
│   │   ├── splash/            # Loading screen (5s countdown)
│   │   ├── search/            # Main search input page
│   │   ├── results/           # Search results & linked articles
│   │   └── settings/          # Settings page
│   ├── components/
│   │   └── InputMethod/       # QWERTY keyboard component
│   ├── common/                # Images & assets
│   └── i18n/                  # Internationalization
├── package.json               # Dependencies & scripts
└── README.md                  # This file
```

## 📖 Usage

### Search for Articles

1. **Splash Screen** - App launches with 5-second countdown (tap to skip)
2. **Search Page** - Enter up to 5 characters of a Wikipedia article title
3. **Results** - Browse search results, click any article to see linked pages
4. **Linked Articles** - View 15 related articles connected within the selected article
5. **Back Button** - Navigate between results and linked articles seamlessly

### Example Search Flow
```
"Einstein" → Browse results → Click "Albert Einstein" → View related articles like:
  • Physics
  • Relativity
  • Nobel Prize
  • Quantum Mechanics
```

## 🛠️ Development

### Pages Overview

| Page | Purpose | Features |
|------|---------|----------|
| **Splash** | App initialization | 5s countdown, skip on tap |
| **Search** | Input query | QWERTY keyboard (max 5 chars) |
| **Results** | Display Wikipedia content | Search results + linked articles |
| **Settings** | App configuration | Global keyboard type setting |

### Key APIs Used

- `@system.router` - Page navigation
- `@system.fetch` - Wikipedia API calls
- `@system.prompt` - Toast notifications
- `@system.vibrator` - Touch feedback
- `@system.storage` - Local data persistence

### Wikipedia API Integration

The app uses the **Wikipedia REST API**:
- **Search endpoint**: `http://en.wikipedia.org/w/api.php?action=query&generator=search`
- **Links endpoint**: `http://en.wikipedia.org/w/api.php?action=query&prop=links`

## 🐛 Troubleshooting

### Network Errors

**"Check WiFi & internet connection"**
- Ensure Redmi Watch 5 is connected to WiFi
- Check internet connectivity
- Tap "Retry" button to attempt again

### No Results Found

- Try a different search term
- Use shorter, simpler keywords
- Ensure Wikipedia has an article for your search

### Slow Performance

- The app is optimized for wearable connectivity
- First search may take 2-3 seconds
- Subsequent searches are faster due to caching

## 🚀 Technology Stack

- **Framework**: Vela Quick App (Xiaomi's framework)
- **Language**: JavaScript (ES5/ES6)
- **Styling**: CSS Flexbox
- **Build Tool**: aiot-toolkit
- **Linting**: ESLint + Prettier + Stylelint

## 📝 Code Standards

The project includes:
- ✅ ESLint configuration for code quality
- ✅ Prettier for consistent formatting
- ✅ Stylelint for CSS validation
- ✅ Husky git hooks for pre-commit checks

### Run Code Quality Checks

```bash
# Format & lint all code
npm run lint
```

## 🌐 Wikipedia Attribution

This app uses data from **Wikipedia**, the free online encyclopedia. 
- Data is provided under the Creative Commons Attribution-ShareAlike License
- Learn more: https://www.wikipedia.org/

## 📱 Device Support

- ✅ **Xiaomi Redmi Watch 5** (480×480px circular display)
- ✅ **Vela Emulator** (for development)
- Other Xiaomi smartwatches with Vela framework support

## 🔐 Privacy & Security

- No user data is stored locally
- All searches are sent to Wikipedia's public API
- HTTP protocol used for better smartwatch compatibility
- No tracking or analytics

## 📄 License

This project is open source. See LICENSE file for details.

## 🤝 Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📞 Support

For issues and feature requests, please use the [GitHub Issues](https://github.com/Kwadwo-O/VelaWiki/issues) page.

## 🔗 Resources

- [Vela Quick App Official Docs](https://iot.mi.com/vela/quickapp)
- [Wikipedia API Documentation](https://www.mediawiki.org/wiki/API)
- [Xiaomi IoT Developer Platform](https://iot.mi.com/)

---

**Built with ❤️ for Xiaomi Redmi Watch 5**

