# 💳 Glass Card Carousel - Pure CSS

> Day 2 of CSS Magic | January 7, 2026

A stunning glassmorphism credit card showcase with animated backgrounds and hover effects — built with **pure CSS**, no JavaScript.

---

## 🎯 Live Demo

Open `index.html` in any modern browser.

---

## ✨ Features

- 💎 Glassmorphism card design
- 🎨 3 distinct color themes (Amber, Rose, Cyan)
- 🌌 Animated gradient orbs background
- 📐 Subtle grid pattern overlay
- ✨ Shimmer effect on hover
- ⬆️ Lift animation on hover
- 🌟 Animated brand text gradient
- 💳 Realistic 3D chip design

---

## 🛠️ CSS Techniques Explained

### 1. Glassmorphism Effect

```css
.card {
    background: linear-gradient(135deg, rgba(245, 158, 11, 0.25) 0%, rgba(245, 158, 11, 0.05) 100%);
    backdrop-filter: blur(20px);
    -webkit-backdrop-filter: blur(20px);
    border: 1px solid rgba(245, 158, 11, 0.4);
    border-top-color: rgba(245, 158, 11, 0.6);
}
```

**How it works:**
- Semi-transparent colored background (25% opacity)
- `backdrop-filter: blur()` blurs content behind the card
- Colored border with brighter top edge (simulates light source)

---

### 2. Animated Background Orbs

```css
.bg::before {
    background: radial-gradient(circle, rgba(99, 102, 241, 0.5) 0%, transparent 70%);
    filter: blur(60px);
    animation: float1 15s ease-in-out infinite;
}

@keyframes float1 {
    0%, 100% { transform: translate(0, 0); }
    50% { transform: translate(50px, 30px); }
}
```

**How it works:**
- `::before` and `::after` pseudo-elements create two orbs
- `radial-gradient` makes circular color blobs
- `filter: blur()` softens the edges
- Animation moves orbs slowly for organic movement

---

### 3. Grid Pattern Overlay

```css
.bg {
    background: 
        linear-gradient(rgba(255,255,255,0.03) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,0.03) 1px, transparent 1px),
        linear-gradient(135deg, #1e1e3f 0%, #2d2d5a 50%, #1a1a40 100%);
    background-size: 40px 40px, 40px 40px, 100% 100%;
}
```

**How it works:**
- First two gradients create horizontal and vertical lines
- `background-size: 40px 40px` sets the grid spacing
- Layered on top of the base gradient

---

### 4. Shimmer Text Animation

```css
.brand {
    background: linear-gradient(135deg, var(--accent) 0%, #fff 50%, var(--accent) 100%);
    background-size: 200% auto;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    animation: shimmerText 3s ease-in-out infinite;
}

@keyframes shimmerText {
    0%, 100% { background-position: 0% center; }
    50% { background-position: 200% center; }
}
```

**How it works:**
- Three-color gradient (accent → white → accent)
- `background-size: 200%` makes gradient twice as wide
- `background-clip: text` applies gradient to text only
- Animation shifts `background-position` for shimmer effect

---

### 5. Card Hover Effects

```css
.card:hover {
    transform: translateY(-12px) scale(1.02);
    box-shadow: 
        0 25px 50px -10px rgba(0, 0, 0, 0.5),
        0 0 40px -10px var(--accent);
}

.card::after {
    /* Shimmer light sweep */
    background: linear-gradient(90deg, transparent, rgba(255,255,255,0.15), transparent);
    transition: left 0.6s ease;
}

.card:hover::after {
    left: 130%;
}
```

**How it works:**
- `translateY(-12px)` lifts card upward
- `scale(1.02)` slightly enlarges the card
- Colored glow added via `box-shadow`
- Shimmer sweeps across via left position change

---

### 6. Realistic Chip Design

```css
.chip {
    background: linear-gradient(135deg, #ffd700 0%, #ffec8b 40%, #daa520 100%);
    box-shadow: 
        0 2px 8px rgba(0,0,0,0.3),
        inset 0 1px 0 rgba(255,255,255,0.4);
}

.chip::before {
    /* Center rectangle */
    border: 1px solid rgba(0,0,0,0.15);
}

.chip::after {
    /* Grid pattern */
    background: 
        repeating-linear-gradient(90deg, transparent 0 8px, rgba(0,0,0,0.1) 8px 9px),
        repeating-linear-gradient(0deg, transparent 0 8px, rgba(0,0,0,0.1) 8px 9px);
}
```

**How it works:**
- Three-color gold gradient for metallic look
- `inset` shadow creates inner highlight
- `::before` adds center contact area
- `::after` creates circuit line pattern

---

## 🎨 Color Palette

| Card | Color Name | Hex | RGB |
|------|------------|-----|-----|
| VISA | Amber | `#f59e0b` | 245, 158, 11 |
| Mastercard | Rose | `#f43f5e` | 244, 63, 94 |
| AMEX | Cyan | `#06b6d4` | 6, 182, 212 |
| Background | Navy | `#1e1e3f` | 30, 30, 63 |
| Orb 1 | Indigo | `#6366f1` | 99, 102, 241 |
| Orb 2 | Pink | `#ec4899` | 236, 72, 153 |

---

## 📐 Key CSS Properties

| Property | Purpose |
|----------|---------|
| `backdrop-filter: blur()` | Frosted glass effect |
| `background-clip: text` | Gradient text |
| `radial-gradient` | Circular color blobs |
| `linear-gradient` | Directional gradients |
| `box-shadow` | Depth and glow effects |
| `transform` | Hover lift animation |
| `transition` | Smooth state changes |
| `animation` | Continuous motion |
| `::before / ::after` | Extra decorative layers |

---

## 📱 Browser Support

| Browser | Support |
|---------|---------|
| Chrome | ✅ Full |
| Firefox | ✅ Full |
| Safari | ✅ Full |
| Edge | ✅ Full |
| IE11 | ❌ No |

---

## 📝 LinkedIn Post Caption

```
💳 Day 2 of #CSSMagic!

Built these glassmorphism credit cards with ZERO JavaScript:

✨ Frosted glass effect (backdrop-filter)
🎨 Animated gradient orbs behind cards
🌟 Shimmer text that flows
⬆️ Smooth hover lift + glow

The secret to good glass UI? CONTRAST!
You need something visual behind it to blur. 🧠

🔗 Live Demo & Code in comments!

What should Day 3 be?
A. Glitch Text Effect
B. 3D Flip Card
C. Liquid Loading Animation

#CSS #WebDev #Frontend #UIUX #Glassmorphism
```

---

## 🔗 Links

- **Series:** CSS Magic
- **Author:** Sitharaj
- **Schedule:** 3x per week (Mon, Wed, Fri)

---

**Made with 💜 using Pure CSS**
