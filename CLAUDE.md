# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static website for investigative journalist Michael Volpe, focused on exposing family court corruption and promoting a national Family Justice Movement. The site is deployed to `volpesvoice.com` via GitHub Pages.

## Architecture

**Technology Stack:** Pure HTML/CSS/JavaScript (no build tools or frameworks)
- Static website with vanilla HTML5, CSS3, and JavaScript
- No package.json, build process, or dependencies
- GitHub Pages deployment with custom domain
- Google Fonts integration (Poppins & Inter)

**File Structure:**
- `index.html` - Main homepage with hero, stories, books, and bio sections
- `family-justice.html` - Dedicated page for the 50-state movement
- `images/` - All assets including story images, book covers, and branding
- `CNAME` - GitHub Pages domain configuration

## Key Features

**Dynamic Content:**
- Substack RSS integration for latest articles (via RSS2JSON API)
- Embedded YouTube videos for testimonies and investigations
- Newsletter signup forms
- Copy-to-clipboard functionality for representative contact templates

**Design System:**
- **Colors:** Dark navy (#18121E), steel blue (#4682B4), burgundy (#984B43)
- **Typography:** Poppins for headings, Inter for body text
- **Layout:** CSS Grid and Flexbox with mobile-first responsive design
- **Animations:** CSS transitions and keyframe animations

## Development Workflow

**Adding Content:**
- **Images:** Place in `/images/` folder and reference with relative paths
- **Videos:** Use embedded instructions in HTML comments (YouTube IDs from URL after `v=`, Vimeo IDs are the numbers in URL)
- **Stories:** Automatically pulled from Substack RSS feed
- **Text Updates:** Direct HTML editing

**Testing:**
- Open HTML files directly in browser (no dev server needed)
- Test responsive design across device sizes
- Verify external integrations (Substack RSS, YouTube embeds)

**Deployment:**
- Changes pushed to main branch automatically deploy via GitHub Pages
- Domain configured through CNAME file pointing to volpesvoice.com

## Code Patterns

**HTML Structure:**
- Semantic HTML5 with proper heading hierarchy
- Comprehensive meta tags for SEO and social sharing
- Inline CSS within `<style>` tags (no external stylesheets)
- JavaScript at bottom of body for performance

**CSS Organization:**
- Reset styles at top
- Typography definitions
- Layout utilities (flexbox, grid)
- Component-specific styles
- Media queries for responsive design
- Animation definitions

**JavaScript Features:**
- Mobile menu toggle
- Scroll-to-top button with smooth scrolling
- Newsletter form handling
- RSS feed integration with error handling
- Clipboard API for copy functionality

## Content Management

**Images:**
- Story investigation images (Cardinal Wuerl, Cindy Palmer, Keith Dobbs, Sandra Grazzini-Rucki)
- Book covers (prosecutors gone wild, definitive dossier)
- Branding assets (electric_lockup.png, solid_metal_lockup.png, black_robe_mafia.png)
- Profile image (michaelvolpe_profile_shot.png)

**External Integrations:**
- Substack RSS endpoint: Uses RSS2JSON service for CORS-friendly access
- YouTube embeds: Direct iframe integration
- Social media links: Twitter, YouTube, Substack profiles

## Common Tasks

**Adding a new investigation story:**
1. Add story images to `/images/` folder
2. Update Substack (stories auto-populate from RSS)
3. If needed, manually add to recent stories section in index.html

**Adding a new video:**
1. Upload to YouTube/Vimeo
2. Extract video ID from URL (see HTML comments for instructions)
3. Update iframe src with new video ID

**Updating Family Justice Movement progress:**
1. Modify progress tracker in family-justice.html
2. Update state checkmarks (✓) as committees are established
3. Add new state victories to the progress section