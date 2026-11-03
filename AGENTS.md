# Agent Instructions - X Bookmarks Explorer

This file provides guidance for AI agents (including Mistral Vibe) working on this project.

## Project Overview

**Name:** X Bookmarks Explorer  
**Purpose:** Client-side web application for browsing 200 curated X/Twitter bookmarks from @shinydiscobear  
**Stack:** Pure HTML, CSS, JavaScript (no frameworks, no build step)  
**Repo:** https://github.com/collectivewinca/x-bookmarks-explorer  
**Live:** https://fierce-scroll-7bsr.here.now/

## Current State (as of 2026-11-03)

✅ **Completed:**
- 200 bookmarks loaded and categorized
- 6 categories defined and applied
- Client-side filtering (search, category, author, sort)
- Grid/List view toggle
- Responsive design
- Dark theme
- Images and cards display
- Git repository created and pushed
- README, CHANGELOG, AGENTS.md created
- Live deployment on here.now

## What's Next - Priority Tasks

### 🎯 High Priority

1. **Data Refresh**
   - Check if @shinydiscobear has new bookmarks
   - Update `bookmarks_all.json` with latest data
   - Re-categorize new bookmarks
   - Commit changes: `feat: update bookmarks data to [date]`

2. **Improve Categorization**
   - Review current categorization for accuracy
   - Fix any miscategorized bookmarks
   - Consider adding sub-categories
   - Update category keywords in the categorization script

3. **Enhance Filtering**
   - Add date range filter (last 24h, 7d, 30d, etc.)
   - Add likes/bookmarks range sliders
   - Add multi-select for categories
   - Add saved filter presets

4. **Add Article Extraction**
   - Integrate article-extractor skill
   - Add "Extract Article" button on each bookmark card
   - Display extracted content in a modal
   - Save extracted articles to localStorage

### 📋 Medium Priority

5. **Improve UI/UX**
   - Add loading skeleton states
   - Improve empty state messages
   - Add keyboard shortcuts (e.g., `/` to focus search)
   - Add smooth scroll to top on filter change
   - Add copy-to-clipboard for tweet URLs

6. **Add More Data**
   - Include quoted tweets content
   - Add media thumbnails for videos
   - Add tweet language detection
   - Add verified badge indicators

7. **Performance Optimizations**
   - Lazy load images below the fold
   - Implement virtual scrolling for large datasets
   - Compress embedded JSON data
   - Minify CSS and JavaScript

### 💡 Low Priority / Nice to Have

8. **Export Features**
   - Export filtered results as JSON
   - Export as CSV
   - Export as markdown
   - Print-friendly view

9. **Social Features**
   - Add share buttons
   - Add embed code for specific bookmarks
   - Add Twitter/X intents for easy sharing

10. **Advanced Features**
    - Add bookmark notes/annotations
    - Add favorites/star system
    - Add tags (user-defined)
    - Sync with browser bookmarks

11. **Documentation**
    - Add API documentation (for the embedded data structure)
    - Add contribution guidelines
    - Add architecture decisions record

## Agent Workflow

### For Data Updates

```bash
# 1. Pull latest changes
cd /Volumes/T7/x-bookmarks-export/web
git pull origin master

# 2. Update bookmarks data
# (Run your data extraction/fetching script)
python3 update_bookmarks.py

# 3. Test locally
open index.html

# 4. Commit and push
git add .
git commit -m "feat: update bookmarks to [date]"
git push origin master

# 5. Deploy (optional)
here-now update fierce-scroll-7bsr .
```

### For Feature Development

1. **Read the existing code** before making changes
2. **Test locally** by opening index.html in a browser
3. **Keep changes minimal** - one feature per commit
4. **Follow existing patterns** for consistency
5. **Commit with clear messages**
6. **Push to GitHub**
7. **Deploy to here.now** (if applicable)

## File Structure

```
.
├── index.html          # Main application - ALL CHANGES GO HERE
├── README.md           # Project documentation
├── CHANGELOG.md        # Release history
├── AGENTS.md           # This file - agent instructions
└── .gitignore          # Git ignore rules
```

## Important Notes

1. **No Backend:** This is a pure client-side app. All data is embedded in index.html.
2. **No Build Step:** Changes to index.html are immediately visible.
3. **Single File:** All logic, styling, and data are in index.html for simplicity.
4. **Here.now:** The live site auto-deploys from the GitHub repo or local updates.

## Testing

After any changes:
- Open `index.html` in Chrome/Firefox/Safari
- Test filtering works
- Test all categories display
- Test search functionality
- Test responsive behavior (resize window)
- Test on mobile device (if possible)

## Git Workflow

```bash
# Create a feature branch
git checkout -b feature/your-feature-name

# Make changes
# Test

# Commit
git add .
git commit -m "feat: your feature description"

# Push
git push origin feature/your-feature-name

# Create PR on GitHub
# Or merge directly if you have permissions
git checkout master
git merge feature/your-feature-name
git push origin master
```

## Questions?

If you're an agent working on this project and need clarification:
1. Check this AGENTS.md file first
2. Check the CHANGELOG for recent changes
3. Check the README for project overview
4. Check the git history for context
5. Ask the user for clarification if still unclear

---

**Last Updated:** 2026-11-03  
**Maintained by:** Mistral Vibe + collectivewinca
