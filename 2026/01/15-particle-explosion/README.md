# 💥 Day 5: Particle Explosion Hover

A stunning CSS-only particle explosion effect that triggers on hover. Particles burst outward in all directions with neon glow trails and staggered timing for a natural explosion feel.

## ✨ Features

- **12 Animated Particles**: Burst outward in 360° directions on hover
- **Neon Glow Effects**: Vibrant colors with CSS box-shadow glow trails
- **Staggered Timing**: Natural explosion feel with varied animation delays
- **Pulse Rings**: Expanding shockwave rings accompany the explosion
- **Cosmic Background**: Animated starfield with gradient nebula
- **Pure CSS**: No JavaScript required!

## 🚀 Technical Highlights

- **CSS Custom Properties**: `--angle` and `--distance` for dynamic particle trajectories
- **Trigonometric Functions**: `cos()` and `sin()` in CSS for radial positioning
- **Keyframe Animations**: Multi-stage explosion with scale and opacity transitions
- **Conic Gradients**: Rotating rainbow border on trigger element
- **Backdrop Filter**: Frosted glass effect on the trigger orb

## 🛠️ Usage

Simply open `index.html` in any modern browser to view the particle explosion.

```bash
open index.html
```

Hover over the central orb to trigger the explosion effect!

## 📜 CSS Techniques Used

1. **Radial Particle Animation**
   ```css
   transform: translate(
       calc(cos(var(--angle)) * var(--distance)),
       calc(sin(var(--angle)) * var(--distance))
   );
   ```

2. **Staggered Animation Delays**
   ```css
   .particle:nth-child(1) { animation-delay: 0ms; }
   .particle:nth-child(2) { animation-delay: 20ms; }
   /* ... */
   ```

3. **Neon Glow Box Shadows**
   ```css
   box-shadow: 0 0 15px var(--color), 0 0 30px var(--color);
   ```
