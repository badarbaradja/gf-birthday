# Romantic Birthday Website

A romantic, cute, and dreamy interactive birthday website created as a gift from Nadhiva Rifka Alifiah to César Defaz Cevallos.

## Project Overview

This is a single-page React application with multiple interactive sections featuring:
- Soft pastel pink and white design theme
- Interactive emoji matching memory game
- Password-protected anniversary date validation
- Animated "Reasons I Love You" hearts
- Typing animation secret letter
- Custom sound effects for all interactions
- Smooth page transitions and micro-interactions

## Technical Architecture

### Core Technology Stack
- **React 18.3.1** with TypeScript for component-based architecture
- **Framer Motion 11.0.8** for sophisticated animations and transitions
- **Tailwind CSS 3.4.17** for responsive, utility-first styling
- **Vite 7.0.0** for fast development and optimized builds
- **Web Audio API** for custom sound effects generation

### Application Structure
```
src/
├── pages/              # Page components for each section
│   ├── WelcomePage.tsx         # Landing page with call-to-action
│   ├── MiniGamePage.tsx        # Emoji matching memory game
│   ├── PasswordPage.tsx        # Anniversary date validation
│   ├── ReasonsPage.tsx         # Interactive hearts with reasons
│   └── SecretLetterPage.tsx    # Typing animation letter
├── utils/
│   └── soundEffects.ts         # Web Audio API sound system
├── App.tsx                    # Main app with routing and transitions
├── index.css                  # Global styles and animations
└── main.tsx                   # Application entry point
```

### Key Features Implementation

#### Sound System (`src/utils/soundEffects.ts`)
- Custom Web Audio API implementation
- Four distinct sound effects: pop, ding, boop, cheer
- No external audio files required
- Generated programmatically using oscillators

#### Page Flow Management
- Centralized state management in `App.tsx`
- Smooth transitions using Framer Motion's AnimatePresence
- Sequential page progression with sound triggers
- No external routing library required

#### Animation System
- Framer Motion for all animations
- Custom keyframe animations in CSS
- Floating decorative elements with continuous motion
- Interactive hover and tap states
- Typing animation for letter reveal

#### Game Logic
- Memory matching game with 6 emoji pairs
- Card flip animations with 3D transforms
- Match detection and celebration effects
- Move counter and game completion detection

## Development Commands

```bash
# Install dependencies
npm install

# Development server (for testing)
npm run dev

# Production build
npm run build

# Preview production build
npm run preview
```

## Design System

### Color Palette
- Primary: Pink gradients (`from-pink-50` to `from-pink-500`)
- Background: Soft pastel pink and white blends
- Accent: Pink-400 to pink-500 for interactive elements
- Text: Pink-800 for headers, pink-600 for body text

### Typography
- Font: Poppins (Google Fonts)
- Weights: 400 (regular), 500 (medium), 600 (semibold), 700 (bold)
- Responsive scaling with mobile-first approach

### Animation Patterns
- Page transitions: Fade and slide with `anticipate` easing
- Button interactions: Scale transforms with shadow effects
- Decorative elements: Continuous floating and rotation
- Card flips: 3D rotation transforms
- Typing effect: Character-by-character reveal

## Build Configuration

### Vite Configuration
- React plugin with TypeScript support
- Optimized production builds with code splitting
- CSS processing with PostCSS and Tailwind
- Asset optimization and gzip compression

### Browser Compatibility
- Modern browsers with ES6+ support
- Web Audio API for sound effects
- CSS Grid and Flexbox for layouts
- CSS custom properties for theming

## Special Implementation Notes

### Sound Effects
All sounds are generated programmatically using the Web Audio API:
- **Pop**: Dual-tone chirp (800Hz → 1000Hz)
- **Ding**: Harmonious chime (1200Hz → 1600Hz)
- **Boop**: Low-frequency square wave (400Hz)
- **Cheer**: Ascending arpeggio (C-E-G-C)

### Password Validation
- Correct password: `01102024` (DDMMYYYY format)
- Shake animation on incorrect attempts
- Success sparkle effect on correct entry
- No backend storage - client-side only

### Responsive Design
- Mobile-first approach with Tailwind breakpoints
- Touch-optimized interactions
- Flexible grid layouts
- Scalable typography

## Performance Optimizations

- Lazy loading of page components
- Optimized animation performance with `will-change`
- Efficient re-rendering with React hooks
- Minimal bundle size with tree shaking
- CSS-in-JS for scoped styles

## Deployment Notes

The application builds to static files suitable for:
- Static hosting services (Netlify, Vercel, GitHub Pages)
- CDN deployment
- Direct file serving
- No server-side requirements

## Maintenance

### Adding New Pages
1. Create new page component in `src/pages/`
2. Add page type to `Page` union in `App.tsx`
3. Implement page in renderPage() function
4. Add navigation logic as needed

### Modifying Sound Effects
Update `src/utils/soundEffects.ts`:
- Adjust frequencies for different tones
- Add new sound methods as needed
- Modify envelope parameters for attack/decay

### Customizing Animations
- Page transitions: Modify `pageVariants` and `pageTransition` in `App.tsx`
- Component animations: Update Framer Motion props in individual components
- CSS animations: Edit keyframes in `src/index.css`

## Design Enhancement Features

### Modern Design System (Updated 2025)
- **Glassmorphism Effects**: Semi-transparent cards with backdrop blur (`glass-card` utility class)
- **Gradient Text**: Animated gradient text for headings (`gradient-text` utility class)
- **Multi-layer Backgrounds**: Gradient backgrounds with image overlays and radial spots
- **Enhanced Depth**: Card depth system with three levels (`card-depth-1`, `card-depth-2`, `card-depth-3`)
- **Shimmer Effects**: Animated shimmer overlays for buttons and interactive elements
- **Pulse Glow**: Breathing glow animation for matched cards and special elements

### Visual Enhancements
- **Background Image**: Hero background from Unsplash integrated with CDN
- **Floating Decorative Elements**: 8 animated emojis with varied timing and motion paths
- **Radial Gradient Spots**: Pulsing gradient circles for atmospheric depth
- **Enhanced Shadows**: Layered shadow system with pink-tinted depth
- **Improved Typography**: Expanded font weight range (300-800) and better spacing

### Interactive Features
- **Button Animations**: Shimmer effects, scale transforms, and glow on hover
- **Card Hover States**: Lift effect with enhanced shadows and color transitions
- **Smooth Page Transitions**: Spring-based animations with better easing
- **Responsive Design**: Enhanced mobile and desktop layouts with better spacing