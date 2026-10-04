# Corolla — Generative Art

> A seed-based generative system for layered petal compositions.  
> A reproducible catalogue of computational textile compositions.

---

## What is this?

**Corolla** is a generative design system that draws four to fifteen concentric petal rings around a central radius. Each ring has its own hue path, its own stroke weight, its own noise scale, and one of three petal styles: smooth, spiky, or dashed. The rings overlap, the colours blur, and the composition resolves as a soft vibration of petals rather than a drawing.

Every artwork in this catalogue is defined by a single numeric seed. The same seed always produces the identical composition — making each piece **traceable, reproducible, and licensable** across textile, print, and apparel applications.

Named for the botanical term for the ring of petals around a flower's centre — the part of the bloom that is actually drawn here — **Corolla** translates that structure into code.

---

## Live

🌐 **[View the catalogue →](https://reyrove.github.io/Corolla-Generative-Art/)**

---

## The System

The generator combines three layers:

| Layer | Description |
|-------|-------------|
| **Petals** | Four to fifteen concentric rings, each drawn in one of three petal styles. |
| **Noise** | Perlin noise warps each petal out of a circle into a living, wobbling edge. |
| **Overlays** | Optional radial gradient, inner polygon pattern, floating particles, and decorative dashed frame. |

All three layers are driven by the same seed, ensuring deterministic output.

### Parameters

- **Base radius** — 20% to 42% of canvas width
- **Petals** — 5 to 20 per ring
- **Layers** — 4 to 15 concentric rings
- **Petal style** — smooth, spiky, or dashed, chosen per layer
- **Stroke weight** — 0.08% to 0.4% of canvas, per layer
- **Hue path** — narrow cool band or full-spectrum drift
- **Wobble** — 0.1 to 0.9 amplitude
- **Distortion** — 0 to 0.3 amplitude, applied in 50% of seeds

---

## Structure

```
Corolla-Generative-Art/
├── index.html          ← Full catalogue (single-file)
├── images/
│   ├── fav.svg
│   ├── tote.png
│   ├── tee.png
│   └── cushion.png
└── README.md
```

The entire project is contained in a single `index.html` — no build step, no framework. Open it in any modern browser.

---

## Features

- **Seed-based generation** — every composition is deterministic and reproducible
- **Three petal styles** — smooth, spiky, and dashed curves, mixed within a single piece
- **Optional overlays** — radial gradient, inner pattern, floating particles, decorative frame
- **Live catalogue** — cover, plate, surfaces, process, archive, commission sections
- **Multiple surfaces** — print, scarf, textile, wallpaper — all rendered from the same seed
- **Archive of 8 seeds** — click any plate to load it into the main view
- **PNG export** — download any composition directly from the browser
- **Keyboard shortcuts** — `R` for new seed, `S` to save
- **Legal modal** — licensing, terms, and credits built in
- **Responsive** — works on desktop, tablet, and mobile
- **Mobile-first navbar** — horizontally scrollable with fade hint

---

## Usage

### Generate a new composition

Click **New Seed** or press `R`.

### Download the current composition

Click **Download** or press `S`.

### Load a seed from the archive

Click any plate in the **Archive** section.

---

## Colour System

Each composition is drawn in HSB and each layer takes its own path through the spectrum:

| Element | Range |
|---------|-------|
| **Background** | Near-black, cool dark, or warm dark — drawn per seed |
| **Layer hue** | Narrow cool band (180–280) or full-spectrum drift, chosen per layer |
| **Saturation** | 60% to 90% |
| **Brightness** | 80% to 100% |
| **Alpha** | 30 to 80 |
| **Particles** | Full-spectrum hue, 50–80% saturation, 70–100% brightness |
| **Radial gradient** | Cool (200–300) or warm (0–60), low saturation, low brightness |

The result reads as luminous petals above a deep, coloured ground — the strokes glow rather than sit on the surface.

---

## Technical Notes

- p5.js 1.9.0 (CDN) for canvas rendering
- Custom seeded random generator for deterministic output
- HSB colour mode, RADIANS angle mode, per-instance
- `noiseSeed()` reset per tile so repeats agree
- Smooth and dashed petals use `curveVertex` for continuous curves
- Spiky petals use straight `vertex` calls for a sharp-edged silhouette
- Rectangular surfaces tile the square composition to fill aspect ratio

---

## About

**Corolla** is a project by [Reyhaneh Daneshdoost](https://reyrove.github.io/) — an Iranian-born artist working at the intersection of classical textile logic and generative systems.

The work begins with a simple observation: the woven surface — repetitive, mathematically structured, infinitely variable — has always been a form of computation, long before computers.

**Corolla** is an attempt to render that logic visible.

> *A circle pushed by noise becomes a petal, and a petal repeated becomes a corolla.*

---

## Licensing

All compositions are seed-documented and available for licensing across textile, surface, and apparel applications.

For commercial use, custom editions, or exclusive rights:

📧 **reyhanehdaneshdoost@gmail.com**

See the **Licensing** section in the live catalogue for details.

---

## Links

- 🌐 [Website](https://reyrove.github.io/)
- 📷 [Instagram](https://www.instagram.com/rey._.rove/)
- 💼 [LinkedIn](https://www.linkedin.com/in/reyhaneh-daneshdoost-730481160/)
- 🐦 [X](https://x.com/reyrove)

---

## Credits

**Design & Generative System**  
Reyhaneh Daneshdoost

**Typefaces**  
Cormorant Garamond · DM Mono

**Edition**  
Corolla — Autumn 2026

---

<p align="center">
  <em>Computational Textile Design</em><br />
  <sub>© Reyrove Studio · All compositions reproducible by seed</sub>
</p>