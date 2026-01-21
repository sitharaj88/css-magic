# 🌌 Day 21: Aurora Borealis

A mesmerizing pure CSS recreation of the Northern Lights (Aurora Borealis) with animated light waves, floating particles, and a scenic silhouette landscape.

## ✨ Features

- 🎨 **Multi-layered Aurora Waves** - Four independently animated gradient layers creating realistic light movement
- ✨ **Twinkling Star Field** - Pure CSS star background with subtle twinkle animation
- 🏔️ **Scenic Silhouette** - Mountain range and pine tree silhouettes for depth
- 💫 **Floating Particles** - Rising light particles that enhance the magical atmosphere
- 🌈 **Aurora Pillars** - Vertical light rays that dance and sway
- 🃏 **Interactive Card** - Hover-activated rotating glow effect
- 📱 **Fully Responsive** - Adapts beautifully to all screen sizes
- 🎭 **Pure CSS** - No JavaScript required!

## 🚀 Technical Highlights

- **CSS Animations** - Complex keyframe animations with varying durations and delays
- **Gradient Mastery** - Multiple linear gradients with transparency for realistic light effects
- **CSS Filters** - Blur effects to soften and blend aurora layers
- **Transform Combinations** - translateX, skewX, and scaleY for organic wave movement
- **Conic Gradients** - Used for the rotating card glow effect
- **Backdrop Filter** - Glassmorphism effect on the interactive card
- **CSS-only Stars** - Radial gradients creating a twinkling starfield
- **Pure CSS Shapes** - Mountains and trees using border triangles

## 🎨 Color Palette

| Color | Hex | Usage |
|-------|-----|-------|
| Aurora Green | `#00ff7f` | Primary aurora layer |
| Turquoise | `#40e0d0` | Secondary highlights |
| Purple | `#8a2be2` | Violet aurora layer |
| Deep Blue | `#00bfff` | Blue aurora accent |
| Pink | `#ff69b4` | Subtle pink tones |
| Night Sky | `#0a0a1a` | Background base |

## 🛠️ Usage

1. Open `index.html` in any modern browser
2. Sit back and enjoy the mesmerizing light show
3. Hover over the card to see the interactive glow effect

## 📜 CSS Techniques Used

### Aurora Wave Animation
```css
@keyframes aurora-wave-1 {
    0%, 100% {
        transform: translateX(-10%) skewX(-5deg) scaleY(1);
    }
    50% {
        transform: translateX(10%) skewX(5deg) scaleY(0.9);
    }
}
```

### Twinkling Stars with Radial Gradients
```css
background-image:
    radial-gradient(2px 2px at 20px 30px, #fff, transparent),
    radial-gradient(2px 2px at 40px 70px, rgba(255,255,255,0.8), transparent);
```

### Conic Gradient Rotating Glow
```css
background: conic-gradient(
    from 0deg,
    transparent,
    rgba(0, 255, 127, 0.1),
    transparent,
    rgba(138, 43, 226, 0.1),
    transparent
);
animation: rotate-glow 10s linear infinite;
```

## 🌟 Browser Support

- Chrome 80+
- Firefox 75+
- Safari 14+
- Edge 80+

## 📝 Notes

This effect is perfect for:
- Landing page backgrounds
- Hero sections
- Loading screens
- Creative portfolios
- Ambient web experiences

The animation is designed to be smooth and non-distracting while still capturing the ethereal beauty of the natural phenomenon.
