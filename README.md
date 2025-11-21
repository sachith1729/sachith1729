
- Use code blocks for progress / badges and ASCII art for headers.

---

## OPTIONAL: Save as `index.html` (Full HTML/CSS/JS)
If you want an **interactive web page** with the same funky design, copy everything in the block below into a file named `index.html` and open it in your browser. (This is a standalone page — scripts will **not** run inside GitHub README; copy to `.html` to run.)

```html
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1"/>
<title>Sachith R — Funky Profile</title>
<style>
  :root{--bg:#0b1020;--card:#0f1724;--muted:#9aa6b2;--accent1:#7b2ff7;--accent2:#ff6fd8;--text:#e6eef6}
  [data-theme="light"]{--bg:#f7fbff;--card:#fff;--muted:#4b5563;--text:#071125}
  *{box-sizing:border-box} body{margin:0;font-family:Inter,system-ui;background:linear-gradient(180deg,var(--bg),#071225);color:var(--text);padding:28px}
  .wrap{max-width:1000px;margin:0 auto}
  pre{background:rgba(255,255,255,0.02);padding:12px;border-radius:10px;overflow:auto}
  .card{background:rgba(255,255,255,0.02);padding:18px;border-radius:12px;margin-bottom:18px;border:1px solid rgba(255,255,255,0.03)}
  .row{display:flex;gap:18px;flex-wrap:wrap}
  .pill{display:inline-block;padding:6px 10px;border-radius:999px;background:linear-gradient(90deg,var(--accent1),var(--accent2));color:#fff;font-weight:700}
  a{color:inherit}
  details{margin-top:8px}
  .center{display:flex;align-items:center;gap:12px}
  button{padding:8px 10px;border-radius:8px;border:none;background:rgba(255,255,255,0.03);color:var(--text);cursor:pointer}
</style>
</head>
<body>
<div class="wrap">
  <h1>✨ <strong>Sachith R</strong> — Frontend Wizard & ML tinkerer</h1>
  <p>A little bit of code, a pinch of design, and a dash of magic.</p>

  <div class="card">
    <div class="row">
      <div style="flex:1">
        <h3>Projects</h3>
        <ul>
          <li><strong>Feel Free</strong> — Mental-health support platform</li>
          <li><strong>Student Gig Platform</strong> — Marketplace for students</li>
          <li><strong>Deepfake Detection</strong> — ResNeXt + LSTM prototype</li>
        </ul>
      </div>
      <div style="width:260px">
        <h4>Contact</h4>
        <div class="center"><button onclick="copy('sachith2118@gmail.com')">📧 Copy Email</button> <a href="https://sachith.vercel.app/" target="_blank">Portfolio</a></div>
        <div style="margin-top:12px"><a href="https://www.linkedin.com/in/sachith-r-abab73254/" target="_blank">LinkedIn</a><br/><a href="https://github.com/sachith1729" target="_blank">GitHub</a></div>
      </div>
    </div>
  </div>

  <div class="card">
    <h3>Skills</h3>
    <pre>HTML      ▮▮▮▮▮▮▮▮▮▮ 90%
CSS/Anim  ▮▮▮▮▮▮▮▮▯ 82%
JS        ▮▮▮▮▮▮▮▯▯ 75%
React     ▮▮▮▮▮▮▯▯ 70%
Python    ▮▮▮▮▯▯▯ 50%</pre>
    <details><summary>Contribute to me (click)</summary>
      <ol>
        <li>⭐ Star a repo</li>
        <li>📝 Open an issue</li>
        <li>🔧 Fork → branch → PR</li>
      </ol>
    </details>
  </div>

  <div class="card">
    <h3>Philosophy</h3>
    <p><em>Code isn't just logic — it's experience.</em></p>
    <p>If it's ugly → rewrite. If it's slow → optimize. If it's boring → animate.</p>
  </div>

  <div style="text-align:center;color:var(--muted)">© Sachith R • sachith2118@gmail.com</div>
</div>

<script>
  function copy(text){
    if(navigator.clipboard) navigator.clipboard.writeText(text).then(()=> alert('Copied: '+text));
    else { const t=document.createElement('textarea'); t.value=text; document.body.appendChild(t); t.select(); document.execCommand('copy'); document.body.removeChild(t); alert('Copied: '+text);}
  }
</script>
</body>
</html>
