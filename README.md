# 🌌 My First Website

> A multi-layered scroll-parallax landing page — the very first thing I ever built, from scratch, with plain HTML, CSS and JavaScript. No frameworks, no libraries, no build step.

<p align="left">
  <img alt="HTML5" src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white">
  <img alt="CSS3" src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white">
  <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black">
  <img alt="No dependencies" src="https://img.shields.io/badge/dependencies-none-success?style=for-the-badge">
</p>

**🔗 Live demo:** https://icexchange22-prog.github.io/my-first-website/

---

## ✨ What it does

Three full-screen sections, each layered from separate PNG cut-outs that move at different speeds as you scroll — the classic parallax depth effect, hand-wired with a single `scroll` listener.

| Section | Effect |
| --- | --- |
| **Home** | A night city skyline in 8 layers. The moon drifts down, a train slides across the rails, and the headline floats upward as you scroll. |
| **About** | A desert scene with a waterfall. The desert moon and the walking man move independently of the background. |
| **Products** | A card grid with hover lift, glow shadows and neon-outline buttons. |

Plus a **circular scroll-progress button** in the bottom-right that fills up with a `conic-gradient` as you read, and scrolls you back to the top on click.

## 🛠️ How it's built

- **Parallax** — every layer is an absolutely positioned `<img>`; on scroll, `window.scrollY` is multiplied by a different factor per layer and applied to `top` / `left`. Higher multiplier = closer to the viewer.
- **Moon glow** — `mix-blend-mode: screen` blends the moon PNG into the sky instead of sitting on top of it as a hard rectangle.
- **Progress ring** — the scroll percentage is fed straight into a `conic-gradient()` so the ring fills without any SVG or canvas.
- **Styling** — pure CSS: flexbox layout, custom scrollbar, cyan neon accent (`#12f7ff`) on a deep purple base (`#1d002c`), and `transition` based hover states.

## 📁 Project structure

```
.
├── index.html          # page markup — all three sections
├── style.css           # all styling
├── script.js           # parallax scroll logic + progress ring
├── Home-Images/        # 10 layered PNGs for the city scene
├── About-Images/       # 9 layered PNGs for the desert scene
├── products/           # product images
└── img/                # misc assets
```

## 🚀 Run it locally

No install, no build — just clone and open:

```bash
git clone https://github.com/icexchange22-prog/my-first-website.git
cd my-first-website
```

Then open `index.html` in your browser.

Or serve it (recommended, so relative paths behave exactly like they do live):

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## 🎨 Credits

- Fonts — [Poppins](https://fonts.google.com/specimen/Poppins) via Google Fonts
- Icons — [Boxicons](https://boxicons.com/)

## 📄 License

[MIT](LICENSE) © Ajay
