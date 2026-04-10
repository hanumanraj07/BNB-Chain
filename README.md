YouTube Video Link: https://youtu.be/3jgkmWfxwuE?si=tMJMfOW48bZn1NiK

LinkedIn Profile: www.linkedin.com/in/hanuman-rajpurohit-203880383

# BNB Chain Website - React

A modern, redesigned React implementation of the BNB Chain website with premium UI/UX, micro-animations, responsive design, and AI-powered chatbot.

![BNB Chain](https://cdn.cookielaw.org/logos/ae41c6b2-058d-429f-b670-c89bbe34ec85/01929491-d19e-7690-a763-aa48a451d2c7/79b977da-95c8-4706-9ebe-b0810f8c9519/Frame_480972175.png)

## Tech Stack

- **React 18** - UI library
- **React Router 6** - Client-side routing
- **Vite** - Build tool and dev server
- **CSS3** - Advanced styling with CSS variables
- **Google Gemini API** - AI-powered chatbot

## Project Structure

```
bnb-chain-react/
├── index.html
├── package.json
├── vite.config.js
├── .env                     # Environment variables (API keys)
├── .env.example             # Example env file
├── README.md
└── src/
    ├── main.jsx              # React entry point
    ├── App.jsx               # Root component with routing
    ├── index.css             # Global styles, variables, typography
    ├── hooks/
    │   ├── useIntersectionObserver.js   # Scroll-triggered animations
    │   └── useCountUp.js               # Animated number counting
    ├── components/
    │   ├── Header.jsx/.css    # Sticky nav with frosted glass
    │   ├── Footer.jsx/.css   # Multi-column footer
    │   ├── Card.jsx/.css     # Reusable glass-morphism card
    │   ├── StatItem.jsx/.css # Animated stat counter component
    │   ├── FloatingButton.jsx/.css  # AI Chat trigger button
    │   └── Chatbot.jsx/.css  # AI-powered chatbot modal
    └── pages/
        ├── Home.jsx/.css      # Hero, features, builder stats
        ├── Developers.jsx/.css # Docs, tools, grants
        ├── Ecosystem.jsx/.css  # Filterable project grid
        └── Technology.jsx/.css # Charts, comparison bars, tokenomics
```

---

## Features

### Visual Design

- **Glassmorphism Cards** - Frosted glass effect with backdrop blur
- **Gradient Borders** - Animated borders on hover
- **Layered Shadows** - Multi-level depth with color tints
- **BNB Yellow Theme** - Primary: #f0b90b on dark: #1e2026
- **Particle Background** - Animated floating particles in hero section
- **Grid Overlay** - Subtle grid pattern in hero background

### Typography System

```css
--text-xs: 0.75rem
--text-sm: 0.875rem
--text-base: 1rem
--text-lg: 1.125rem
--text-xl: 1.25rem
--text-2xl: 1.5rem
--text-3xl: 1.875rem
--text-4xl: 2.25rem
--text-5xl: 3rem
```

### Micro-Animations

- **Entrance Animations** - Fade-in + slide-up using Intersection Observer
- **Typewriter Effect** - Hero headline types out on load
- **Hover Transitions** - All cards, buttons, nav links
- **Particle Background** - 20 floating particles in hero section
- **Shimmer Effects** - Glowing CTA buttons
- **Scroll Indicator** - Animated mouse wheel in hero
- **Pulsing FAB** - Floating action button with ring pulse

---

## Components

### `<Card />`

Reusable card with multiple variants:
```jsx
<Card 
  variant="default"     // default | gradient | highlight
  padding="medium"      // none | small | medium | large
  hover={true}         // enable/disable lift effect
>
  {children}
</Card>
```

### `<StatItem />`

Animated counting stat:
```jsx
<StatItem 
  value="2000"
  prefix="$"
  suffix="+"
  label="Total Value Locked"
/>
```

### `<Header />`

Sticky navigation with:
- Frosted glass blur on scroll (backdrop-filter)
- Active route indicator (yellow underline)
- Animated hamburger menu (mobile)
- Smooth slide-down menu animation
- "Ask AI" button to open chatbot

### `<FloatingButton />`

Persistent floating action button:
- Fixed position (bottom-right corner)
- Pulse animation ring
- Toggle between chat/close icon
- Triggers chatbot modal on click

### `<Chatbot />`

AI-powered conversational interface:
- Integrates with Google Gemini API
- Context-aware responses about BNB Chain
- Quick question shortcuts
- Typing indicator (3-dot animation)
- Error handling for API issues
- Message history with auto-scroll
- User/bot message differentiation

---

## Pages

### Home (`/`)

- **Hero Section**
  - Animated particle/grid background
  - Typewriter headline effect
  - Glowing CTA button with shimmer
  - AI search bar with focus state
  - Scroll indicator animation
  
- **Features Grid** - 3 glassmorphism cards
- **Builder Stats** - Visual image gallery with stat overlays
- **Stats Section** - 4 animated counting numbers
- **Ecosystem Preview** - 4 category cards with hover effects

### Developers (`/developers`)

- Page header with gradient background
- Step-by-step getting started guide (numbered steps)
- 6 development tool cards
- 3 learning resource cards
- 3 grant program cards with feature lists
- 3 support channel cards

### Ecosystem (`/ecosystem`)

- Animated filter with underline indicator
- 6 category filters (All, DeFi, NFTs, Gaming, Tools, Infrastructure)
- Smooth card grid transitions during filtering
- 10 project cards with icons
- Growth section with highlight cards

### Technology (`/technology`)

- **Specs Header** - 6 key metrics grid
- Dual-chain architecture cards (Beacon Chain, Smart Chain)
- PoSA consensus mechanism details
- **Animated Progress Bars** - TPS, Block Time, Fees comparison
- **Finality Chart** - Visual bar comparison vs ETH/Solana
- Security & Reliability section (4 cards)
- Developer Tools & APIs grid (6 tools)
- Upcoming Innovations (zkBNB, Greenfield, Sidechains)
- Tokenomics section (4 cards)

---

## Custom Hooks

### `useIntersectionObserver`

Triggers animations when elements enter viewport:
```javascript
const [ref, isVisible] = useIntersectionObserver({ 
  threshold: 0.2,
  rootMargin: '0px'
});
```

### `useCountUp`

Animated number counter with easing:
```javascript
const { ref, displayValue } = useCountUp(2000, {
  duration: 2500,
  prefix: '$',
  suffix: '+',
  decimals: 1,
});
```

---

## Responsive Breakpoints

| Breakpoint | Width | Description |
|------------|-------|-------------|
| Mobile | < 375px | Compact layouts, stacked cards |
| Tablet | < 768px | Hamburger menu, 2-column grids |
| Desktop | < 1024px | Expanded navigation |
| Large | < 1280px | Full 4-column grids |

### Mobile Optimizations
- Minimum 44px tap targets
- No horizontal overflow
- Reduced padding/margins
- Full-width buttons
- Collapsible navigation

---

## Getting Started

```bash
# Navigate to project
cd bnb-chain-react

# Install dependencies
npm install

# Start dev server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

---

## AI Chatbot Setup

The website includes an AI-powered chatbot powered by Google Gemini.

### 1. Get a Gemini API Key

1. Visit [Google AI Studio](https://aistudio.google.com/app/apikey)
2. Sign in with your Google account
3. Click **"Create API Key"**
4. Select **"Create API key in new project"**
5. Copy the generated API key

### 2. Configure Environment Variable

Create a `.env` file in the project root:
```bash
VITE_GEMINI_API_KEY=your_api_key_here
```

Or copy the example:
```bash
cp .env.example .env
# Then edit .env and add your API key
```

### 3. Restart Development Server

```bash
npm run dev
```

### Using the Chatbot

Access the chatbot via:
- **Floating AI button** (bottom-right corner)
- **"Ask AI" button** in header navigation
- **Hero search bar** on homepage

### Available Models

The chatbot automatically tries these models in order:
1. `gemini-2.0-flash` (fastest)
2. `gemini-2.5-flash`
3. `gemini-2.0-flash-lite`

---

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| `--primary` | #f0b90b | Buttons, highlights, active states |
| `--primary-light` | #fcd535 | Gradients, glows |
| `--primary-dark` | #e6a800 | Button hover states |
| `--dark` | #1e2026 | Background |
| `--dark-gray` | #2b2f36 | Cards, sections |
| `--medium-gray` | #474d57 | Borders, muted text |
| `--light-gray` | #eaecef | Body text on dark |
| `--white` | #ffffff | Headings |

---

## Animation Reference

### Timing Functions
```css
--transition-fast: 150ms ease
--transition-base: 250ms ease
--transition-slow: 400ms ease
--transition-spring: 500ms cubic-bezier(0.34, 1.56, 0.64, 1)
```

### Keyframes
| Name | Description |
|------|-------------|
| `fadeInUp` | Entry animation for sections |
| `pulse` | Breathing effect for indicators |
| `shimmer` | Light sweep on CTA buttons |
| `float` | Gentle bounce for icons |
| `glow` | Shadow pulse for emphasis |
| `blink` | Cursor blink for typewriter |
| `scroll` | Mouse wheel animation |
| `slideUp` | Chatbot modal entrance |
| `particle-float` | Hero background particles |
| `typing` | 3-dot loading indicator |

---

## Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

> Requires CSS `backdrop-filter` for glassmorphism (graceful fallback for unsupported browsers)

---

## Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `VITE_GEMINI_API_KEY` | Google Gemini API key | Yes |

---

## License

&copy; 2024 BNB Chain. All rights reserved.


BNB Chain™ is a trademark of its respective owner.
 
