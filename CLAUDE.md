# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

MonsterSurvivors.com is a single-page website for an online survival game that embeds a Unity WebGL game via iframe. The site uses Tailwind CSS for styling and features a modern, Apple-inspired design with responsive layouts.

## Architecture

### Core Structure
- **Single HTML file**: `index.html` contains the entire website
- **No build process**: Static HTML with embedded CSS and JavaScript
- **CDN dependencies**: Tailwind CSS loaded from CDN
- **Game integration**: Unity WebGL game embedded via iframe from `cloud.onlinegames.io`

### Key Components
1. **Navigation**: Fixed header with mobile-responsive hamburger menu
2. **Hero Section**: Game title, description, and CTAs
3. **Game Container**: 16:9 aspect ratio iframe with responsive design
4. **Features Grid**: 3-column responsive grid showcasing game features
5. **How to Play**: Two-column layout with controls and tips
6. **About Section**: Prose content about the game
7. **Footer**: 4-column layout with links and social media

### Design System
- **Color Palette**: Apple-inspired purple to pink gradients (`#667eea` to `#764ba2`)
- **Typography**: System fonts with Tailwind utilities
- **Glassmorphism**: Modern glass effects with backdrop blur
- **Animations**: Fade-in effects and smooth hover transitions
- **Responsive**: Mobile-first design with Tailwind breakpoints

## Development Workflow

### File Structure
```
/
├── index.html          # Main website file
├── CLAUDE.md           # This file
└── .git/              # Git repository
```

### Making Changes
1. Edit `index.html` directly
2. Test changes in browser
3. Commit changes to Git
4. Deploy to web server

### Styling Approach
- **Primary**: Tailwind CSS classes from CDN
- **Custom CSS**: Embedded `<style>` block for specific effects
- **Responsive Design**: Tailwind responsive utilities (sm:, md:, lg:)

## Game Integration

### Iframe Configuration
- **Source**: `https://cloud.onlinegames.io/games/2025/unity/monster-survivors/index-og.html`
- **Aspect Ratio**: 16:9 (56.25% padding-bottom)
- **Responsive**: Maintains aspect ratio across all devices
- **Styling**: Rounded corners, shadow effects

### Game Features Showcased
- Fast-paced action gameplay
- Character progression system
- Infinite replayability
- Multiple weapons
- Leaderboards
- Mobile compatibility

## SEO Optimization

### Meta Tags
- **Canonical URL**: `https://monstersurvivors.com/`
- **Open Graph**: Facebook/social sharing
- **Twitter Cards**: Twitter sharing
- **Meta Description**: Search engine optimization

### Content Structure
- **H1**: Main game title
- **H2**: Section headers (Features, How to Play, About)
- **Semantic HTML**: Proper HTML5 structure
- **Alt Text**: Images have descriptive alt attributes

## Performance Considerations

### Optimization
- **CDN Delivery**: Tailwind CSS from CDN
- **Lazy Loading**: Iframe has loading="lazy"
- **Minimal Dependencies**: Single external CSS framework
- **Inline CSS**: Custom styles embedded to avoid extra requests

### Mobile Optimization
- **Touch-friendly**: Large tap targets
- **Responsive menus**: Hamburger menu for mobile
- **Viewport settings**: Proper meta viewport tag
- **Performance**: Lightweight, fast-loading

## Content Updates

### Game Information
- Update feature descriptions in Features section
- Modify "How to Play" instructions based on game changes
- Update meta descriptions with current game details

### SEO Content
- Modify title and meta descriptions for better ranking
- Update canonical URL if domain changes
- Refresh Open Graph images when needed

## Deployment Notes

### Static Hosting
This is a static website that can be hosted on:
- Apache/Nginx web servers
- Static hosting services (Netlify, Vercel, GitHub Pages)
- CDN services (Cloudflare, AWS CloudFront)

### File Serving
- `index.html` should be served as the default document
- Ensure proper MIME types for HTML files
- Configure HTTPS for production deployment
- Set appropriate caching headers for static assets

## Browser Compatibility

### Target Browsers
- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile browsers (iOS Safari, Chrome Mobile)
- WebGL support required for Unity game

### Fallbacks
- No JavaScript required for basic navigation
- CSS gracefully degrades in older browsers
- Iframe requires modern browser for Unity WebGL support