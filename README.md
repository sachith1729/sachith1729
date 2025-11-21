
<p align="center">
  <!-- Animated gradient text + sparkles -->
  <svg width="100%" height="140" viewBox="0 0 1200 140" preserveAspectRatio="xMidYMid meet" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Sachith R">
    <defs>
      <linearGradient id="g" x1="0" x2="1">
        <stop offset="0" stop-color="#7b2ff7"/>
        <stop offset="0.5" stop-color="#ff6fd8"/>
        <stop offset="1" stop-color="#ffd54a"/>
      </linearGradient>

      <filter id="glow" x="-50%" y="-50%" width="200%" height="200%">
        <feGaussianBlur stdDeviation="6" result="b"/>
        <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
      </filter>

      <mask id="fade">
        <linearGradient id="mf" x1="0" x2="0" y1="0" y2="1">
          <stop offset="0" stop-color="#fff" stop-opacity="1"/>
          <stop offset="1" stop-color="#fff" stop-opacity="0.06"/>
        </linearGradient>
        <rect x="0" y="0" width="100%" height="100%" fill="url(#mf)"/>
      </mask>
    </defs>

    <!-- background subtle wave -->
    <rect width="100%" height="100%" fill="#071125" rx="10"/>

    <!-- sweeping gradient bar -->
    <rect x="-400" y="0" width="400" height="140" fill="url(#g)" opacity="0.12">
      <animate attributeName="x" from="-400" to="1400" dur="6s" repeatCount="indefinite" />
    </rect>

    <!-- Main name (gradient fill + glow) -->
    <text x="50%" y="68" text-anchor="middle" font-family="Segoe UI, Roboto, Helvetica, Arial, sans-serif" font-size="42" font-weight="800" fill="url(#g)" filter="url(#glow)">
      S A C H I T H &nbsp; R
    </text>

    <!-- Subtitle with shimmering -->
    <text x="50%" y="100" text-anchor="middle" font-family="Inter, system-ui, -apple-system, 'Segoe UI', Roboto" font-size="14" fill="#dbeafe" opacity="0.95">
      Frontend Wizard · ML Tinkerer · UI Lover ✨
    </text>

    <!-- sparkles -->
    <g>
      <circle cx="980" cy="24" r="3" fill="#fff" opacity="0.9">
        <animate attributeName="r" values="2;6;2" dur="2.8s" repeatCount="indefinite"/>
        <animate attributeName="opacity" values="0.2;1;0.2" dur="2.8s" repeatCount="indefinite"/>
      </circle>
      <circle cx="115" cy="36" r="2.2" fill="#fff" opacity="0.9">
        <animate attributeName="r" values="1.5;5;1.5" dur="3.2s" repeatCount="indefinite"/>
        <animate attributeName="opacity" values="0.1;0.9;0.1" dur="3.2s" repeatCount="indefinite"/>
      </circle>
    </g>
  </svg>
</p>

<p align="center">
  <strong style="font-size:14px">A little bit of code, a pinch of design, and a dash of magic ✨</strong>
</p>

---

## 🧭 Quick Snapshot
- 🎓 **4th semester** — BE (Computer Science & Design)  
- 💻 **Primary:** HTML · CSS · JavaScript · React · Next.js · PHP · MySQL · Python  
- 🔭 **Currently:** *Feel Free* (mental-health platform), Student Gig Platform, Deepfake Detection  
- 🌐 **Portfolio:** https://sachith.vercel.app/ · ✉️ **Email:** sachith2118@gmail.com

---

## 🚀 Projects (short & shiny)

| Project | Short |
|---|---|
| **Feel Free** | Interactive mental-health web app — assessments, resources, accessibility-first UI |
| **Student Gig Platform** | Student marketplace — PHP + MySQL with student/recruiter flows |
| **Deepfake Detection** | ResNeXt + LSTM prototype; dockerized Django UI for testing |

---

## 🧰 Tech Stack & Skills

**Frontend:** HTML5 · CSS3 · Tailwind · React · Next.js · Framer Motion · GSAP  
**Backend:** Node.js · Express · PHP · Django  
**DB:** MySQL · SQLite  
**ML / CV:** OpenCV · PyTorch  
**Other:** Git · Docker · XAMPP · Figma

---

## ✨ Animated Skill Bars (SVG)
*These are inline SVG bars — animated and pure code (no external images).*

<p align="center">
  <svg width="100%" height="110" viewBox="0 0 900 110" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Skill bars">
    <defs>
      <linearGradient id="skillGrad" x1="0" x2="1">
        <stop offset="0" stop-color="#7b2ff7"/><stop offset="1" stop-color="#ff6fd8"/>
      </linearGradient>
      <style><![CDATA[
        .label { font: 12px Inter, system-ui, -apple-system, 'Segoe UI', Roboto; fill: #dbeafe; }
        .muted { font: 11px Inter, system-ui; fill: #9aa6b2; }
      ]]></style>
    </defs>

    <!-- HTML -->
    <text x="8" y="18" class="label">HTML</text>
    <rect x="80" y="6" rx="8" ry="8" width="800" height="18" fill="#0f1724" opacity="0.9"></rect>
    <rect x="80" y="6" rx="8" ry="8" width="720" height="18" fill="url(#skillGrad)">
      <animate attributeName="width" from="0" to="720" dur="1.1s" begin="0.2s" fill="freeze"/>
    </rect>
    <text x="820" y="18" class="muted">90%</text>

    <!-- CSS/Anim -->
    <text x="8" y="44" class="label">CSS / Anim</text>
    <rect x="80" y="32" rx="8" ry="8" width="800" height="18" fill="#0f1724" opacity="0.9"></rect>
    <rect x="80" y="32" rx="8" ry="8" width="656" height="18" fill="url(#skillGrad)">
      <animate attributeName="width" from="0" to="656" dur="1.2s" begin="0.4s" fill="freeze"/>
    </rect>
    <text x="820" y="44" class="muted">82%</text>

    <!-- JS -->
    <text x="8" y="70" class="label">JavaScript</text>
    <rect x="80" y="58" rx="8" ry="8" width="800" height="18" fill="#0f1724" opacity="0.9"></rect>
    <rect x="80" y="58" rx="8" ry="8" width="600" height="18" fill="url(#skillGrad)">
      <animate attributeName="width" from="0" to="600" dur="1.3s" begin="0.6s" fill="freeze"/>
    </rect>
    <text x="820" y="70" class="muted">75%</text>

    <!-- Python -->
    <text x="8" y="96" class="label">Python / ML</text>
    <rect x="80" y="84" rx="8" ry="8" width="800" height="18" fill="#0f1724" opacity="0.9"></rect>
    <rect x="80" y="84" rx="8" ry="8" width="400" height="18" fill="url(#skillGrad)">
      <animate attributeName="width" from="0" to="400" dur="1.4s" begin="0.8s" fill="freeze"/>
    </rect>
    <text x="820" y="96" class="muted">50%</text>
  </svg>
</p>

---

## 🤝 Contribute to Me
I love collaboration — here's a friendly workflow:

1. ⭐ Star the repo you like  
2. 📝 Open an issue to propose large changes or discuss design  
3. 🔧 Fork → create branch `feature/your-idea` → implement  
4. 🧪 Add tests / screenshots where relevant  
5. 🗣️ Open a PR with a clear description and link related issues

**Good-first PR ideas**
- Add or improve README for small repos  
- Create a demo page for frontend projects  
- Add `good-first-issue` tasks for beginners

---

## 📫 Contact & Socials
- 🔗 Portfolio: https://sachith.vercel.app/  
- 💼 LinkedIn: https://www.linkedin.com/in/sachith-r-abab73254/  
- 🐙 GitHub: https://github.com/sachith1729  
- ✉️ Email: sachith2118@gmail.com

---

## 🪄 Little Easter — copyable mini card
