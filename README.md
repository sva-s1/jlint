# JLint - JSON Validator & Formatter

[![Netlify Status](https://img.shields.io/netlify/d9639eee-a57b-4fb3-9a73-16e373dca637?style=for-the-badge&logo=netlify&logoColor=white)](https://app.netlify.com/projects/jlint/deploys)
[![GitHub stars](https://img.shields.io/github/stars/sva-s1/jlint?style=for-the-badge&logo=github&color=yellow)](https://github.com/sva-s1/jlint/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/sva-s1/jlint?style=for-the-badge&logo=github&color=blue)](https://github.com/sva-s1/jlint/network)
[![License](https://img.shields.io/badge/license-MIT-green.svg?style=for-the-badge)](LICENSE)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Astro](https://img.shields.io/badge/Astro-FF5D01?style=for-the-badge&logo=astro&logoColor=white)](https://astro.build/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Catppuccin](https://img.shields.io/badge/theme-Catppuccin-pink?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTEyIDJMMTMuMDkgOC4yNkwyMCAxMkwxMy4wOSAxNS43NEwxMiAyMkwxMC45MSAxNS43NEw0IDEyTDEwLjkxIDguMjZMMTIgMloiIGZpbGw9IndoaXRlIi8+Cjwvc3ZnPgo=)](https://catppuccin.com/)

A lightweight, client-side JSON validation and formatting tool built with Astro, TypeScript, and Tailwind CSS. Features beautiful Catppuccin theming (Mocha/Latte), syntax highlighting, compress/prettify toggle, and responsive design. Inspired by jsonlint.com but with modern styling and enhanced UX.

## ✨ Features

- **Client-side processing** - No data leaves your browser
- **Beautiful Catppuccin theming** - Toggle between Mocha (dark) and Latte (light) themes
- **Syntax highlighting** - Color-coded JSON output for better readability
- **Line numbers** - Visual line numbers in the input area for easy error tracking
- **Compress/Prettify toggle** - Switch between formatted and minified JSON
- **Copy to clipboard** - One-click copying of formatted output
- **Responsive design** - Works on desktop and mobile
- **Real-time validation** - Instant feedback on JSON validity
- **Modern UX** - Clean, intuitive interface

## 🚀 Getting Started

### Prerequisites

- Node.js 18+ and npm

### Installation

1. Clone the repository:

```bash
git clone https://github.com/sva-s1/jlint.git
cd jlint
```

2. Install dependencies:

```bash
npm install
```

3. Copy the example environment file:

```bash
cp .env.example .env
```

(The default values work out of the box, but you can customize them if needed)

4. Start the development server:

```bash
npm run dev
```

5. Open [http://localhost:4321](http://localhost:4321) in your browser

## 📖 How to Use

1. **Paste your JSON** - Copy and paste your JSON data into the left input area
2. **Validate & Format** - Click the "Validate & Format" button to check syntax and prettify
3. **Toggle compression** - Use the "Compress" button to minify or "Prettify" to format with indentation
4. **Copy results** - Click the "Copy" button to copy the formatted JSON to your clipboard
5. **Switch themes** - Use the toggle in the top-right corner to switch between light and dark themes
6. **Clear workspace** - Click "Clear" to reset both input and output areas

### Features in Detail

- **Real-time validation**: Get instant feedback if your JSON has syntax errors
- **Syntax highlighting**: Keys, strings, numbers, booleans, and null values are color-coded
- **Line numbers**: Visual line numbers with synchronized scrolling help locate errors quickly
- **Error reporting**: Clear error messages with line and column information, word-wrapped for full visibility
- **Theme persistence**: Your preferred theme is saved and restored on future visits
- **Privacy-focused**: All processing happens in your browser - no data is sent to any server

## 🛠️ Development

### Commands

| Command           | Action                                       |
| :---------------- | :------------------------------------------- |
| `npm install`     | Installs dependencies                        |
| `npm run dev`     | Starts local dev server at `localhost:4321`  |
| `npm run build`   | Build your production site to `./dist/`      |
| `npm run preview` | Preview your build locally, before deploying |

### Project Structure

```text
/
├── .env                     # Environment configuration
├── .env.example             # Environment template
├── README.md                # Project documentation
├── astro.config.mjs         # Astro configuration
├── package-lock.json        # Dependency lock file
├── package.json             # Project dependencies and scripts
├── tailwind.config.mjs      # Tailwind CSS configuration
├── tsconfig.json            # TypeScript configuration
├── public/
│   └── favicon.svg          # Site favicon
└── src/
    ├── pages/
    │   └── index.astro      # Main application page
    └── styles/
        └── global.css       # Catppuccin theme styles
```

## 🎨 Theming

JLint uses the beautiful [Catppuccin](https://catppuccin.com) color palette with two variants:

- **Mocha** - Dark theme with warm, cozy colors
- **Latte** - Light theme with soft, creamy tones

The theme toggle is located in the top-right corner and remembers your preference.

## 🔧 Configuration

Environment variables can be configured in `.env`:

### Core Site Configuration
- `JLINT_SITE_NAME` - Application name (displayed in footer)
- `JLINT_SITE_AUTHOR` - Author name
- `JLINT_SITE_AUTHOR_URL` - Author website/profile URL
- `REFERRER` - Organization/entity name (e.g., "A DataDocs Tool")
- `REFERRER_URL` - Organization website URL

### External References
- `JSONLINT_URL` - Original jsonlint.com URL for attribution
- `CATPPUCCIN_URL` - Catppuccin theme URL for credits
- `NETLIFY_URL` - Netlify hosting URL for credits

### Additional Site Info (Currently Unused)
- `JLINT_SITE_URL` - Production URL (not implemented yet)
- `JLINT_SITE_DESCRIPTION` - Site description (not implemented yet)
- `JLINT_SITE_VERSION` - Application version (not implemented yet)

## 🌐 Deployment

Build the project for production:

```bash
npm run build
```

The built site will be in the `./dist/` directory, ready to deploy to any static hosting service like Netlify, Vercel, or GitHub Pages.

## 🎯 Inspiration

- **[jsonlint.com](https://jsonlint.com)** - The original JSON validation tool
- **[Catppuccin](https://catppuccin.com)** - Beautiful color palette
- **[Font Awesome](https://fontawesome.com/)** - Icons

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

---

## 🗺️ Roadmap

### v1.1.0 - Enhanced Features

- [x] **Line numbers** - Visual line numbers in input area with synchronized scrolling
- [ ] GitHub icon in top-right corner linking to project repository
- [ ] "Edit this page" or "Contribute to this project" widget/button
- [ ] Dynamic icon/favicon that changes based on validation state or theme
- [ ] GitHub Actions workflow for automated Lighthouse performance testing
- [ ] JSON schema validation
- [ ] Import/export functionality for JSON files
- [ ] Keyboard shortcuts (Ctrl+Enter to validate, Ctrl+C to copy)
- [ ] Multiple format support (YAML, XML conversion)
- [ ] JSON path explorer

### v1.2.0 - Advanced Tools

- [ ] JSON diff/comparison tool
- [ ] Batch validation for multiple JSON objects
- [ ] Custom validation rules
- [ ] JSON minification statistics
- [ ] History of validated JSONs (local storage)

### v1.3.0 - Developer Experience

- [ ] API for programmatic validation
- [ ] Browser extension
- [ ] CLI version
- [ ] Integration with popular IDEs
- [ ] Export formatted JSON as image

### Future Considerations

- [ ] Collaborative editing features
- [ ] Plugin system for custom validators
- [ ] Advanced syntax highlighting themes
- [ ] Performance optimizations for large JSON files
- [ ] Accessibility improvements

---

**Privacy**: All JSON processing happens client-side. No data is sent to any server.
