<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Sachith R — Frontend Wizard & ML Tinkerer</title>
  <meta name="description" content="Sachith R — Frontend & ML tinkerer. Portfolio, projects, contact." />
  <style>
    /* -------------------------
       Base & Variables
       -------------------------*/
    :root{
      --bg:#0b1020;
      --card:#0f1724;
      --muted:#9aa6b2;
      --accent1:#7b2ff7;
      --accent2:#ff6fd8;
      --accent3:#ffd54a;
      --glass: rgba(255,255,255,0.03);
      --radius:14px;
      --glass-2: rgba(255,255,255,0.02);
      --text: #e6eef6;
      --mono: "SF Mono", "Segoe UI Mono", ui-monospace, Menlo, Monaco, "Roboto Mono", monospace;
      --sans: system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }

    [data-theme="light"]{
      --bg:#f7fbff;
      --card:#ffffff;
      --muted:#4b5563;
      --accent1:#5b21b6;
      --accent2:#db2777;
      --accent3:#d97706;
      --glass: rgba(10,10,10,0.02);
      --glass-2: rgba(10,10,10,0.01);
      --text:#071125;
    }

    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:var(--sans);
      background: linear-gradient(180deg, var(--bg), rgba(11,16,32,0.92));
      color:var(--text);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
      padding:28px;
      transition:background .35s ease, color .35s ease;
    }

    .container{
      max-width:1100px;
      margin:0 auto;
      display:grid;
      grid-template-columns: 1fr 360px;
      gap:28px;
      align-items:start;
    }

    /* Responsive */
    @media (max-width:980px){
      .container{grid-template-columns: 1fr; padding:0 12px}
      header .meta {justify-content:center}
    }

    /* -------------------------
       Header
       -------------------------*/
    header{
      grid-column:1 / -1;
      display:flex;
      gap:18px;
      align-items:center;
      justify-content:space-between;
      margin-bottom:2px;
    }

    .title{
      display:flex;
      gap:16px;
      align-items:center;
    }

    .badge-wand{
      width:68px;
      height:68px;
      border-radius:12px;
      background: linear-gradient(135deg, rgba(123,47,247,0.18), rgba(255,111,216,0.12));
      display:grid;
      place-items:center;
      box-shadow: 0 6px 18px rgba(11,12,20,0.6), inset 0 -6px 14px rgba(255,255,255,0.02);
      transform: translateZ(0);
    }

    .badge-wand svg{width:36px;height:36px;display:block;filter:drop-shadow(0 6px 16px rgba(123,47,247,0.12))}

    h1{
      margin:0;
      font-size:20px;
      letter-spacing:0.6px;
    }
    p.lead{
      margin:.25rem 0 0 0;
      font-size:13px;
      color:var(--muted);
    }

    .meta{
      display:flex;
      gap:10px;
      align-items:center;
    }

    button.icon-btn{
      background:var(--glass);
      border:1px solid transparent;
      color:var(--text);
      padding:8px 12px;
      border-radius:10px;
      cursor:pointer;
      font-weight:600;
      display:inline-flex;
      gap:10px;
      align-items:center;
      transition:all .18s ease;
    }
    button.icon-btn:hover{transform:translateY(-3px); box-shadow:0 8px 24px rgba(11,12,20,0.3)}

    /* -------------------------
       Main card & panels
       -------------------------*/
    .card{
      background: linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.00));
      border-radius: var(--radius);
      padding:18px;
      border:1px solid rgba(255,255,255,0.03);
      box-shadow: 0 8px 30px rgba(2,6,23,0.5);
    }

    .hero{
      display:flex;
      gap:18px;
      align-items:flex-start;
      padding:20px;
      border-radius:12px;
      background: linear-gradient(135deg, rgba(255,255,255,0.012), rgba(255,255,255,0.015));
      border:1px solid rgba(255,255,255,0.03);
    }

    .hero-left{flex:1; min-width:0}
    .hero-right{
      width:320px;
      display:flex;
      flex-direction:column;
      gap:12px;
    }

    .skill-pill{display:inline-flex; gap:8px; align-items:center; padding:8px 10px; border-radius:999px; font-weight:600; font-size:13px; background:var(--glass-2); color:var(--muted)}
    .skill-pill strong{color:var(--text)}

    /* Progress bar */
    .prog{
      margin:8px 0 14px 0;
    }
    .prog .label{display:flex;justify-content:space-between;font-size:13px;color:var(--muted);margin-bottom:6px}
    .bar{
      height:12px;
      border-radius:999px;
      background: linear-gradient(90deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      overflow:hidden;
      border:1px solid rgba(255,255,255,0.02);
    }
    .bar > i{
      display:block;
      height:100%;
      width:0%;
      border-radius:999px;
      background: linear-gradient(90deg, var(--accent1), var(--accent2));
      transition:width .9s cubic-bezier(.2,.9,.2,1);
      box-shadow: 0 6px 16px rgba(123,47,247,0.12);
    }

    /* Projects grid */
    .projects{display:grid; gap:12px; grid-template-columns:repeat(auto-fit, minmax(240px,1fr))}
    .proj{
      padding:12px;
      border-radius:12px;
      background: linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.00));
      border:1px solid rgba(255,255,255,0.03);
      transition: transform .18s ease, box-shadow .18s ease;
    }
    .proj:hover{transform:translateY(-6px); box-shadow:0 16px 40px rgba(2,6,23,0.5)}
    .proj h4{margin:0 0 6px 0}
    .proj p{margin:0;color:var(--muted);font-size:13px}

    /* Right column */
    .profile{
      display:flex;
      flex-direction:column;
      gap:12px;
    }
    .info-row{display:flex;gap:10px;align-items:center;justify-content:space-between}
    .info{
      padding:12px;border-radius:12px;background:var(--glass); border:1px solid rgba(255,255,255,0.02)
    }

    /* social links */
    .socials{display:flex;flex-wrap:wrap;gap:8px}
    .link-chip{
      display:inline-flex;align-items:center;gap:8px;padding:8px 12px;border-radius:999px;background:linear-gradient(90deg, rgba(255,255,255,0.01), rgba(255,255,255,0.00));
      border:1px solid rgba(255,255,255,0.03);text-decoration:none;color:var(--text);font-weight:600;font-size:13px
    }
    .link-chip svg{width:16px;height:16px;opacity:.95}

    /* Contribute */
    .contrib{
      display:flex;flex-direction:column;gap:10px;padding:12px;border-radius:12px;background:linear-gradient(180deg,rgba(255,255,255,0.01),rgba(255,255,255,0.00));border:1px solid rgba(255,255,255,0.03)
    }
    .contrib li{margin:6px 0;font-size:14px;color:var(--muted)}

    /* Footer */
    footer{grid-column:1/-1;margin-top:18px;opacity:.95}
    .copy-btn{background:transparent;border:1px dashed rgba(255,255,255,0.04);padding:8px 12px;border-radius:10px;font-family:var(--mono);font-weight:700;cursor:pointer}

    /* small screens tweaks */
    @media (max-width:520px){
      .hero-right{width:auto}
    }

    /* subtle floating animation for accent */
    .float{
      animation: floaty 6s ease-in-out infinite;
    }
    @keyframes floaty{
      0%{transform:translateY(0)}
      50%{transform:translateY(-8px)}
      100%{transform:translateY(0)}
    }

    /* tiny helpers */
    .muted{color:var(--muted);font-size:13px}
    .tag{display:inline-block;padding:6px 8px;border-radius:8px;background:rgba(255,255,255,0.02);font-weight:700;font-size:12px}
    .pill{padding:6px 10px;border-radius:999px;background:linear-gradient(90deg,var(--accent1),var(--accent2));color:white;font-weight:700;font-size:13px}

    a{color:inherit}
  </style>
</head>
<body>
  <div class="container" id="app">
    <header>
      <div class="title" aria-hidden="false">
        <span class="badge-wand float" title="Magic of UI">
          <!-- wand icon -->
          <svg viewBox="0 0 24 24" fill="none" aria-hidden="true">
            <rect x="10" y="3" width="4" height="14" rx="2" fill="white" opacity="0.92" transform="rotate(20 12 10)"></rect>
            <circle cx="19.5" cy="4.5" r="2.5" fill="white" opacity="0.95"></circle>
            <circle cx="4.5" cy="15.5" r="1.6" fill="white" opacity="0.9"></circle>
          </svg>
        </span>
        <div>
          <h1>Sachith R <span style="font-size:12px;color:var(--muted);font-weight:600">· Frontend • ML tinkerer</span></h1>
          <p class="lead">I build clean UIs, playful interactions, and experiment with ML for real-world problems.</p>
        </div>
      </div>

      <div class="meta">
        <button id="theme-toggle" class="icon-btn" aria-pressed="false" title="Toggle theme (T)">
          <!-- moon / sun -->
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" aria-hidden="true"><path d="M21 12.79A9 9 0 1111.21 3 7 7 0 0021 12.79z" fill="currentColor"/></svg>
          <span id="theme-label">Dark</span>
        </button>
        <a class="icon-btn" href="https://sachith.vercel.app/" target="_blank" rel="noopener noreferrer" title="Portfolio">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" aria-hidden="true"><path d="M12 2l4 4-8 8-4-4 8-8z" fill="currentColor"/></svg>
          Portfolio
        </a>
        <a class="icon-btn" href="mailto:sachith2118@gmail.com" title="Email">
          ✉️ Email
        </a>
      </div>
    </header>

    <!-- left column -->
    <main>
      <section class="card hero" aria-label="Hero">
        <div class="hero-left">
          <div style="display:flex;gap:12px;align-items:center;flex-wrap:wrap">
            <div class="skill-pill">✨ <strong>Frontend</strong> • UI & Animations</div>
            <div class="skill-pill">🛰️ <strong>ML/CV</strong> • Deepfake Detection</div>
            <div class="skill-pill">🗄️ <strong>Backend</strong> • PHP / Node / MySQL</div>
          </div>

          <h2 style="margin-top:14px;margin-bottom:6px">Projects & Highlights</h2>
          <div class="projects" style="margin-top:6px">
            <article class="proj">
              <h4>Feel Free</h4>
              <p class="muted">Mental-health support platform with interactive assessments and resources. Built with HTML/CSS/JS + planned AI personalization.</p>
            </article>

            <article class="proj">
              <h4>Student Gig Platform</h4>
              <p class="muted">Marketplace for student gigs — PHP + MySQL starter with dashboards for students & startups.</p>
            </article>

            <article class="proj">
              <h4>Deepfake Detection</h4>
              <p class="muted">Prototype using ResNeXt + LSTM, dockerized Django UI for quick testing and demos.</p>
            </article>
          </div>

          <div style="margin-top:18px;display:flex;gap:12px;flex-wrap:wrap;align-items:center">
            <button class="icon-btn" onclick="scrollToSection('contribute')">🤝 Contribute</button>
            <button class="icon-btn" onclick="generateREADME()">📄 Export README</button>
            <button class="icon-btn" onclick="copyToClipboard('sachith2118@gmail.com')">📧 Copy Email</button>
          </div>

          <hr style="border:none;height:1px;background:linear-gradient(90deg, transparent, rgba(255,255,255,0.03), transparent);margin:18px 0">

          <h3 style="margin:0 0 6px 0">Selected Tech</h3>
          <div style="display:flex;gap:10px;flex-wrap:wrap">
            <span class="tag">HTML</span><span class="tag">CSS</span><span class="tag">JavaScript</span><span class="tag">React</span><span class="tag">Next.js</span><span class="tag">PHP</span><span class="tag">MySQL</span><span class="tag">Python</span><span class="tag">PyTorch</span>
          </div>

          <hr style="border:none;height:1px;background:linear-gradient(90deg, transparent, rgba(255,255,255,0.03), transparent);margin:16px 0">

          <h3 style="margin:0 0 10px 0">Skills</h3>
          <div class="prog">
            <div class="label"><span>HTML</span><span>90%</span></div>
            <div class="bar"><i style="width:90%"></i></div>
          </div>
          <div class="prog">
            <div class="label"><span>CSS / Animations</span><span>82%</span></div>
            <div class="bar"><i style="width:82%"></i></div>
          </div>
          <div class="prog">
            <div class="label"><span>JavaScript</span><span>75%</span></div>
            <div class="bar"><i style="width:75%"></i></div>
          </div>
          <div class="prog">
            <div class="label"><span>React / Next</span><span>70%</span></div>
            <div class="bar"><i style="width:70%"></i></div>
          </div>
          <div class="prog">
            <div class="label"><span>Python / ML</span><span>50%</span></div>
            <div class="bar"><i style="width:50%"></i></div>
          </div>
        </div>

        <aside class="hero-right">
          <div class="card info" aria-hidden="false">
            <div style="display:flex;justify-content:space-between;align-items:center">
              <div>
                <div class="muted">NAME</div>
                <div style="font-weight:800">Sachith R</div>
              </div>
              <div style="text-align:right">
                <div class="muted">ROLE</div>
                <div style="font-weight:800">Frontend & ML tinkerer</div>
              </div>
            </div>
            <div style="margin-top:10px" class="muted">4th semester BE — Computer Science & Design</div>
          </div>

          <div class="card info">
            <div class="muted">Contact</div>
            <div style="display:flex;flex-direction:column;gap:6px;margin-top:8px">
              <a class="link-chip" href="https://sachith.vercel.app/" target="_blank" rel="noopener noreferrer">
                <!-- globe svg -->
                <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M12 2a10 10 0 100 20 10 10 0 000-20z"></path></svg>
                Portfolio
              </a>
              <a class="link-chip" href="https://www.linkedin.com/in/sachith-r-abab73254/" target="_blank" rel="noopener noreferrer">
                <!-- linkedin -->
                <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M4.98 3.5a2.3 2.3 0 11-.02 0zM3 8h4v12H3zM8 8h3.8v1.64h.05C12.48 8.48 13.9 7 16.98 7 21 7 21 10.06 21 14.02V20H17v-5c0-1.2-.02-2.74-1.67-2.74C13.6 12.26 13.4 13.7 13.4 15V20H8z"></path></svg>
                LinkedIn
              </a>
              <a class="link-chip" href="https://github.com/sachith1729" target="_blank" rel="noopener noreferrer">
                <!-- github -->
                <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M12 .5C5.38.5 0 5.88 0 12.5c0 5.29 3.438 9.77 8.205 11.36.6.11.82-.26.82-.58 0-.29-.01-1.05-.02-2.06-3.338.73-4.042-1.61-4.042-1.61-.546-1.39-1.333-1.76-1.333-1.76-1.09-.75.083-.73.083-.73 1.205.086 1.84 1.24 1.84 1.24 1.07 1.83 2.8 1.3 3.485.99.11-.77.42-1.3.77-1.6-2.665-.3-5.466-1.33-5.466-5.92 0-1.31.47-2.38 1.24-3.22-.124-.3-.54-1.52.117-3.16 0 0 1.01-.32 3.3 1.23a11.5 11.5 0 016 0c2.29-1.55 3.29-1.23 3.29-1.23.66 1.64.24 2.86.12 3.16.77.84 1.23 1.91 1.23 3.22 0 4.6-2.8 5.61-5.47 5.91.43.38.81 1.13.81 2.28 0 1.64-.02 2.96-.02 3.36 0 .32.21.7.82.58A12.01 12.01 0 0024 12.5C24 5.88 18.62.5 12 .5z"></path></svg>
                GitHub
              </a>
              <button class="link-chip" onclick="copyToClipboard('sachith2118@gmail.com')">📧 Copy Email</button>
            </div>
          </div>

          <div class="card contrib" id="contribute">
            <div style="display:flex;justify-content:space-between;align-items:center">
              <div style="font-weight:800">Contribute to me</div>
              <div class="pill">Good first PRs</div>
            </div>
            <div style="font-size:13px;color:var(--muted);margin-top:8px">I love collaboration — here's a simple flow:</div>
            <ul style="padding-left:18px;margin:10px 0 0 0;color:var(--muted)">
              <li>⭐ Star a repo you like</li>
              <li>📝 Open an issue to propose changes</li>
              <li>🔧 Fork → create <code>feature/your-idea</code> → PR</li>
              <li>🧪 Add tests / screenshots if relevant</li>
              <li>🗣️ Use clear PR description & link related issues</li>
            </ul>
          </div>
        </aside>
      </section>

      <section class="card" style="margin-top:16px">
        <h3 style="margin:0 0 10px 0">Why I care about UX & ML</h3>
        <p class="muted">I believe good interfaces amplify human ability. ML should assist not confuse. My experiments focus on clear UI patterns for complex ML tools — think: sane defaults, clear feedback, and delightful micro-interactions.</p>
      </section>

      <section class="card" style="margin-top:16px">
        <h3 style="margin:0 0 10px 0">Quick Links</h3>
        <div style="display:flex;gap:10px;flex-wrap:wrap">
          <a class="link-chip" href="https://github.com/sachith1729" target="_blank">GitHub</a>
          <a class="link-chip" href="https://sachith.vercel.app/" target="_blank">Portfolio</a>
          <a class="link-chip" href="https://www.linkedin.com/in/sachith-r-abab73254/" target="_blank">LinkedIn</a>
          <a class="link-chip" href="mailto:sachith2118@gmail.com">Email</a>
        </div>
      </section>

    </main>

    <!-- right column -->
    <aside>
      <div class="card profile">
        <div style="display:flex;flex-direction:column;gap:6px">
          <div style="font-size:13px;color:var(--muted)">PROFILE</div>
          <div style="font-weight:800">Sachith R</div>
          <div class="muted">Frontend • ML tinkerer • UI lover</div>
        </div>

        <div style="margin-top:8px">
          <div class="muted" style="font-size:13px">Location</div>
          <div style="font-weight:700">India</div>
        </div>

        <div style="margin-top:10px">
          <div class="muted" style="font-size:13px">Contact</div>
          <div style="display:flex;gap:8px;margin-top:8px">
            <button class="copy-btn" onclick="copyToClipboard('sachith2118@gmail.com')">Copy Email</button>
            <a class="copy-btn" href="https://github.com/sachith1729" target="_blank">GitHub</a>
          </div>
        </div>

        <div style="margin-top:12px">
          <div class="muted" style="font-size:13px">Social</div>
          <div class="socials" style="margin-top:8px">
            <a class="link-chip" href="https://sachith.vercel.app/" target="_blank">Portfolio</a>
            <a class="link-chip" href="https://www.linkedin.com/in/sachith-r-abab73254/" target="_blank">LinkedIn</a>
            <a class="link-chip" href="https://github.com/sachith1729" target="_blank">GitHub</a>
          </div>
        </div>

        <div style="margin-top:12px">
          <div class="muted" style="font-size:13px">Status</div>
          <div style="margin-top:8px">
            <div class="tag">Open to collaborate</div>
          </div>
        </div>
      </div>

      <div class="card" style="margin-top:12px">
        <div style="display:flex;justify-content:space-between;align-items:center">
          <div style="font-weight:800">Mini Checklist</div>
          <div class="muted" style="font-size:12px">Make a PR</div>
        </div>
        <ol style="margin:10px 0 0 16px;color:var(--muted)">
          <li>Fork repo</li>
          <li>Create <code>feature/your-idea</code></li>
          <li>Write code & tests</li>
          <li>Open PR → link issue</li>
        </ol>
      </div>
    </aside>

    <footer>
      <div style="display:flex;justify-content:space-between;gap:12px;align-items:center;flex-wrap:wrap">
        <div class="muted">© <strong>Sachith R</strong> • Made with ✨ + ☕</div>
        <div style="display:flex;gap:10px;align-items:center">
          <div class="muted" style="font-size:13px">Theme</div>
          <button class="icon-btn" onclick="exportMarkdown()" title="Copy README Markdown">Copy README</button>
        </div>
      </div>
    </footer>
  </div>

  <script>
    // -------------------------
    // Theme toggle
    // -------------------------
    const root = document.documentElement;
    const themeToggle = document.getElementById('theme-toggle');
    const themeLabel = document.getElementById('theme-label');

    function setTheme(theme){
      document.documentElement.setAttribute('data-theme', theme);
      localStorage.setItem('pref-theme', theme);
      themeLabel.textContent = theme === 'light' ? 'Light' : 'Dark';
      themeToggle.setAttribute('aria-pressed', theme === 'light');
    }

    // initialize
    (function initTheme(){
      const saved = localStorage.getItem('pref-theme');
      const prefersDark = window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches;
      if(saved) setTheme(saved);
      else setTheme(prefersDark ? 'dark' : 'light');
    })();

    themeToggle.addEventListener('click', () => {
      const current = document.documentElement.getAttribute('data-theme') || 'dark';
      setTheme(current === 'dark' ? 'light' : 'dark');
    });

    // keyboard toggle (T)
    document.addEventListener('keydown', (e) => {
      if(e.key.toLowerCase() === 't' && !/input|textarea/i.test(document.activeElement.tagName)){
        themeToggle.click();
      }
    });

    // -------------------------
    // Copy to clipboard helper
    // -------------------------
    function copyToClipboard(text){
      navigator.clipboard?.writeText(text).then(() => {
        alert('Copied: ' + text);
      }).catch(() => {
        // fallback
        const ta = document.createElement('textarea');
        ta.value = text;
        ta.style.position = 'fixed';
        ta.style.opacity = 0;
        document.body.appendChild(ta);
        ta.select();
        document.execCommand('copy');
        document.body.removeChild(ta);
        alert('Copied: ' + text);
      });
    }

    // -------------------------
    // Generate README Markdown
    // -------------------------
    function generateREADME(){
      const md = buildMarkdown();
      // open in new tab and show markdown (so user can copy/save)
      const blob = new Blob([md], {type:'text/markdown'});
      const url = URL.createObjectURL(blob);
      window.open(url, '_blank');
    }

    function exportMarkdown(){
      const md = buildMarkdown();
      navigator.clipboard?.writeText(md).then(() => {
        alert('README.md content copied to clipboard — paste into your profile repo README.md');
      }).catch(() => {
        // fallback: open download
        const blob = new Blob([md], {type:'text/markdown'});
        const a = document.createElement('a');
        a.href = URL.createObjectURL(blob);
        a.download = 'README.md';
        a.click();
      });
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
      lines.push('I love collaboration — here\'s the flow I prefer:');
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
      return lines.join('\\n');
    }

    // -------------------------
    // Utility to smooth scroll to section
    // -------------------------
    function scrollToSection(id){
      const el = document.getElementById(id);
      if(el) el.scrollIntoView({behavior:'smooth', block:'center'});
    }

    // small entrance animation for progress bars
    window.addEventListener('load', () => {
      document.querySelectorAll('.bar > i').forEach((el, idx) => {
        const w = el.style.width || '0%';
        el.style.width = '0%';
        setTimeout(()=> el.style.width = w, idx * 150);
      });
    });
  </script>
</body>
</html>
