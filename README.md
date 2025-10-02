# Trello Markdown Descriptions

A browser extension that renders Trello card descriptions as proper markdown when not in edit mode, finally bringing the long-requested table support and other markdown features to Trello.

## 🎯 Problem Solved

This extension addresses a [highly requested feature](https://community.atlassian.com/forums/Trello-questions/Adding-a-Table-inside-Trello-Card-Description/qaq-p/775080) in the Trello community: the ability to render markdown tables and other markdown syntax directly in card descriptions. Users have been asking for this functionality for years!

## ✨ Features

- **Markdown Tables**: Finally use tables in your Trello card descriptions
- **Full Markdown Support**: Headers, lists, code blocks, links, images, and more
- **GitHub-flavored Markdown**: Supports strikethrough, task lists, and other GFM features
- **Smart Detection**: Only processes descriptions that contain markdown syntax
- **Edit Mode Preservation**: Automatically switches back to plain text when editing
- **Non-intrusive**: Works seamlessly with Trello's existing interface

## 🛠 Supported Markdown Features

- **Headers** (`# H1`, `## H2`, etc.)
- **Tables** (`| Column 1 | Column 2 |`)
- **Lists** (ordered and unordered)
- **Code blocks** and `inline code`
- **Links** (`[text](url)`)
- **Images** (`![alt](url)`)
- **Bold** (`**text**`) and *italic* (`*text*`)
- **Strikethrough** (`~~text~~`)
- **Blockquotes** (`> quote`)
- **Task lists** (`- [ ] todo`)
- **Horizontal rules** (`---`)

## 📦 Installation

### Chrome Web Store

[Install from Chrome Web Store](https://chrome.google.com/webstore/detail/trello-markdown-renderer)

### Firefox Add-ons

[Install from Firefox Add-ons](https://addons.mozilla.org/firefox/addon/trello-markdown-renderer)

### Microsoft Edge Add-ons

[Install from Edge Add-ons](https://microsoftedge.microsoft.com/addons/detail/trello-markdown-renderer)

### Safari Extension (macOS)

[Download from Mac App Store](https://apps.apple.com/app/trello-markdown-renderer)

## 🚀 Usage

1. Install the extension for your browser
2. Open any Trello card with a description
3. Write your description using markdown syntax:

   ```markdown
   # Project Overview
   
   ## Tasks

   | Task | Status | Assignee |
   |------|--------|----------|
   | Design | ✅ Done | Alice |
   | Development | 🔄 In Progress | Bob |
   | Testing | ⏳ Pending | Carol |
   
   ## Notes
   - **Important**: Remember to update the documentation
   - Use `git commit -m "message"` for commits
   - > Don't forget to run tests before deploying
   ```

4. The extension automatically renders the markdown when you're not editing

## 🏗 Development

### Prerequisites

- Node.js 18+
- npm or yarn

### Setup

```bash
git clone https://github.com/pke/trello-markdown-descriptions.git
cd trello-markdown-descriptions
yarn install
```

### Build

```bash
# Build for all browsers
yarn build

# Build and package for distribution
yarn package:all
```

### Manual Installation for Development

#### Chrome/Edge

1. Run npm run build
2. Open chrome://extensions/
3. Enable "Developer mode"
4. Click "Load unpacked" and select build/chrome/

#### Firefox

1. Run npm run build
2. Open about:debugging
3. Click "This Firefox"
4. Click "Load Temporary Add-on"
5. Select any file in build/firefox/

### 🚢 Deployment

#### Automated Deployment

The extension automatically deploys to all stores when you create a release on GitHub.

### Manual Deployment

```bash
# Deploy to specific store
npm run deploy:chrome
npm run deploy:firefox
npm run deploy:edge
npm run deploy:safari

# Deploy to all stores
npm run deploy:all
```

### Environment Variables

Create a `.env` file with your store credentials:

```env
# Chrome Web Store
CHROME_CLIENT_ID=your_client_id
CHROME_CLIENT_SECRET=your_client_secret
CHROME_REFRESH_TOKEN=your_refresh_token
CHROME_APP_ID=your_app_id

# Firefox Add-ons
FIREFOX_JWT_ISSUER=your_jwt_issuer
FIREFOX_JWT_SECRET=your_jwt_secret
FIREFOX_ADDON_ID=your_addon_id

# Microsoft Edge Add-ons
EDGE_CLIENT_ID=your_client_id
EDGE_CLIENT_SECRET=your_client_secret
EDGE_PRODUCT_ID=your_product_id
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (git checkout -b feature/amazing-feature)
3. Commit your changes (git commit -m 'Add amazing feature')
4. Push to the branch (git push origin feature/amazing-feature)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for details.

## 🙏 Acknowledgments

- Thanks to the Trello community for their continuous feedback and feature requests
- Built with marked.js for markdown parsing
- Inspired by the community discussion about table support in Trello

## 📞 Support

- 🐛 [Report bugs](https://github.com/pke/trello-markdown-renderer/issues)
- 💡 [Request features](https://github.com/pke/trello-markdown-renderer/issues)
- 💬 [Community discussions](https://github.com/pke/trello-markdown-renderer/discussions)
