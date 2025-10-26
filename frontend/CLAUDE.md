# Professional React + TypeScript + Convex Frontend Application

## Project Overview

Build a production-quality frontend application using React, TypeScript, and Convex with professional design standards. All code and design must meet enterprise-grade quality standards with no placeholder content or "AI slop" aesthetics.

## Technology Stack

- **Framework**: React 18+ with TypeScript
- **Database & Backend**: Convex
- **Styling**: CSS Modules or Styled Components (NO Tailwind)
- **Animation**: Framer Motion
- **Build Tool**: Vite
- **Package Manager**: npm or pnpm

## Design Principles

### Typography Standards

**NO INTER FONT** - Use a sophisticated, multi-font type system:

#### Primary Font Pairing Options

1. **Serif + Sans Pairing**:
   - Headings: Playfair Display, Lora, or Crimson Pro
   - Body: Work Sans, Open Sans, or Source Sans Pro

2. **Modern Sans Pairing**:
   - Headings: Space Grotesk, Outfit, or Manrope
   - Body: DM Sans, Plus Jakarta Sans, or Rubik

3. **Classic Editorial**:
   - Headings: Fraunces or Libre Baskerville
   - Body: IBM Plex Sans or Public Sans

#### Type Scale

Implement a proper typographic scale with clear hierarchy:

```typescript
// typography.ts
export const typography = {
  // Display - Hero sections, major headings
  display: {
    fontSize: '3.75rem',      // 60px
    lineHeight: '1.1',
    fontWeight: 700,
    letterSpacing: '-0.02em'
  },
  
  // H1 - Page titles
  h1: {
    fontSize: '3rem',         // 48px
    lineHeight: '1.2',
    fontWeight: 700,
    letterSpacing: '-0.01em'
  },
  
  // H2 - Section headings
  h2: {
    fontSize: '2.25rem',      // 36px
    lineHeight: '1.25',
    fontWeight: 600,
    letterSpacing: '-0.01em'
  },
  
  // H3 - Sub-sections
  h3: {
    fontSize: '1.875rem',     // 30px
    lineHeight: '1.3',
    fontWeight: 600,
    letterSpacing: '0'
  },
  
  // H4 - Card titles
  h4: {
    fontSize: '1.5rem',       // 24px
    lineHeight: '1.4',
    fontWeight: 600,
    letterSpacing: '0'
  },
  
  // H5 - Small headings
  h5: {
    fontSize: '1.25rem',      // 20px
    lineHeight: '1.4',
    fontWeight: 500,
    letterSpacing: '0'
  },
  
  // Body Large - Intro text, important content
  bodyLarge: {
    fontSize: '1.125rem',     // 18px
    lineHeight: '1.6',
    fontWeight: 400,
    letterSpacing: '0'
  },
  
  // Body - Default text
  body: {
    fontSize: '1rem',         // 16px
    lineHeight: '1.6',
    fontWeight: 400,
    letterSpacing: '0'
  },
  
  // Body Small - Secondary text
  bodySmall: {
    fontSize: '0.875rem',     // 14px
    lineHeight: '1.5',
    fontWeight: 400,
    letterSpacing: '0'
  },
  
  // Caption - Labels, metadata
  caption: {
    fontSize: '0.75rem',      // 12px
    lineHeight: '1.4',
    fontWeight: 500,
    letterSpacing: '0.02em',
    textTransform: 'uppercase' as const
  },
  
  // Button text
  button: {
    fontSize: '1rem',
    lineHeight: '1',
    fontWeight: 500,
    letterSpacing: '0.01em'
  }
} as const;
```

### Color Palette

Professional, muted, pastel colors only. NO bright neons or saturated colors.

```typescript
// colors.ts
export const colors = {
  // Primary palette - Muted blues
  primary: {
    50: '#f0f4f8',
    100: '#d9e6f2',
    200: '#b3cde0',
    300: '#8ab4ce',
    400: '#6a9fb5',
    500: '#4a8a9d',   // Primary brand
    600: '#3a6e7d',
    700: '#2a525d',
    800: '#1a363e',
    900: '#0d1b1f'
  },
  
  // Secondary palette - Warm neutrals with pink undertones
  secondary: {
    50: '#faf7f5',
    100: '#f0e8e3',
    200: '#e0d1c7',
    300: '#d0baab',
    400: '#c0a390',
    500: '#a88b74',   // Secondary brand
    600: '#8a6f5d',
    700: '#6b5446',
    800: '#4d3930',
    900: '#2e1f1a'
  },
  
  // Accent - Muted lavender
  accent: {
    50: '#f5f3f9',
    100: '#e8e3f0',
    200: '#d1c7e0',
    300: '#baabce',
    400: '#a390bc',
    500: '#8b74aa',   // Accent
    600: '#6f5d8a',
    700: '#53466b',
    800: '#38304d',
    900: '#1c182e'
  },
  
  // Neutrals - Warm grays
  neutral: {
    50: '#fafaf9',
    100: '#f5f5f4',
    200: '#e7e5e4',
    300: '#d6d3d1',
    400: '#a8a29e',
    500: '#78716c',
    600: '#57534e',
    700: '#44403c',
    800: '#292524',
    900: '#1c1917'
  },
  
  // Semantic colors - muted versions
  semantic: {
    success: '#6b9f7f',     // Muted sage green
    warning: '#d4a574',     // Muted amber
    error: '#c47b7b',       // Muted rose
    info: '#7a9fbe'         // Muted sky blue
  },
  
  // Backgrounds
  background: {
    primary: '#ffffff',
    secondary: '#fafaf9',
    tertiary: '#f5f5f4',
    elevated: '#ffffff'
  },
  
  // Text
  text: {
    primary: '#1c1917',
    secondary: '#57534e',
    tertiary: '#78716c',
    disabled: '#a8a29e',
    inverse: '#ffffff'
  },
  
  // Borders
  border: {
    light: '#e7e5e4',
    medium: '#d6d3d1',
    dark: '#a8a29e'
  }
} as const;
```

### Design Standards

1. **NO EMOJIS** - Use professional iconography only (e.g., Lucide React, Heroicons)
2. **NO "VIBE CODED" LANGUAGE** - Professional, clear copy only
3. **Proper spacing system** - 4px base unit, consistent rhythm
4. **Proper shadows** - Subtle, realistic depth
5. **Smooth animations** - 60fps, purposeful motion
6. **Accessibility first** - WCAG AA minimum, AAA preferred

## File Structure

```
/frontend
├── src/
│   ├── components/
│   │   ├── common/           # Reusable UI components
│   │   │   ├── Button/
│   │   │   │   ├── Button.tsx
│   │   │   │   ├── Button.module.css
│   │   │   │   └── index.ts
│   │   │   ├── Input/
│   │   │   ├── Card/
│   │   │   ├── Modal/
│   │   │   └── Typography/
│   │   ├── layout/           # Layout components
│   │   │   ├── Header/
│   │   │   ├── Footer/
│   │   │   ├── Sidebar/
│   │   │   └── Container/
│   │   └── features/         # Feature-specific components
│   │       ├── auth/
│   │       ├── dashboard/
│   │       └── [feature]/
│   ├── convex/
│   │   ├── schema.ts         # Convex schema definitions
│   │   ├── functions/        # Convex queries and mutations
│   │   │   ├── users.ts
│   │   │   └── [resource].ts
│   │   └── _generated/       # Auto-generated Convex files
│   ├── hooks/                # Custom React hooks
│   │   ├── useAuth.ts
│   │   ├── useMediaQuery.ts
│   │   └── [feature].ts
│   ├── lib/                  # Utilities and helpers
│   │   ├── utils.ts
│   │   ├── validators.ts
│   │   └── constants.ts
│   ├── styles/               # Global styles and design tokens
│   │   ├── globals.css
│   │   ├── typography.ts
│   │   ├── colors.ts
│   │   ├── spacing.ts
│   │   └── animations.ts
│   ├── types/                # TypeScript type definitions
│   │   ├── index.ts
│   │   └── [domain].ts
│   ├── pages/                # Page components
│   │   ├── Home/
│   │   ├── Dashboard/
│   │   └── [Page]/
│   ├── App.tsx
│   ├── main.tsx
│   └── vite-env.d.ts
├── convex/                   # Convex backend folder (root level)
│   ├── schema.ts
│   └── [functions].ts
├── public/
│   └── assets/
├── index.html
├── package.json
├── tsconfig.json
├── vite.config.ts
└── convex.json
```

## Component Architecture

### Example: Professional Button Component

```typescript
// components/common/Button/Button.tsx
import { ButtonHTMLAttributes, forwardRef } from 'react';
import { motion, HTMLMotionProps } from 'framer-motion';
import styles from './Button.module.css';

type ButtonVariant = 'primary' | 'secondary' | 'outline' | 'ghost';
type ButtonSize = 'small' | 'medium' | 'large';

interface ButtonProps extends Omit<ButtonHTMLAttributes<HTMLButtonElement>, 'className'> {
  variant?: ButtonVariant;
  size?: ButtonSize;
  fullWidth?: boolean;
  loading?: boolean;
  leftIcon?: React.ReactNode;
  rightIcon?: React.ReactNode;
}

export const Button = forwardRef<HTMLButtonElement, ButtonProps>(
  (
    {
      variant = 'primary',
      size = 'medium',
      fullWidth = false,
      loading = false,
      leftIcon,
      rightIcon,
      disabled,
      children,
      ...props
    },
    ref
  ) => {
    const MotionButton = motion.button;

    return (
      <MotionButton
        ref={ref}
        className={`${styles.button} ${styles[variant]} ${styles[size]} ${
          fullWidth ? styles.fullWidth : ''
        }`}
        disabled={disabled || loading}
        whileHover={{ scale: disabled ? 1 : 1.02 }}
        whileTap={{ scale: disabled ? 1 : 0.98 }}
        transition={{ duration: 0.15, ease: 'easeOut' }}
        {...props}
      >
        {loading && (
          <span className={styles.spinner} aria-label="Loading">
            <svg className={styles.spinnerSvg} viewBox="0 0 24 24">
              <circle
                className={styles.spinnerCircle}
                cx="12"
                cy="12"
                r="10"
                fill="none"
                strokeWidth="3"
              />
            </svg>
          </span>
        )}
        {!loading && leftIcon && <span className={styles.leftIcon}>{leftIcon}</span>}
        <span className={styles.label}>{children}</span>
        {!loading && rightIcon && <span className={styles.rightIcon}>{rightIcon}</span>}
      </MotionButton>
    );
  }
);

Button.displayName = 'Button';
```

```css
/* components/common/Button/Button.module.css */
.button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  border: none;
  border-radius: 0.5rem;
  font-family: 'DM Sans', sans-serif;
  font-weight: 500;
  letter-spacing: 0.01em;
  cursor: pointer;
  transition: all 0.15s ease-out;
  position: relative;
  white-space: nowrap;
  user-select: none;
  outline: none;
}

.button:focus-visible {
  outline: 2px solid var(--color-primary-500);
  outline-offset: 2px;
}

.button:disabled {
  cursor: not-allowed;
  opacity: 0.5;
}

/* Sizes */
.small {
  padding: 0.5rem 1rem;
  font-size: 0.875rem;
  height: 2rem;
}

.medium {
  padding: 0.75rem 1.5rem;
  font-size: 1rem;
  height: 2.75rem;
}

.large {
  padding: 1rem 2rem;
  font-size: 1.125rem;
  height: 3.5rem;
}

/* Variants */
.primary {
  background: var(--color-primary-500);
  color: var(--color-text-inverse);
}

.primary:hover:not(:disabled) {
  background: var(--color-primary-600);
  box-shadow: 0 4px 12px rgba(74, 138, 157, 0.2);
}

.secondary {
  background: var(--color-secondary-500);
  color: var(--color-text-inverse);
}

.secondary:hover:not(:disabled) {
  background: var(--color-secondary-600);
  box-shadow: 0 4px 12px rgba(168, 139, 116, 0.2);
}

.outline {
  background: transparent;
  color: var(--color-primary-500);
  border: 1.5px solid var(--color-primary-500);
}

.outline:hover:not(:disabled) {
  background: var(--color-primary-50);
  border-color: var(--color-primary-600);
}

.ghost {
  background: transparent;
  color: var(--color-text-secondary);
}

.ghost:hover:not(:disabled) {
  background: var(--color-neutral-100);
  color: var(--color-text-primary);
}

/* Full width */
.fullWidth {
  width: 100%;
}

/* Icons */
.leftIcon,
.rightIcon {
  display: flex;
  align-items: center;
  font-size: 1.25em;
}

/* Loading spinner */
.spinner {
  position: absolute;
  display: flex;
  align-items: center;
  justify-content: center;
}

.spinnerSvg {
  width: 1.25em;
  height: 1.25em;
  animation: spin 0.8s linear infinite;
}

.spinnerCircle {
  stroke: currentColor;
  stroke-linecap: round;
  stroke-dasharray: 50;
  stroke-dashoffset: 25;
}

@keyframes spin {
  to {
    transform: rotate(360deg);
  }
}
```

## Convex Integration

### Setup

```bash
# In /frontend directory
npm install convex
npx convex dev
```

### Schema Definition

```typescript
// convex/schema.ts
import { defineSchema, defineTable } from 'convex/server';
import { v } from 'convex/values';

export default defineSchema({
  users: defineTable({
    email: v.string(),
    name: v.string(),
    createdAt: v.number(),
    updatedAt: v.number(),
  }).index('by_email', ['email']),

  // Add your tables here
});
```

### Query Example

```typescript
// convex/functions/users.ts
import { query, mutation } from '../_generated/server';
import { v } from 'convex/values';

export const getUsers = query({
  handler: async (ctx) => {
    return await ctx.db.query('users').collect();
  },
});

export const getUserByEmail = query({
  args: { email: v.string() },
  handler: async (ctx, args) => {
    return await ctx.db
      .query('users')
      .filter((q) => q.eq(q.field('email'), args.email))
      .first();
  },
});

export const createUser = mutation({
  args: {
    email: v.string(),
    name: v.string(),
  },
  handler: async (ctx, args) => {
    const now = Date.now();
    return await ctx.db.insert('users', {
      email: args.email,
      name: args.name,
      createdAt: now,
      updatedAt: now,
    });
  },
});
```

### React Integration

```typescript
// src/App.tsx
import { ConvexProvider, ConvexReactClient } from 'convex/react';

const convex = new ConvexReactClient(import.meta.env.VITE_CONVEX_URL);

function App() {
  return (
    <ConvexProvider client={convex}>
      {/* Your app */}
    </ConvexProvider>
  );
}

export default App;
```

```typescript
// Using in components
import { useQuery, useMutation } from 'convex/react';
import { api } from '../convex/_generated/api';

function UserList() {
  const users = useQuery(api.functions.users.getUsers);
  const createUser = useMutation(api.functions.users.createUser);

  if (users === undefined) {
    return <LoadingSpinner />;
  }

  return (
    <div>
      {users.map((user) => (
        <div key={user._id}>{user.name}</div>
      ))}
    </div>
  );
}
```

## Animation Guidelines

Use Framer Motion sparingly and purposefully. Every animation should have a reason.

```typescript
// lib/animations.ts
export const fadeIn = {
  initial: { opacity: 0 },
  animate: { opacity: 1 },
  exit: { opacity: 0 },
  transition: { duration: 0.2, ease: 'easeOut' }
};

export const slideUp = {
  initial: { opacity: 0, y: 20 },
  animate: { opacity: 1, y: 0 },
  exit: { opacity: 0, y: -20 },
  transition: { duration: 0.3, ease: [0.22, 1, 0.36, 1] }
};

export const scaleIn = {
  initial: { opacity: 0, scale: 0.95 },
  animate: { opacity: 1, scale: 1 },
  exit: { opacity: 0, scale: 0.95 },
  transition: { duration: 0.2, ease: 'easeOut' }
};

export const staggerContainer = {
  animate: {
    transition: {
      staggerChildren: 0.05
    }
  }
};

// Usage
import { motion } from 'framer-motion';
import { fadeIn, slideUp } from '@/lib/animations';

<motion.div {...fadeIn}>
  <motion.h1 {...slideUp}>Title</motion.h1>
</motion.div>
```

## Global Styles Setup

```css
/* styles/globals.css */
@import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=DM+Sans:wght@400;500;600&display=swap');

:root {
  /* Colors - Primary */
  --color-primary-50: #f0f4f8;
  --color-primary-100: #d9e6f2;
  --color-primary-200: #b3cde0;
  --color-primary-300: #8ab4ce;
  --color-primary-400: #6a9fb5;
  --color-primary-500: #4a8a9d;
  --color-primary-600: #3a6e7d;
  --color-primary-700: #2a525d;
  --color-primary-800: #1a363e;
  --color-primary-900: #0d1b1f;

  /* Colors - Secondary */
  --color-secondary-50: #faf7f5;
  --color-secondary-100: #f0e8e3;
  --color-secondary-200: #e0d1c7;
  --color-secondary-300: #d0baab;
  --color-secondary-400: #c0a390;
  --color-secondary-500: #a88b74;
  --color-secondary-600: #8a6f5d;
  --color-secondary-700: #6b5446;
  --color-secondary-800: #4d3930;
  --color-secondary-900: #2e1f1a;

  /* Colors - Neutral */
  --color-neutral-50: #fafaf9;
  --color-neutral-100: #f5f5f4;
  --color-neutral-200: #e7e5e4;
  --color-neutral-300: #d6d3d1;
  --color-neutral-400: #a8a29e;
  --color-neutral-500: #78716c;
  --color-neutral-600: #57534e;
  --color-neutral-700: #44403c;
  --color-neutral-800: #292524;
  --color-neutral-900: #1c1917;

  /* Semantic colors */
  --color-success: #6b9f7f;
  --color-warning: #d4a574;
  --color-error: #c47b7b;
  --color-info: #7a9fbe;

  /* Text colors */
  --color-text-primary: #1c1917;
  --color-text-secondary: #57534e;
  --color-text-tertiary: #78716c;
  --color-text-disabled: #a8a29e;
  --color-text-inverse: #ffffff;

  /* Background colors */
  --color-bg-primary: #ffffff;
  --color-bg-secondary: #fafaf9;
  --color-bg-tertiary: #f5f5f4;

  /* Border colors */
  --color-border-light: #e7e5e4;
  --color-border-medium: #d6d3d1;
  --color-border-dark: #a8a29e;

  /* Spacing scale (4px base) */
  --space-1: 0.25rem;   /* 4px */
  --space-2: 0.5rem;    /* 8px */
  --space-3: 0.75rem;   /* 12px */
  --space-4: 1rem;      /* 16px */
  --space-5: 1.25rem;   /* 20px */
  --space-6: 1.5rem;    /* 24px */
  --space-8: 2rem;      /* 32px */
  --space-10: 2.5rem;   /* 40px */
  --space-12: 3rem;     /* 48px */
  --space-16: 4rem;     /* 64px */
  --space-20: 5rem;     /* 80px */
  --space-24: 6rem;     /* 96px */

  /* Border radius */
  --radius-sm: 0.25rem;
  --radius-md: 0.5rem;
  --radius-lg: 0.75rem;
  --radius-xl: 1rem;
  --radius-full: 9999px;

  /* Shadows */
  --shadow-sm: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
  --shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.07), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.08), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
  --shadow-xl: 0 20px 25px -5px rgba(0, 0, 0, 0.08), 0 10px 10px -5px rgba(0, 0, 0, 0.04);

  /* Z-index scale */
  --z-dropdown: 1000;
  --z-sticky: 1100;
  --z-fixed: 1200;
  --z-modal-backdrop: 1300;
  --z-modal: 1400;
  --z-popover: 1500;
  --z-tooltip: 1600;

  /* Transitions */
  --transition-fast: 150ms ease-out;
  --transition-base: 200ms ease-out;
  --transition-slow: 300ms ease-out;
}

/* Reset and base styles */
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {
  font-size: 16px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-rendering: optimizeLegibility;
}

body {
  font-family: 'DM Sans', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  font-size: 1rem;
  line-height: 1.6;
  color: var(--color-text-primary);
  background-color: var(--color-bg-primary);
}

h1, h2, h3, h4, h5, h6 {
  font-family: 'Space Grotesk', sans-serif;
  font-weight: 600;
  line-height: 1.2;
  color: var(--color-text-primary);
}

button {
  font-family: inherit;
}

/* Focus styles for accessibility */
*:focus-visible {
  outline: 2px solid var(--color-primary-500);
  outline-offset: 2px;
}

/* Utility classes */
.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border: 0;
}
```

## TypeScript Configuration

```json
// tsconfig.json
{
  "compilerOptions": {
    "target": "ES2020",
    "useDefineForClassFields": true,
    "lib": ["ES2020", "DOM", "DOM.Iterable"],
    "module": "ESNext",
    "skipLibCheck": true,
    "moduleResolution": "bundler",
    "allowImportingTsExtensions": true,
    "resolveJsonModule": true,
    "isolatedModules": true,
    "noEmit": true,
    "jsx": "react-jsx",
    "strict": true,
    "noUnusedLocals": true,
    "noUnusedParameters": true,
    "noFallthroughCasesInSwitch": true,
    "baseUrl": ".",
    "paths": {
      "@/*": ["./src/*"],
      "@/components/*": ["./src/components/*"],
      "@/lib/*": ["./src/lib/*"],
      "@/styles/*": ["./src/styles/*"],
      "@/types/*": ["./src/types/*"],
      "@/hooks/*": ["./src/hooks/*"]
    }
  },
  "include": ["src"],
  "references": [{ "path": "./tsconfig.node.json" }]
}
```

## Code Quality Standards

### TypeScript

- Use strict mode
- Define explicit types for all props and function parameters
- Use `interface` for object shapes, `type` for unions/intersections
- Never use `any` - use `unknown` if type is truly unknown
- Use const assertions where appropriate

### React

- Use functional components exclusively
- Use proper prop destructuring
- Implement proper error boundaries
- Use React.memo() for expensive components
- Implement proper loading and error states
- Use proper key props in lists

### CSS

- Use CSS Modules for component-specific styles
- Follow BEM naming convention within modules
- Mobile-first responsive design
- Use CSS variables for theming
- Avoid magic numbers - use design tokens

### Accessibility

- Semantic HTML elements
- Proper heading hierarchy
- ARIA labels where necessary
- Keyboard navigation support
- Focus management
- Screen reader tested
- Minimum contrast ratio: 4.5:1 for normal text, 3:1 for large text

## Performance Optimization

1. **Code splitting**: Use React.lazy() for route-based splitting
2. **Image optimization**: WebP format, lazy loading, responsive images
3. **Memoization**: React.memo, useMemo, useCallback where appropriate
4. **Bundle size**: Keep under 200KB initial bundle
5. **Tree shaking**: Ensure proper ES module imports
6. **Convex optimization**: Implement proper pagination and indexing

## Testing Strategy

```typescript
// Example component test
import { render, screen, fireEvent } from '@testing-library/react';
import { Button } from './Button';

describe('Button', () => {
  it('renders with correct text', () => {
    render(<Button>Click me</Button>);
    expect(screen.getByText('Click me')).toBeInTheDocument();
  });

  it('calls onClick when clicked', () => {
    const handleClick = jest.fn();
    render(<Button onClick={handleClick}>Click me</Button>);
    fireEvent.click(screen.getByText('Click me'));
    expect(handleClick).toHaveBeenCalledTimes(1);
  });

  it('is disabled when loading', () => {
    render(<Button loading>Click me</Button>);
    expect(screen.getByRole('button')).toBeDisabled();
  });
});
```

## Development Workflow

1. **Setup**:
   ```bash
   npm create vite@latest frontend -- --template react-ts
   cd frontend
   npm install
   npm install convex framer-motion
   npm install -D @types/node
   ```

2. **Environment variables**:
   ```env
   VITE_CONVEX_URL=your_convex_url
   ```

3. **Development**:
   ```bash
   npm run dev          # Start Vite dev server
   npx convex dev       # Start Convex development
   ```

4. **Build**:
   ```bash
   npm run build
   npm run preview
   ```

## Production Checklist

- [ ] All TypeScript errors resolved
- [ ] No console warnings or errors
- [ ] Accessibility audit passed (Lighthouse score 95+)
- [ ] Performance audit passed (Lighthouse score 90+)
- [ ] Mobile responsive on all breakpoints
- [ ] Cross-browser tested (Chrome, Firefox, Safari, Edge)
- [ ] Error boundaries implemented
- [ ] Loading states for all async operations
- [ ] Form validation with clear error messages
- [ ] Proper meta tags and SEO optimization
- [ ] Analytics implemented
- [ ] Error tracking set up (e.g., Sentry)
- [ ] Environment variables properly configured
- [ ] Build size under 200KB (gzipped)

## Key Reminders

1. **NO TAILWIND** - Use CSS Modules or Styled Components only
2. **NO INTER FONT** - Use sophisticated font pairings
3. **NO EMOJIS** - Professional icons only
4. **NO VIBE CODED LANGUAGE** - Clear, professional copy
5. **NO AI SLOP** - Production-quality code and design only
6. **PASTEL COLORS** - Muted, professional palette only
7. **PROPER TYPE SCALE** - Multiple font sizes for clear hierarchy
8. **FRAMER MOTION** - For purposeful animations only

---

This document defines the standards for a production-quality React + TypeScript + Convex application. Every component, style, and interaction should meet these standards before deployment.