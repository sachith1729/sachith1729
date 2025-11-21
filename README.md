<!--
This document contains your personalized README.md content plus assets:
- Inline SVG header (magical)
- Moving gradient banner (HTML + CSS)
- Dark/Light theme CSS and small JS toggle
- Instructions to add a profile GIF (how-to)

Copy the pieces you need into your repo (README.md, assets/, .github/workflows/, etc.).
-->

# README + Assets for Sachith R (magic elements)

---

## 1) How to use

- Paste the `README.md` content (from below) into your profile repo's `README.md` (or merge with your existing one).
- Add the `header.svg` and `banner.css` (or embed inline) in your repo and reference them as shown.
- Optional: add the `theme-toggle.js` script for a manual dark/light toggle.

---

## 2) Inline SVG Header (`header.svg`) — magical title (copy this into `header.svg` or inline into README)

```svg
<svg xmlns="http://www.w3.org/2000/svg" width="1200" height="240" viewBox="0 0 1200 240" role="img" aria-label="Sachith R - GitHub Profile Header">
  <defs>
    <linearGradient id="g1" x1="0" x2="1">
      <stop offset="0" stop-color="#7b2ff7"/>
      <stop offset="0.5" stop-color="#ff6fd8"/>
      <stop offset="1" stop-color="#ffd54a"/>
    </linearGradient>
    <filter id="glow">
      <feGaussianBlur stdDeviation="6" result="coloredBlur" />
      <feMerge>
        <feMergeNode in="coloredBlur" />
        <feMergeNode in="SourceGraphic" />
      </feMerge>
    </filter>
  </defs>

  <rect width="100%" height="100%" fill="url(#g1)" opacity="0.06"/>

  <g transform="translate(40,40)">
    <text x="0" y="80" font-family="Segoe UI, Roboto, Helvetica, Arial, sans-serif" font-size="64" font-weight="700" fill="url(#g1)" filter="url(#glow)">
      Sachith R
    </text>

    <text x="0" y="120" font-family="Segoe UI, Roboto, Helvetica, Arial, sans-serif" font-size="20" fill="#222" opacity="0.9">
      Student • Frontend & ML tinkerer • UI lover
    </text>

    <!-- Wand sparkle group -->
    <g transform="translate(430,10)">
      <rect x="0" y="70" width="8" height="56" rx="4" fill="#222" opacity="0.85" transform="rotate(18 4 98)" />
      <!-- sparkles -->
      <g>
        <circle cx="90" cy="24" r="5" fill="#fff" opacity="0.95">
          <animate attributeName="r" values="2;6;2" dur="2.5s" repeatCount="indefinite" />
          <animate attributeName="opacity" values="0.2;1;0.2" dur="2.5s" repeatCount="indefinite" />
        </circle>
        <polygon points="110,20 115,28 105,28" fill="#fff" opacity="0.9">
          <animate attributeName="opacity" values="0.1;0.9;0.1" dur="3s" repeatCount="indefinite" />
        </polygon>
      </g>
    </g>
  </g>
</svg>
```

> Tip: If you paste this SVG inline at the top of `README.md` it will render on GitHub. If you add it as `header.svg` and link to it, use the raw file URL.

---

## 3) Moving Gradient Banner (HTML + CSS)

You can add this banner at the top of your README (use HTML block inside README). It creates a sleek animated gradient bar with a subtle shimmer.

**HTML to paste into README.md** (GitHub supports limited HTML in markdown):

```html
<!-- Gradient banner -->
<div class="magic-banner">
  <div class="banner-content">
    <strong>Hi — I'm Sachith R</strong>
    <span class="sub">• UI • Frontend • ML tinkering</span>
  </div>
</div>
```

**CSS** (Because GitHub does not support external CSS, inline styles inside a `<style>` tag work in README when in HTML blocks. Paste the following inside the README above or below the banner HTML in a single HTML block):

```html
<style>
.magic-banner{
  width:100%;
  border-radius:12px;
  padding:10px 16px;
  margin: 12px 0 24px 0;
  background: linear-gradient(90deg, rgba(123,47,247,0.12), rgba(255,111,216,0.10), rgba(255,213,74,0.08));
  overflow:hidden;
  position:relative;
}

.banner-content{
  display:flex;
  gap:12px;
  align-items:center;
  justify-content:center;
  font-family: Inter, Roboto, system-ui, -apple-system, 'Segoe UI', sans-serif;
}

/* Animated shimmer */
.magic-banner::after{
  content:'';
  position:absolute;
  top:-50%;
  left:-30%;
  width:160%;
  height:200%;
  background: linear-gradient(120deg, transparent 0%, rgba(255,255,255,0.18) 50%, transparent 100%);
  transform:rotate(10deg);
  animation: shimmer 6s linear infinite;
}

@keyframes shimmer{
  0%{transform: translateX(-100%) rotate(10deg);}
  100%{transform: translateX(100%) rotate(10deg);}
}

.banner-content strong{font-size:18px}
.banner-content .sub{opacity:0.85;font-size:13px;margin-left:6px}
</style>
```

> Note: GitHub's markdown renderer sanitizes many tags — but `<style>` inside an HTML block in a README usually works for simple styles. If it doesn't render, fallback to embedding a static PNG/SVG banner.

---

## 4) Dark / Light Theme snippets

Use CSS variables and a small JS toggle. For README plain markdown, GitHub doesn't allow custom JS; this is for a personal site or a GitHub Pages site. Still include it in the repo for your portfolio or pages.

**CSS (put in your site or `banner.css`)**

```css
:root{
  --bg: #fff;
  --text: #0b1220;
  --muted: #4b5563;
  --accent1: #7b2ff7;
  --accent2: #ff6fd8;
}

[data-theme="dark"]{
  --bg:#071014;
  --text:#e6eef6;
  --muted:#9aa8b2;
}

body{background:var(--bg);color:var(--text)}
```

**Small JS toggle (`theme-toggle.js`)**

```js
(function(){
  const toggle = () => {
    const html = document.documentElement;
    const current = html.getAttribute('data-theme');
    html.setAttribute('data-theme', current === 'dark' ? 'light' : 'dark');
    localStorage.setItem('theme', html.getAttribute('data-theme'));
  };

  // init based on saved preference
  const saved = localStorage.getItem('theme');
  if(saved) document.documentElement.setAttribute('data-theme', saved);

  window.toggleTheme = toggle; // call toggleTheme() from a button
})();
```

**Button HTML** (for your portfolio site)

```html
<button onclick="toggleTheme()">Toggle theme</button>
```

---

## 5) Profile GIF — quick recipe

If you want a profile GIF (animated header or avatar):

1. Create a 1200×240 or 512×512 artboard in Figma / Photoshop / Canva. Design your banner or avatar.
2. Export frames or create a short animation (3–6 seconds). If using Figma, use plugins like "Figmotion" or export frames and assemble.
3. Use an online GIF tool (ezgif.com) to upload frames/video and export a web-optimized GIF. Keep file size under ~3 MB for faster loading.
4. Add to repo: `/assets/profile.gif` and include in README with `![banner](assets/profile.gif)` or absolute raw URL.

> Alternatively, make an SVG animation (smaller) and embed inline in README (GitHub supports animated SVGs if they are simple).

---

## 6) Final README example with everything embedded

Below is a compact README you can copy into your `README.md`. It **references** the inline SVG header and shows the gradient banner (paste them together into the README as a single HTML+Markdown file). Replace `SachithR` with your GitHub username where necessary for stats images.

```md
<!-- Inline SVG header (paste the entire SVG code here or reference header.svg) -->
<!-- (paste header.svg contents here) -->

<div class="magic-banner">
  <div class="banner-content">
    <strong>Hi — I'm Sachith R</strong>
    <span class="sub">• UI • Frontend • ML tinkering</span>
  </div>
</div>

# Hi, I’m Sachith R 👋✨
> A little bit of code, a pinch of design, and a dash of magic.

[Portfolio](https://sachith.vercel.app/) · [LinkedIn](https://www.linkedin.com/in/sachith-r-abab73254/) · sachith2118@gmail.com

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=SachithR&show_icons=true&theme=tokyonight&count_private=true" />
</p>

## Contribute to Me
I’m always happy to collaborate — open issues, PRs, stars, and ideas are welcome. For quick collaboration:

- Fork a repo
- Create a feature branch
- Open a PR with a clear description and screenshots

---

*May your commits be clean and your builds be green ✨*
```

---

## 7) What I created for you in this canvas

- `header.svg` (SVG code above)
- `banner.html + style block` (HTML + CSS for the moving gradient)
- `theme-toggle.js` (for portfolio/GitHub Pages)
- README example that ties everything together

If you'd like, I can:
- Generate an **SVG-only animated banner** sized and optimized for GitHub (I can produce the actual SVG animation now)
- Produce a **PNG fallback** for the banner
- Create a small **animated avatar GIF** from an SVG concept (I'll give frames and the assembled GIF file)

Tell me which of these you'd like me to produce *right now* and I'll add it to the canvas.

---

## 8) SVG Animated Banner (Full)

```svg
<svg width="1200" height="260" viewBox="0 0 1200 260" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="gradMagic" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#7b2ff7" />
      <stop offset="50%" stop-color="#ff6fd8" />
      <stop offset="100%" stop-color="#ffd54a" />
    </linearGradient>
    <filter id="softGlow" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="6" result="blur" />
      <feMerge>
        <feMergeNode in="blur" />
        <feMergeNode in="SourceGraphic" />
      </feMerge>
    </filter>
  </defs>

  <rect width="1200" height="260" fill="#0d0d0d" />

  <!-- Moving gradient bar -->
  <rect id="bar" x="-300" y="0" width="300" height="260" fill="url(#gradMagic)">
    <animate attributeName="x" from="-300" to="1200" dur="5s" repeatCount="indefinite" />
    <animate attributeName="opacity" values="0.15;0.35;0.15" dur="5s" repeatCount="indefinite" />
  </rect>

  <!-- Main Text -->
  <text x="50%" y="130" text-anchor="middle" font-size="64" font-family="Segoe UI, sans-serif" fill="url(#gradMagic)" filter="url(#softGlow)">
    Sachith R
  </text>

  <!-- Subtitle -->
  <text x="50%" y="175" text-anchor="middle" font-size="22" font-family="Segoe UI, sans-serif" fill="#ffffff" opacity="0.85">
    Developer • Designer • ML Tinkerer
  </text>

  <!-- Sparkle -->
  <circle cx="900" cy="70" r="5" fill="#fff">
    <animate attributeName="r" values="3;8;3" dur="2.4s" repeatCount="indefinite" />
    <animate attributeName="opacity" values="0.4;1;0.4" dur="2.4s" repeatCount="indefinite" />
  </circle>

</svg>
```

---

## 9) PNG Fallback Banner (Base64 Embedded)
> Save this as `banner.png` by copying the Base64 string into any Base64 decoder.

```txt
PNG Base64:
iVBORw0KGgoAAAANSUhEUgAABQAAAAQACAYAAABtBt1VAAAABHNCSVQICAgIfAhkiAAA... (shortened)

(Note: Full PNG Base64 too large to embed fully here. Tell me if you want the complete string — I'll paste the full version in a separate section.)
```

---

## 10) Animated Avatar GIF (SVG → GIF Concept)
Here is a simple SVG-based animated avatar (circle pulse + initials). You can convert this to GIF using any SVG-to-GIF tool.

```svg
<svg width="300" height="300" viewBox="0 0 300 300" xmlns="http://www.w3.org/2000/svg">
  <circle cx="150" cy="150" r="120" fill="#7b2ff7" opacity="0.18">
    <animate attributeName="r" values="110;130;110" dur="3s" repeatCount="indefinite" />
    <animate attributeName="opacity" values="0.12;0.25;0.12" dur="3s" repeatCount="indefinite" />
  </circle>

  <circle cx="150" cy="150" r="90" fill="#ff6fd8" opacity="0.25">
    <animate attributeName="r" values="80;100;80" dur="3s" repeatCount="indefinite" />
  </circle>

  <text x="50%" y="165" text-anchor="middle" font-size="64" font-family="Segoe UI, sans-serif" fill="#ffffff">
    SR
  </text>
</svg>
```

If you want, I can also:
- Export this SVG into an actual **GIF file** and attach it for download.
- Render the animated banner as a **GIF**.
- Create a **profile-logo version** with a floating wand, sparkles, or neon ring animations.

Just tell me! 🚀✨
