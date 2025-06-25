# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Slidev presentation about strategic AI usage in development, comparing it to poker vs gambling. The talk is titled "¿Estás programando o apostando?" (Are you programming or gambling?) and focuses on intentional "vibecoding" with AI tools.

## Development Commands

```bash
# Start development server
npm run dev

# Build the presentation
npm run build

# Export to PDF
npm run export

# Access presenter mode
# Run npm run dev, then open http://localhost:3030/presenter
```

## Architecture

- **Framework**: Slidev (Vue-based presentation framework)
- **Theme**: Seriph with custom styling
- **Components**: Vue 3 components with TypeScript
- **Animations**: @vueuse/motion for card animations and transitions
- **Styling**: Utility-first CSS with custom color variables

### Key Files

- `slides.md`: Main presentation content with frontmatter configuration
- `components/FallingCard.vue`: Animated card component for AI tool showcase
- `components/Counter.vue`: Basic counter component (Slidev default)
- `package.json`: Contains all build scripts and dependencies

### Styling System

The presentation uses a custom color scheme defined in CSS variables:
- Primary colors: Dark purple/blue gradient (--primary-900 to --primary-100)
- Accent: Green (--accent-400)
- Card components use glassmorphism with backdrop-filter and border gradients

### Content Structure

- Interactive opening with AI tool cards animation
- Strategic comparison between gambling and poker
- Technical analogies (MPC, schedulers)
- Practical "vibecoding" strategies
- Call to awareness conclusion

The presentation is designed for a 10-minute talk with specific timing markers in comments.