# 🎚️ DiffSlider – Interactive Before & After Image Comparison Slider

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Website](https://img.shields.io/badge/Website-diffslider.app-0ea5e9?style=flat&logo=safari)](https://diffslider.app)


> ⚡ **The fastest, cleanest, zero-dependency interactive Before/After image slider.**  
> Create, compare, and embed 60fps responsive sliders in under 10 seconds. 

🌐 **Official Online Generator**: [https://diffslider.app](https://diffslider.app)

---

## ✨ Features

- 🚀 **Zero Dependencies**: Lightweight, clean vanilla HTML/CSS/JS with zero runtime overhead.
- 🎚️ **Fluid 60FPS Controls**: Touch-friendly, smooth dragging on mobile, tablets, and desktop.
- 📐 **Universal Responsiveness**: Auto-scales to any viewport or aspect ratio (16:9, 4:3, square, portrait).
- 🎨 **Multiple Modes**: Classic Split Slider, Side-by-Side Sync, Vertical Split, and Fade Comparison.
- 🌍 **Instant Embed**: Drop one line of code into Shopify, Webflow, WordPress, Ghost, React, or Vue.
- 🔒 **Privacy-First**: No tracking, fast edge-cached delivery.

---

## 🚀 Quick Start (1-Minute Embed)

### Option 1: Using the Cloud-Hosted Widget (Zero Setup)

You can generate any slider instantly using the free online creator at [diffslider.app](https://diffslider.app). Then, simply copy & paste the responsive `iframe`:

```html
<iframe
  src="https://diffslider.app/embed/demo-ai-upscale"
  width="100%"
  height="500"
  style="border: none; border-radius: 12px; overflow: hidden;"
  loading="lazy"
  allowfullscreen
></iframe>
```

---

### Option 2: Pure Vanilla HTML/CSS/JS (Standalone)

Want complete offline control? Here is the minimalist implementation:

```html
<!-- Container -->
<div class="diff-container" id="my-slider">
  <img src="after.jpg" alt="After" class="diff-img diff-after" />
  <div class="diff-overlay">
    <img src="before.jpg" alt="Before" class="diff-img diff-before" />
  </div>
  <input type="range" min="0" max="100" value="50" class="diff-slider" />
</div>

<style>
  .diff-container {
    position: relative;
    width: 100%;
    max-width: 800px;
    aspect-ratio: 16 / 9;
    overflow: hidden;
    border-radius: 12px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.15);
  }
  .diff-img {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    pointer-events: none;
  }
  .diff-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 50%;
    height: 100%;
    overflow: hidden;
  }
  .diff-slider {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    opacity: 0;
    cursor: ew-resize;
    z-index: 10;
  }
</style>

<script>
  const container = document.getElementById('my-slider');
  const slider = container.querySelector('.diff-slider');
  const overlay = container.querySelector('.diff-overlay');

  slider.addEventListener('input', (e) => {
    overlay.style.width = `${e.target.value}%`;
  });
</script>
```

---

## 🎯 Popular Use Cases

- **AI Generation & Upscaling**: Benchmark Midjourney, Stable Diffusion, Flux, and Magnific AI enhancements.
- **Photography & Color Grading**: Showcase RAW flat profiles vs cinematic color treatments.
- **E-Commerce & Retouching**: Product restoration, jewelry cleaning, and apparel details on Shopify/Amazon.
- **Architecture & 3D Staging**: Wireframe CAD models vs photorealistic ray-traced interiors.
- **Aesthetic & Clinical**: Dental veneers, teeth whitening, skincare, and hair restoration proofs.

Explore over 50+ interactive case studies at [diffslider.app/explore](https://diffslider.app/explore).

---

## 🛠️ Tech Stack & Philosophy

DiffSlider is crafted with performance and simplicity in mind:
- **Framework**: Astro 5 (Server-driven, Zero client-side bloat)
- **Edge Runtime**: Cloudflare Workers, KV, and D1 database
- **Styling**: Tailwind CSS
- **Payments**: Stripe Radar + Customer Portal

Read our full guide on how to build high-performance image sliders:  
👉 [Interactive Before/After Slider Complete Guide](https://diffslider.app/blog/interactive-before-after-slider-complete-guide)

---

## 📄 License

This project is open-source under the [MIT License](LICENSE).

Made with ❤️ by [DiffSlider](https://diffslider.app).
