# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static website for OllamaFlow, a load balancing and model orchestration solution for Ollama. The website is hosted on GitHub Pages and consists of:

- `index.html` - Main landing page with hero section, features, API compatibility, use cases, and get started sections
- `styles.css` - CSS styling with CSS custom properties for theming (light/dark mode support)
- `script.js` - JavaScript for theme switching, smooth scrolling, animations, and code copy functionality
- `CNAME` - Domain configuration for GitHub Pages

## Development Commands

This is a static website with no build process or package managers. Files can be edited directly and previewed by opening `index.html` in a browser or through a local web server.

To preview locally:
```bash
# Simple HTTP server (if Python is available)
python -m http.server 8000

# Or using Node.js http-server (if installed)
npx http-server
```

## Architecture

### Theme System
- Uses CSS custom properties (`--variable-name`) for theming
- Light/dark theme switching via `data-theme` attribute on `html` element
- Theme preference stored in localStorage
- All theme variables defined in `:root` and `[data-theme="dark"]` selectors

### JavaScript Features
- Theme toggle functionality with icon switching
- Smooth scrolling navigation
- Intersection Observer for scroll-triggered animations
- Dynamic navbar styling on scroll
- Copy-to-clipboard functionality for code blocks
- Mobile-responsive design considerations

### Styling Structure
- Mobile-first responsive design
- CSS Grid and Flexbox layouts
- Consistent spacing using CSS custom properties (`--space-*`)
- Component-based styling approach
- Hover effects and transitions throughout

### Content Sections
- Hero section with gradient text effects
- Feature grid with hover animations
- API compatibility showcase
- Use cases grid
- Installation/getting started with code examples
- Footer with links

## File Organization

- All styles are in a single `styles.css` file organized by component sections
- JavaScript functionality is in `script.js` with logical groupings
- HTML uses semantic structure with clear section divisions
- External assets (logo, favicon) are loaded from the main OllamaFlow repository

## Development Notes

- The website promotes the main OllamaFlow project (https://github.com/ollamaflow/ollamaflow)
- All external links open in new tabs
- Code examples are provided for Docker and .NET installation methods
- Responsive breakpoint is at 768px for mobile adaptations