# X Bookmarks Explorer

> A client-side web application for browsing 200 curated X/Twitter bookmarks from @shinydiscobear with filtering, images, and categorization.

## 🚀 Live Demo

**URL:** https://fierce-scroll-7bsr.here.now/

## ✨ Features

- **200 Curated Bookmarks** from @shinydiscobear
- **6 Categories**: Design & Code, Game Development, Vibe Coding, Security, Terminals, Other
- **Real-time Filtering**: Search by text, filter by category or author
- **Multiple Sort Options**: Date, Likes, Bookmarks (ascending/descending)
- **View Modes**: Grid or List layout
- **Responsive Design**: Works on mobile, tablet, and desktop
- **Dark Theme**: Modern dark UI with smooth animations
- **Cards Display**: Author avatars, text preview, media images, engagement metrics
- **No Backend**: All data embedded inline - no API calls or fetch required

## 📁 Project Structure

```
x-bookmarks-explorer/
├── index.html          # Main application
├── README.md           # Project documentation
├── CHANGELOG.md        # Release history
├── AGENTS.md           # Agent instructions
└── .gitignore          # Git ignore rules
```

## 💻 Development

### Prerequisites

None! This is a pure client-side application. Just open `index.html` in a browser.

### Running Locally

```bash
# Clone the repository
git clone https://github.com/collectivewinca/x-bookmarks-explorer.git
cd x-bookmarks-explorer

# Open in browser
open index.html
# or: start index.html
# or: python3 -m http.server 8000
```

### Deploying

The app can be deployed to any static hosting service:
- GitHub Pages
- Netlify
- Vercel
- Cloudflare Pages
- here.now (as currently deployed)

## 📊 Categories

| Category | Count | Description |
|----------|-------|-------------|
| Design & Code | 93 | UI/UX, frontend, web design, landing pages, React, CSS |
| Game Development | 8 | Game engines, Unity, Unreal, 3D, physics, terrain |
| Vibe Coding | 15 | Claude Code, agents, automation, MCP, AI workflows |
| Security | 4 | Authentication, encryption, MFA, SSO, vulnerabilities |
| Terminals | 6 | CLI, command line, shell, TUI, automation |
| Other | 98 | Everything else |

## 🎨 Design

- **Theme**: Dark mode with orange accent (`#ff6b35`)
- **Colors**:
  - Background: `#0a0a0a`
  - Cards: `#141414`
  - Text: `#e0e0e0`
  - Soft text: `#8a8a8a`
  - Border: `#2a2a2a`
- **Typography**: System fonts (-apple-system, BlinkMacSystemFont, etc.)
- **Category Badges**: Each category has a unique gradient color

## 🛠️ Data Structure

The bookmark data is embedded directly in the HTML as a JavaScript array. Each bookmark object contains:

```javascript
{
  id: "2115738391467946090",
  text: "GitHub is a goldmine for game developers...",
  author: "heyrimsha",
  authorName: "Rimsha Bhardwaj",
  authorImage: "https://pbs.twimg.com/profile_images/...",
  likes: 4920,
  retweets: 432,
  replies: 52,
  bookmarks: 10064,
  views: 269576,
  date: "2026-10-29 05:31",
  url: "https://x.com/heyrimsha/status/2115738391467946090",
  media: [{ type: "photo", url: "..." }],
  category: "Game Development"
}
```

## 🔧 Customization

To add or modify bookmarks:

1. Edit the `allBookmarks` array in `index.html`
2. Update the category mapping if adding new categories
3. Update the category color definitions in CSS

## 📜 License

MIT License - Feel free to use, modify, and distribute.

## 🙏 Acknowledgments

- Built with data from @shinydiscobear's X/Twitter bookmarks
- Powered by Mistral Vibe
- Deployed on here.now

---

**Repository:** https://github.com/collectivewinca/x-bookmarks-explorer
