<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Sachith R — Profile Utility</title>
  <meta name="description" content="Sachith R — Frontend & ML tinkerer. Portfolio, projects, contact." />
  <style>
    :root{
      --bg:#0b1020; --card:#0f1724; --muted:#9aa6b2;
      --accent1:#7b2ff7; --accent2:#ff6fd8; --accent3:#ffd54a;
      --glass: rgba(255,255,255,0.03); --radius:14px; --text:#e6eef6;
      --sans: system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    [data-theme="light"]{
      --bg:#f7fbff; --card:#ffffff; --muted:#4b5563; --text:#071125;
      --accent1:#5b21b6; --accent2:#db2777; --accent3:#d97706;
    }
    *{box-sizing:border-box} html,body{height:100%}
    body{
      margin:0; font-family:var(--sans); background:linear-gradient(180deg,var(--bg),rgba(11,16,32,0.92));
      color:var(--text); padding:24px; transition:background .35s ease,color .35s ease;
    }
    .container{max-width:1100px;margin:0 auto;display:grid;grid-template-columns:1fr 360px;gap:24px}
    @media (max-width:980px){.container{grid-template-columns:1fr;padding:0 12px}}
    header{grid-column:1 / -1;display:flex;justify-content:space-between;align-items:center;gap:12px;margin-bottom:6px}
    .title{display:flex;gap:12px;align-items:center}
    .badge-wand{width:64px;height:64px;border-radius:12px;background:linear-gradient(135deg,rgba(123,47,247,0.18),rgba(255,111,216,0.12));display:grid;place-items:center}
    h1{margin:0;font-size:20px}
    p.lead{margin:.25rem 0 0 0;color:var(--muted);font-size:13px}
    .meta{display:flex;gap:10px;align-items:center}
    button.icon-btn{background:var(--glass);border:1px solid rgba(255,255,255,0.02);padding:8px 12px;border-radius:10px;color:var(--text);cursor:pointer;font-weight:700;display:inline-flex;gap:8px;align-items:center}
    .card{background:linear-gradient(180deg,rgba(255,255,255,0.01),rgba(255,255,255,0.00));border-radius:12px;padding:16px;border:1px solid rgba(255,255,255,0.03)}
    .hero{display:flex;gap:18px;padding:18px;border-radius:12px}
    .hero-left{flex:1}
    .hero-right{width:320px;display:flex;flex-direction:column;gap:12px}
    .skill-pill{display:inline-flex;gap:8px;padding:8px 10px;border-radius:999px;background:rgba(255,255,255,0.02);font-weight:700;font-size:13px;color:var(--muted)}
    .proj{padding:12px;border-radius:10px;border:1px solid rgba(255,255,255,0.03);background:transparent}
    .projects{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:12px}
    .muted{color:var(--muted);font-size:13px}
    .bar{height:12px;border-radius:999px;background:linear-gradient(90deg,rgba(255,255,255,0.02),rgba(255,255,255,0.01));overflow:hidden;border:1px solid rgba(255,255,255,0.02)}
    .bar > i{display:block;height:100%;width:0%;border-radius:999px;background:linear-gradient(90deg,var(--accent1),var(--accent2));transition:width .9s cubic-bezier(.2,.9,.2,1)}
    .link-chip{display:inline-flex;align-items:center;gap:8px;padding:8px 12px;border-radius:999px;background:linear-gradient(90deg,rgba(255,255,255,0.01),rgba(255,255,255,0.00));border:1px solid rgba(255,255,255,0.03);text-decoration:none;color:var(--text);font-weight:700}
    .pill{padding:6px 10px;border-radius:999px;background:linear-gradient(90deg,var(--accent1),var(--accent2));color:white;font-weight:700;font-size:13px}
    footer{grid-column:1/-1;margin-top:18px;opacity:.95}
    .copy-btn{background:transparent;border:1px dashed rgba(255,255,255,0.04);padding:8px 12px;border-radius:10px;font-family:monospace;font-weight:700;cursor:pointer;color:var(--text)}
  </style>
</head>
<body>
  <div class="container" id="app">
    <header>
      <div class="title">
        <span class="badge-wand" aria-hidden="true">
          <svg viewBox="0 0 24 24" width="36" height="36" fill="none"><rect x="9" y="2" width="6" height="12" rx="2" fill="white" opacity="0.9" transform="rotate(18 12 8)"></rect><circle cx="18.5" cy="4.5" r="2" fill="white" opacity="0.95"/></svg>
        </span>
        <div>
          <h1>Sachith R <span style="font-size:12px;color:var(--muted);font-weight:700">· Frontend • ML tinkerer</span></h1>
          <p class="lead">I build clean UIs, playful interactions, and experiment with ML for real-world problems.</p>
        </div>
      </div>

      <div class="meta">
        <button id="theme-toggle" class="icon-btn" aria-pressed="false" title="Toggle theme (T)"><span id="theme-label">Dark</span></button>
        <a class="icon-btn" href="https://sachith.vercel.app/" target="_blank" rel="noopener noreferrer">Portfolio</a>
        <a class="icon-btn" href="mailto:sachith2118@gmail.com">Email</a>
      </div>
    </header>

    <main>
      <section class="card hero" aria-label="Hero">
        <div class="hero-left">
          <div style="display:flex;gap:10px;flex-wrap:wrap">
            <span class="skill-pill">✨ <strong>Frontend</strong></span>
            <span class="skill-pill">🛰️ <strong>ML/CV</strong></span>
            <span class="skill-pill">🗄️ <strong>Backend</strong></span>
          </div>

          <h2 style="margin-top:14px;margin-bottom:6px">Projects & Highlights</h2>
          <div class="projects" style="margin-top:6px">
            <article class="proj"><h4>Feel Free</h4><p class="muted">Mental-health support platform with interactive assessments & resources.</p></article>
            <article class="proj"><h4>Student Gig Platform</h4><p class="muted">Marketplace for student gigs — PHP + MySQL starter with dashboards.</p></article>
            <article class="proj"><h4>Deepfake Detection</h4><p class="muted">ResNeXt + LSTM prototype; dockerized Django UI.</p></article>
          </div>

          <div style="margin-top:18px;display:flex;gap:12px;flex-wrap:wrap">
            <button class="icon-btn" onclick="scrollToSection('contribute')">🤝 Contribute</button>
            <button class="icon-btn" onclick="generateREADME()">📄 Export README</button>
            <button class="icon-btn" onclick="copyToClipboard('sachith2118@gmail.com')">📧 Copy Email</button>
          </div>

          <hr style="border:none;height:1px;background:linear-gradient(90deg, transparent, rgba(255,255,255,0.03), transparent);margin:18px 0">

          <h3 style="margin:0 0 10px 0">Skills</h3>
          <div style="margin-bottom:8px"><div class="muted">HTML <span style="float:right">90%</span></div><div class="bar"><i style="width:90%"></i></div></div>
          <div style="margin-bottom:8px"><div class="muted">CSS / Animations <span style="float:right">82%</span></div><div class="bar"><i style="width:82%"></i></div></div>
          <div style="margin-bottom:8px"><div class="muted">JavaScript <span style="float:right">75%</span></div><div class="bar"><i style="width:75%"></i></div></div>
          <div style="margin-bottom:8px"><div class="muted">React / Next <span style="float:right">70%</span></div><div class="bar"><i style="width:70%"></i></div></div>
          <div style="margin-bottom:8px"><div class="muted">Python / ML <span style="float:right">50%</span></div><div class="bar"><i style="width:50%"></i></div></div>
        </div>

        <aside class="hero-right">
          <div class="card">
            <div class="muted">NAME</div>
            <div style="font-weight:800">Sachith R</div>
            <div class="muted" style="margin-top:8px">4th semester BE — Computer Science & Design</div>
          </div>

          <div class="card">
            <div class="muted">Contact</div>
            <div style="margin-top:8px;display:flex;flex-direction:column;gap:8px">
              <a class="link-chip" href="https://sachith.vercel.app/" target="_blank">Portfolio</a>
              <a class="link-chip" href="https://www.linkedin.com/in/sachith-r-abab73254/" target="_blank">LinkedIn</a>
              <a class="link-chip" href="https://github.com/sachith1729" target="_blank">GitHub</a>
              <button class="link-chip" onclick="copyToClipboard('sachith2118@gmail.com')">📧 Copy Email</button>
            </div>
          </div>

          <div class="card" id="contribute">
            <div style="display:flex;justify-content:space-between;align-items:center"><div style="font-weight:800">Contribute to me</div><div class="pill">Good first PRs</div></div>
            <div style="font-size:13px;color:var(--muted);margin-top:8px">I love collaboration — here's a simple flow:</div>
            <ul style="margin:10px 0 0 18px;color:var(--muted)">
              <li>⭐ Star a repo you like</li>
              <li>📝 Open an issue to propose changes</li>
              <li>🔧 Fork → create <code>feature/your-idea</code> → PR</li>
              <li>🧪 Add tests / screenshots if relevant</li>
              <li>🗣️ Write clear PR description & link issues</li>
            </ul>
          </div>
        </aside>
      </section>

      <section class="card" style="margin-top:16px"><h3 style="margin:0 0 10px 0">Why I care about UX & ML</h3><p class="muted">Good interfaces amplify human ability. ML should assist, not confuse. I focus on sane defaults, clear feedback, and delightful micro-interactions.</p></section>

      <section class="card" style="margin-top:16px"><h3 style="margin:0 0 10px 0">Quick Links</h3><div style="display:flex;gap:10px;flex-wrap:wrap"><a class="link-chip" href="https://github.com/sachith1729" target="_blank">GitHub</a><a class="link-chip" href="https://sachith.vercel.app/">Portfolio</a><a class="link-chip" href="mailto:sachith2118@gmail.com">Email</a></div></section>
    </main>

    <aside>
      <div class="card" style="display:flex;flex-direction:column;gap:12px">
        <div><div class="muted">PROFILE</div><div style="font-weight:800">Sachith R</div><div class="muted">Frontend • ML tinkerer • UI lover</div></div>
        <div><div class="muted">Location</div><div style="font-weight:700">India</div></div>
        <div><div class="muted">Status</div><div style="margin-top:8px"><div class="tag">Open to collaborate</div></div></div>
        <div><div class="muted">Contact</div><div style="display:flex;gap:8px;margin-top:8px"><button class="copy-btn" onclick="copyToClipboard('sachith2118@gmail.com')">Copy Email</button><a class="copy-btn" href="https://github.com/sachith1729" target="_blank">GitHub</a></div></div>
      </div>

      <div class="card" style="margin-top:12px"><div style="display:flex;justify-content:space-between;align-items:center"><div style="font-weight:800">Mini Checklist</div><div class="muted" style="font-size:12px">Make a PR</div></div><ol style="margin:10px 0 0 18px;color:var(--muted)"><li>Fork repo</li><li>Create <code>feature/your-idea</code></li><li>Write code & tests</li><li>Open PR → link issue</li></ol></div>
    </aside>

    <footer><div style="display:flex;justify-content:space-between;align-items:center;gap:12px;flex-wrap:wrap"><div class="muted">© <strong>Sachith R</strong> • Made with ✨ + ☕</div><div style="display:flex;gap:10px;align-items:center"><div class="muted" style="font-size:13px">Theme</div><button class="icon-btn" onclick="exportMarkdown()">Copy README</button></div></div></footer>
  </div>

  <script>
    // Theme handling
    const themeToggle = document.getElementById('theme-toggle');
    const themeLabel = document.getElementById('theme-label');
    function setTheme(theme){
      document.documentElement.setAttribute('data-theme', theme);
      localStorage.setItem('pref-theme', theme);
      themeLabel.textContent = theme === 'light' ? 'Light' : 'Dark';
      themeToggle.setAttribute('aria-pressed', theme === 'light');
    }
    (function initTheme(){
      const saved = localStorage.getItem('pref-theme');
      const prefersDark = window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches;
      if(saved) setTheme(saved);
      else setTheme(prefersDark ? 'dark' : 'light');
    })();
    themeToggle.addEventListener('click', ()=> {
      const current = document.documentElement.getAttribute('data-theme') || 'dark';
      setTheme(current === 'dark' ? 'light' : 'dark');
    });
    document.addEventListener('keydown', (e)=> { if(e.key.toLowerCase()==='t' && !/input|textarea/i.test(document.activeElement.tagName)) themeToggle.click(); });

    // copy helper
    function copyToClipboard(text){
      if(navigator.clipboard && navigator.clipboard.writeText){
        navigator.clipboard.writeText(text).then(()=> alert('Copied: ' + text)).catch(()=> fallbackCopy(text));
      } else fallbackCopy(text);
      function fallbackCopy(t){
        const ta = document.createElement('textarea'); ta.value = t; ta.style.position='fixed'; ta.style.opacity=0; document.body.appendChild(ta); ta.select(); document.execCommand('copy'); document.body.removeChild(ta); alert('Copied: ' + t);
      }
    }

    // README generation / export
    function generateREADME(){
      const md = buildMarkdown();
      const blob = new Blob([md], {type:'text/markdown'});
      const url = URL.createObjectURL(blob);
      window.open(url, '_blank');
    }
    function exportMarkdown(){
      const md = buildMarkdown();
      if(navigator.clipboard && navigator.clipboard.writeText){
        navigator.clipboard.writeText(md).then(()=> alert('README.md copied to clipboard — paste into your profile repo README.md')).catch(()=> download(md));
      } else download(md);
      function download(content){
        const blob = new Blob([content], {type:'text/markdown'});
        const a = document.createElement('a'); a.href = URL.createObjectURL(blob); a.download = 'README.md'; a.click();
      }
    }

    function buildMarkdown(){
      const lines = [];
      lines.push('# Hi, I’m Sachith R 👋✨');
      lines.push('');
      lines.push('> A little bit of code, a pinch of design, and a dash of magic.');
      lines.push('');
      lines.push('---');
      lines.push('');
      lines.push('## 🪄 About Me');
      lines.push('');
      lines.push('- 🎓 4th semester — BE (Computer Science & Design)');
      lines.push('- 💻 Tech stack: **HTML · CSS · JavaScript · React · Next.js · PHP · MySQL · Python**');
      lines.push('- 🎨 Passionate about UI/UX and smooth animations');
      lines.push('- ⚙️ Current builds: Feel Free (mental-health platform), Student Gig Platform, Deepfake Detection');
      lines.push('');
      lines.push('---');
      lines.push('');
      lines.push('## 🔮 Featured Projects');
      lines.push('');
      lines.push('- **Feel Free** — Mental-health support platform with interactive assessments & resources.');
      lines.push('- **Student Gig Platform** — Marketplace for students: PHP + MySQL starter with dashboards.');
      lines.push('- **Deepfake Detection** — ResNeXt + LSTM prototype; dockerized Django UI.');
      lines.push('');
      lines.push('---');
      lines.push('');
      lines.push('## 🧰 Toolbox');
      lines.push('');
      lines.push('- **Frontend:** HTML5, CSS3, Tailwind, React, Next.js, Framer Motion');
      lines.push('- **Backend:** Node.js, Express, PHP, Django');
      lines.push('- **Databases:** MySQL, SQLite');
      lines.push('- **ML/CV:** OpenCV, PyTorch');
      lines.push('');
      lines.push('---');
      lines.push('');
      lines.push('## 🤝 Contribute to Me');
      lines.push('');
      lines.push('I love collaboration — here\\'s the flow I prefer:');
      lines.push('');
      lines.push('1. ⭐ Star a repo');
      lines.push('2. 📝 Open an issue to discuss the idea');
      lines.push('3. 🔧 Fork → create `feature/your-idea` → PR');
      lines.push('4. 🧪 Add tests and screenshots (if applicable)');
      lines.push('5. 🗣️ Write a clear PR description and link related issues');
      lines.push('');
      lines.push('---');
      lines.push('');
      lines.push('## 📫 Contact & Links');
      lines.push('');
      lines.push('- 🔗 Portfolio: https://sachith.vercel.app/');
      lines.push('- 📧 Email: sachith2118@gmail.com');
      lines.push('- 💼 LinkedIn: https://www.linkedin.com/in/sachith-r-abab73254/');
      lines.push('- 🐙 GitHub: https://github.com/sachith1729');
      lines.push('');
      lines.push('---');
      lines.push('');
      lines.push('> May your commits be clean and your builds be green ✨');
      return lines.join('\n');
    }

    // smooth scroll helper
    function scrollToSection(id){ const el=document.getElementById(id); if(el) el.scrollIntoView({behavior:'smooth', block:'center'}); }

    // animate progress bars on load
    window.addEventListener('load', ()=> {
      document.querySelectorAll('.bar > i').forEach((el, idx) => {
        const w = el.style.width || '0%';
        el.style.width = '0%';
        setTimeout(()=> el.style.width = w, idx * 120);
      });
    });
  </script>
</body>
</html>
