# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Shopify Dawn theme - Shopify's reference theme built with a web-native, performance-first approach. The codebase follows strict principles: no frameworks, server-rendered with Liquid, and functional over pixel-perfect design.

## Development Commands

```bash
# Launch development server with hot reload
shopify theme serve

# Run theme validation and linting
shopify theme check

# Push theme changes to Shopify store
shopify theme push

# Pull latest theme from Shopify store
shopify theme pull

# Run specific theme checks
shopify theme check --check <check-name>
```

## Architecture and Structure

The theme uses Shopify's standard architecture with Liquid templating:

- **Business logic** stays on the server (Liquid)
- **JavaScript** only for progressive enhancement
- **CSS** uses custom properties and follows BEM-like naming
- **Sections** are the primary building blocks for page customization
- **Snippets** contain reusable code fragments
- **Templates** define page structures and use JSON for section composition

Key architectural patterns:
- Component-based CSS (one file per component)
- Deferred loading for non-critical JavaScript
- SVG icons stored as individual files in assets/
- Global JavaScript utilities in `assets/global.js`
- Form handling through Shopify's native forms API

## Critical Development Guidelines

1. **Performance is paramount** - Target zero CLS, no render-blocking JavaScript
2. **Progressive enhancement** - Features must work without JavaScript
3. **Web-native only** - No frameworks, libraries, or polyfills
4. **Accessibility first** - Follow WCAG guidelines, semantic HTML
5. **Mobile-first responsive** - Design for small screens first

## Theme Customization

- Theme settings defined in `config/settings_schema.json`
- Current settings stored in `config/settings_data.json`
- Sections include schema for customizer options
- All user-facing text must use translation keys from `locales/`

## Testing and Validation

Before committing changes:
1. Run `shopify theme check` to validate code
2. Test on multiple browsers (Chrome, Safari, Firefox, Edge)
3. Verify mobile responsiveness
4. Check accessibility with screen readers
5. Monitor performance metrics (use Chrome DevTools)

## Version Control

- Current version: Dawn 15.3.0
- Follow semantic versioning for updates
- Update `release-notes.md` for significant changes
- The theme tracks upstream Dawn for updates