# AVO — Modern Web Developer Portfolio & Pande Permadi Personal Site

**Dual-Page PHP Website dengan Modular CSS & JavaScript ES6 Modules**

**Version:** 2.0.0 (Dual-Site + Theme System Refactor)

---

## 🚀 Quick Start

```bash
# Access via browser
http://localhost/avo/           # AVO Landing Page
http://localhost/avo/pandepermadi.php  # Personal Portfolio

# Or production
https://pandepermadi.com/avo/
https://pandepermadi.com/
```

**No installation needed** - just copy folder to web server!

> 📁 **For complete directory structure, see** [`PROJECT_STRUCTURE.md`](PROJECT_STRUCTURE.md)

---

## ✨ Features

### **1. Dual-Page Architecture** 🎯

**Two distinct pages with different purposes:**

| Feature | `index.php` (AVO) | `pandepermadi.php` (Personal) |
|---------|-------------------|-------------------------------|
| **Style** | Corporate, Professional | Personal, Creative |
| **Themes** | 10 themes available | 5 themes (CSS variables) |
| **Language** | Indonesian | English |
| **Hero** | CodeRain + Tech Marquee | 3D Aquarium |
| **Services** | 9 cards (Indonesian) | 7 cards (English) |
| **Projects** | Timeline Portfolio | Card Stack |
| **Fish Cursor** | ✅ Yes | ❌ No |
| **Hanging Card** | ✅ Yes | ❌ No |

---

### **2. Theme System** 🎨

**Two independent theme systems:**

#### **index.php (10 Themes)**
| # | Theme | Primary | Style |
|---|-------|---------|-------|
| 1 | Default | #8b5cf6 | Professional Purple |
| 2 | Dark Teal Neon | #00f9ff | Cyberpunk |
| 3 | Dark Orange Neon | #ff6b00 | Fiery |
| 4 | Cyberpunk | #fcee0a | Edgy |
| 5 | Cyberpunk Crazy | Multi | Madness |
| 6 | Corporate Blue | #1e40af | Trust |
| 7 | Executive Charcoal | #374151 | Premium |
| 8 | Clean Slate | #0f172a | Minimal |
| 9 | Forest Corporate | #166534 | Eco |
| 10 | Midnight Professional | #1e293b | Dark Tech |

**Storage:** `data/theme_studio.json` (~40 bytes)

#### **pandepermadi.php (5 Themes)**
| Theme | Accent Primary | Aquarium Theme |
|-------|----------------|----------------|
| Dark Teal | #38d0c0 | Deep ocean blue |
| Dark Red | #ef4444 | Red/dark mood |
| Ocean Blue | #0ea5e9 | Ocean blue |
| Coral Orange | #f97316 | Warm coral |
| Deep Purple | #a855f7 | Mystic purple |

**Storage:** `data/theme_pribadi.json` (~66 bytes)

**Features:**
- ✅ Instant switch (no page reload)
- ✅ Persists after refresh
- ✅ Aquarium atmosphere changes
- ✅ CSS variables for easy theming

---

### **3. 3D Aquarium** 🐠

**Shared feature across both pages:**

- **10 swimming fish** (random from 35 models)
- **7 coral models** with vibrant colors
- **Day/night cycle** (20 second loop)
- **Pause/Play button**
- **Bubble particles**
- **Interactive feeding** (click to feed)
- **Theme-responsive** water color & lighting

**Controls:**
- 🐟 **Pause/Play** - Toggle animation
- 🌅 **Phase Indicator** - Current day/night phase

---

### **4. Card Swiper Portfolio** 🃏

**Tinder-style project showcase:**

- **Drag** with mouse or touch
- **Keyboard** controls (arrow keys)
- **11+ project cards** in stack
- **Card edges visible** (rotated stack)
- **Project detail modal** on click

**Swipe Directions:**
- ← **Left** - Reject
- → **Right** - Like
- ↑ **Up** - Super like
- ↓ **Down** - Pass

---

### **5. Fish Cursor Follower** 🐟

**3D fish follows cursor (index.php only):**

- **Random fish** from 12 models each refresh
- **Smooth movement** with lerp
- **Tail wagging** animation
- **Loading indicator**
- **Non-blocking** (doesn't cover content)

---

### **6. Hanging Card Animation** 🃏

**Interactive business card (About section):**

- **Spring physics** (Hooke's Law)
- **Drag** in any direction
- **Natural swing** with gravity
- **Bounce effect** on release
- **Constraints** keep card in bounds

**Physics Parameters:**
```javascript
SPRING_K: 0.015    // Soft spring
DAMPING: 0.995     // Long swing
GRAVITY: 0.1       // Smooth fall
BOUNCE: 0.4        // Energy loss
```

---

### **7. Tech Stack Marquee** 💻

**Infinite scrolling technologies (index.php):**

- **2 rows** opposite directions
- **30+ technologies** with icons
- **Hover effects** with neon glow

**Row 1 (← Left):** Python, Django, PHP, Laravel, JavaScript, React, Node.js, MySQL, PostgreSQL, Docker, Git, Tailwind, Android, Rust, Ruby

**Row 2 (→ Right):** Go, TypeScript, Vue.js, Next.js, MongoDB, Redis, Kubernetes, AWS, Flutter, Swift, Kotlin, GraphQL, REST API, Linux, Nginx

---

### **8. Network/Constellation Animation** 🌐

**CodeRain background effect (index.php):**

- **Connected points** with lines
- **Mouse interaction**
- **Code syntax display**
- **Gentle floating**

---

### **9. Responsive Design** 📱

**Mobile-first approach:**

| Breakpoint | Layout | Features |
|------------|--------|----------|
| **Desktop** (>968px) | Full | All features |
| **Tablet** (769-968px) | Adjusted | Optimized spacing |
| **Mobile** (<768px) | Compact | Touch-friendly |

**Mobile Optimizations:**
- Card stack without rotation
- Smaller fonts and padding
- Touch-friendly swipe (50px threshold)
- Compact controls

---

## 🎨 Design System

### **Colors**

**pandepermadi.php (Dark Teal Base):**
```css
--accent-primary: #38d0c0
--accent-primary-hover: #2bd5c4
```

**index.php (Theme-based):**
```css
/* Default Purple */
--primary-500: #8b5cf6
--secondary-500: #ec4899
--accent-500: #06b6d4
```

---

### **Typography**

```css
/* pandepermadi.php */
--font-body: 'Inter', sans-serif
--font-mono: 'JetBrains Mono', monospace

/* index.php */
--font-heading: 'Space Grotesk', monospace
--font-body: 'Inter', sans-serif
```

---

### **Spacing**

```css
--spacing-xs: 0.25rem
--spacing-sm: 0.5rem
--spacing-md: 1rem
--spacing-lg: 1.5rem
--spacing-xl: 2rem
--spacing-2xl: 3rem
--spacing-3xl: 4rem

--radius-sm: 8px
--radius-md: 12px
--radius-lg: 16px
--radius-xl: 24px
--radius-full: 9999px
```

---

## 🛠️ Customization

### **Add New Theme (index.php)**

**Step 1:** Create CSS file
```css
/* css/15-11-theme-new-theme.css */
[data-theme="new-theme"] {
  --primary-500: #yourcolor;
  --secondary-500: #anothercolor;
}
```

**Step 2:** Update `save_theme_studio.php`
```php
$themeMap = [
  // ... existing
  'new-theme' => '15-11'
];
```

**Step 3:** Add to HTML
```html
<option value="new-theme">New Theme Name</option>
```

---

### **Add New Theme (pandepermadi.php)**

**Step 1:** Update theme config in `pandepermadi.php`
```javascript
var themes = {
  // ... existing
  'new-theme': {
    accentPrimary: '#color',
    accentPrimaryHover: '#colorhover',
    aquarium: {
      water: 0x0a0a0b,
      fogDensity: 0.03,
      lighting: 0x4080ff
    }
  }
};
```

**Step 2:** Add option to selector
```html
<option value="new-theme">New Theme</option>
```

**Step 3:** Update `save_theme_pribadi.php`
```php
$allowed_themes = ['dark-teal', 'dark-red', /* 'new-theme' */];
```

---

### **Add JavaScript Module**

**Step 1:** Create module
```javascript
// js/modules/new-module.js
export const NewModule = {
  init() {
    // Your code
  }
};
```

**Step 2:** Import in `index.js`
```javascript
import { NewModule } from './new-module.js';

document.addEventListener('DOMContentLoaded', () => {
  NewModule.init();
});
```

---

## 🐛 Troubleshooting

### **Theme Not Saving**
```bash
# Check permissions
chmod 666 data/theme_*.json

# Check PHP handler exists
ls -la save_theme_*.php
```

### **3D Models Not Loading**
```bash
# Check model paths
ls -la model/ikan/

# Check console for GLTFLoader errors
```

### **CSS Not Updating**
```bash
# Hard refresh
Ctrl + Shift + R

# Clear browser cache
```

### **Modules Not Loading**
```javascript
// Check console for 404 errors
// Verify import paths in index.js
```

---

## 🚀 Performance

### **Optimization Strategies**

| Area | Technique | Result |
|------|-----------|--------|
| **CSS** | Modular (30+ files) | Maintainable |
| **JS** | ES6 modules | Tree-shaking ready |
| **3D** | Lazy load models | Fast initial load |
| **Animations** | CSS transforms | GPU accelerated |
| **Theme** | JSON storage (~50 bytes) | Fast save/load |

### **File Sizes**

| Type | Size | Notes |
|------|------|-------|
| **CSS** | ~80KB | 30 modular files |
| **JS** | ~60KB | 12 modules + aquarium |
| **3D Models** | ~7MB | 35 fish + 7 coral |
| **Images** | ~400KB | favicon + OG cover |
| **JSON** | ~100 bytes | 2 theme files |

---

## 📊 Browser Support

| Browser | Version | Support |
|---------|---------|---------|
| Chrome | 90+ | ✅ Full |
| Firefox | 88+ | ✅ Full |
| Safari | 14+ | ✅ Full |
| Edge | 90+ | ✅ Full |
| Mobile Safari | iOS 14+ | ✅ Full |
| Chrome Mobile | Android 10+ | ✅ Full |

---

## 📝 Version History

### **v2.0.0** (March 29, 2026) - Current

**Major Changes:**
- ✅ Dual-page architecture (`index.php` + `pandepermadi.php`)
- ✅ Independent theme systems (10 + 5 themes)
- ✅ ES6 modules for JavaScript
- ✅ Theme system refactor (97% smaller JSON)
- ✅ DRY principles applied throughout

**Files Added:**
- ✅ `pandepermadi.php` - Personal portfolio
- ✅ `save_theme_pribadi.php` - Theme handler
- ✅ `data/theme_pribadi.json` - Theme storage
- ✅ `js/modules/` - ES6 modules directory

**Files Updated:**
- ✅ `.cursorrules` - DRY & Modular guidelines
- ✅ `theme-manager.js` - Dual-site support
- ✅ `save_theme_studio.php` - Fixed path & permissions

---

### **v1.1.0** (March 28, 2026)

**Features:**
- ✅ Hanging card animation (About section)
- ✅ 5 corporate themes (10 total)
- ✅ Service cards layout fix
- ✅ Mobile swipe optimizations

---

### **v1.0.0** (March 27, 2026)

**Initial Release:**
- ✅ Modular CSS (18 files)
- ✅ Card Swiper portfolio
- ✅ 3D Aquarium
- ✅ Fish cursor follower
- ✅ Theme system
- ✅ Tech marquee
- ✅ Hamburger menu

---

## 🤝 Credits

**Created by:** Pande Permadi
**Location:** Jakarta & Kendari, Indonesia
**Website:** 
- https://pandepermadi.com/ (Personal)
- https://pandepermadi.com/avo/ (AVO)

**Email:** owner@pandepermadi.com
**WhatsApp:** +62 821 9584 7899

---

## 📄 License

© 2026 Pande Permadi. All rights reserved.

---

## 🎯 Quick Reference

### **Access URLs**
```
Local:
  - AVO:          http://localhost/avo/
  - Personal:     http://localhost/avo/pandepermadi.php

Production:
  - AVO:          https://pandepermadi.com/avo/
  - Personal:     https://pandepermadi.com/
```

### **Keyboard Shortcuts**
- **Arrow Keys** - Swipe cards
- **ESC** - Close menu
- **Space** - Pause aquarium

### **Touch Gestures**
- **Swipe** - Navigate cards
- **Tap** - Open links
- **Drag** - Move hanging card / fish cursor

---

**Last Updated:** March 29, 2026
**Version:** 2.0.0 (Dual-Site + DRY Refactor)
**Status:** ✅ Production Ready
