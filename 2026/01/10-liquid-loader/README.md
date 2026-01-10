# 🌊 Liquid Loading Animation - Pure CSS

> Day 3 of CSS Magic | January 10, 2026

A mesmerizing liquid orb loader with morphing shapes, internal waves, floating bubbles, and dripping effects — built with **pure CSS**.

---

## ✨ Features

- 🫧 **Morphing Blob** - Organic 8-point border-radius animation
- 🌊 **Internal Waves** - Rotating wave layers inside the orb
- 💧 **Rising Bubbles** - Animated bubbles floating up
- 💦 **Gravity Drip** - Droplet falling from the orb
- 💫 **Glow Rings** - Expanding pulse rings
- 🪞 **Floor Reflection** - Soft mirror effect below
- 🎨 **Color Cycling** - Gradient shifts cyan → purple → pink

---

## 🛠️ Key CSS Techniques

### 1. Organic Morphing Shape

```css
.orb {
  border-radius: 60% 40% 30% 70% / 60% 30% 70% 40%;
  animation: morph 8s ease-in-out infinite;
}

@keyframes morph {
  0%, 100% { border-radius: 60% 40% 30% 70% / 60% 30% 70% 40%; }
  25% { border-radius: 30% 60% 70% 40% / 50% 60% 30% 60%; }
  50% { border-radius: 50% 60% 30% 60% / 30% 40% 70% 50%; }
  75% { border-radius: 40% 50% 60% 50% / 60% 50% 40% 60%; }
}
```

**How it works:** Using 8-value `border-radius` creates asymmetric, organic shapes that transition smoothly.

---

### 2. Rotating Internal Waves

```css
.wave {
  position: absolute;
  width: 200%; height: 200%;
  background: rgba(255, 255, 255, 0.15);
  border-radius: 40%;
  animation: wave 4s linear infinite;
}

@keyframes wave {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
```

**How it works:** Oversized rotating elements with offset center create the illusion of internal liquid movement.

---

### 3. Gradient Color Cycling

```css
.orb {
  background: linear-gradient(135deg, #06b6d4, #8b5cf6, #ec4899);
  background-size: 200% 200%;
  animation: colorShift 6s ease-in-out infinite;
}

@keyframes colorShift {
  0%, 100% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
}
```

**How it works:** Oversized gradient + position animation creates smooth color transitions.

---

## 🎨 Color Palette

| Element | Color | Hex |
|---------|-------|-----|
| Cyan | Primary | `#06b6d4` |
| Purple | Secondary | `#8b5cf6` |
| Pink | Accent | `#ec4899` |
| Background | Dark | `#0a0a1a` |

---

## 📱 Browser Support

| Browser | Support |
|---------|---------|
| Chrome | ✅ Full |
| Firefox | ✅ Full |
| Safari | ✅ Full |
| Edge | ✅ Full |

---

## 🔗 Links

- **Live Demo:** [View Demo](https://sitharaj88.github.io/css-magic/2026/01/10-liquid-loader/)
- **Series:** CSS Magic
- **Author:** Sitharaj

---

**Made with 💜 using Pure CSS**
