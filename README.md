<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Dev Irshad — Let’s Get Started: The New Game of Python</title>
  <meta name="description" content="Landing page for Dev Irshad — Let’s Get Started: The New Game of Python." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600;800&family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg: #0b1020;
      --bg-2: #0f1530;
      --text:#e6e9f5;
      --muted:#aab2d6;
      --accent:#7c5cff;
      --accent-2:#00e5ff;
      --card:#121735;
      --border: rgba(255,255,255,.08);
      --success:#2dd4bf;
    }
    @media (prefers-color-scheme: light){
      :root{
        --bg:#f7f8ff; --bg-2:#ffffff; --text:#111322; --muted:#3a4766; --card:#ffffff; --border:rgba(0,0,0,.08);
      }
      .glow::before{filter: blur(60px); opacity:.45}
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; background: radial-gradient(1200px 600px at 10% 10%, rgba(124,92,255,.15), transparent 60%),
                 radial-gradient(900px 500px at 90% 20%, rgba(0,229,255,.10), transparent 60%),
                 linear-gradient(180deg, var(--bg), var(--bg-2));
      color:var(--text); font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
      line-height:1.6;
    }
    a{color:inherit; text-decoration:none}
    .container{max-width:1100px; margin:0 auto; padding:24px}
    header{position:sticky; top:0; z-index:50; backdrop-filter:saturate(120%) blur(6px); background: color-mix(in oklab, var(--bg-2) 80%, transparent); border-bottom:1px solid var(--border)}
    .nav{display:flex; align-items:center; justify-content:space-between; gap:16px}
    .brand{display:flex; align-items:center; gap:10px; font-weight:800; letter-spacing:.3px}
    .brand .logo{width:36px; height:36px; border-radius:12px; background:linear-gradient(135deg, var(--accent), var(--accent-2)); display:grid; place-items:center; box-shadow:0 6px 30px rgba(124,92,255,.35)}
    .brand .logo span{font:800 18px/1 "JetBrains Mono", monospace; color:#0b1020}
    .nav a.btn{padding:10px 16px; border:1px solid var(--border); border-radius:12px; font-weight:600}
    .nav a.btn.primary{background:linear-gradient(135deg, var(--accent), var(--accent-2)); color:#0b1020; border:0; box-shadow:0 10px 30px rgba(124,92,255,.35)}

    /* Hero */
    .hero{padding:72px 24px 32px; position:relative}
    .hero h1{font-size: clamp(32px, 4vw + 16px, 64px); line-height:1.05; margin:0 0 16px; font-weight:800}
    .hero p{font-size:clamp(16px, 1.2vw + 10px, 22px); color:var(--muted); max-width:780px}

    .cta{display:flex; gap:12px; flex-wrap:wrap; margin-top:24px}
    .cta .btn{padding:14px 18px; border:1px solid var(--border); border-radius:14px; font-weight:700; letter-spacing:.2px}
    .cta .btn.primary{background:linear-gradient(135deg, var(--accent), var(--accent-2)); color:#0b1020; border:0}
    .cta .hint{font-size:14px; color:var(--muted); display:flex; align-items:center; gap:8px}

    /* Cards */
    .grid{display:grid; grid-template-columns:repeat(12,1fr); gap:18px; margin-top:36px}
    .card{grid-column: span 12; background:linear-gradient(180deg, color-mix(in oklab, var(--card) 90%, transparent), color-mix(in oklab, var(--bg-2) 50%, transparent)); border:1px solid var(--border); border-radius:20px; padding:22px; position:relative; overflow:hidden}
    .card h3{margin:0 0 8px; font-size:20px}
    .card p{margin:0; color:var(--muted)}
    .card .tag{position:absolute; top:14px; right:14px; font:700 12px/1 "JetBrains Mono", monospace; border:1px solid var(--border); padding:6px 8px; border-radius:999px; opacity:.9}
    .glow::before{content:""; position:absolute; inset:auto -30% -40% -30%; height:140px; background:radial-gradient(60% 120% at 50% 0%, rgba(124,92,255,.35), transparent 60%); filter:blur(80px); opacity:.35; pointer-events:none}

    @media (min-width:768px){
      .card--wide{grid-column: span 7}
      .card--tall{grid-column: span 5}
    }

    /* Code block */
    pre, code{font-family: "JetBrains Mono", ui-monospace, SFMono-Regular, Menlo, Consolas, monospace}
    pre{background: #0c1333; color:#dfe5ff; border:1px solid var(--border); border-radius:16px; padding:16px; overflow:auto}
    .kbd{font:700 12px/1 "JetBrains Mono", monospace; border:1px solid var(--border); padding:4px 8px; border-radius:8px}

    /* Footer */
    footer{margin-top:40px; padding:28px 0; border-top:1px solid var(--border); color:var(--muted)}

    /* Nice focus rings */
    :where(a, button, .btn){outline:none}
    :where(a, button, .btn):focus-visible{box-shadow:0 0 0 3px color-mix(in oklab, var(--accent-2) 60%, white)}
  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <a class="brand" href="#home" aria-label="Go to start">
        <div class="logo" aria-hidden="true"><span>Py</span></div>
        <span>Dev Irshad</span>
      </a>
      <nav style="display:flex; gap:10px; align-items:center">
        <!-- <a class="btn" href="#features">Features</a>
        <a class="btn" href="#demo">Demo</a> -->
        <a class="btn primary" href="#+">Get Started</a>
      </nav>
    </div>
  </header>

  <main id="home" class="container">
    <section class="hero">
      <h1>Let’s Get Started: <span style="background:linear-gradient(135deg, var(--accent), var(--accent-2)); -webkit-background-clip:text; background-clip:text; color:transparent">The New Game of Python</span></h1>
      <p>Build your first Python game in minutes. This starter kit by <strong>Dev Irshad</strong> includes clean HTML & CSS for your landing page, plus a plug‑and‑play Python loop you can run locally. No frameworks required.</p>
      <div class="cta">
        <a class="btn primary" href="#demo">▶ Play Demo</a>
        <a class="btn" href="#get-started">⚡ Quick Start</a>
        <span class="hint">Press <span class="kbd">G</span> then <span class="kbd">S</span> to “Get Started”.</span>
      </div>
    </section>

    <section id="features" class="grid">
      <article class="card card--wide glow">
        <span class="tag">HTML + CSS</span>
        <h3>Beautiful by default</h3>
        <p>A modern, responsive layout with neon‑glass accents, smooth focus rings, and zero JavaScript required.</p>
      </article>
      <article class="card card--tall">
        <span class="tag">Python</span>
        <h3>Minimal game loop</h3>
        <p>Start from a tiny Python loop (below) and expand with levels, scoring, and keyboard controls.</p>
      </article>
      <article class="card card--tall">
        <span class="tag">Open Source</span>
        <h3>Yours to remix</h3>
        <p>MIT‑style starter. Replace text, drop in your sprites, and ship.</p>
      </article>
    </section>

    <section id="demo" style="margin-top:28px">
      <div class="card">
        <h3 style="margin:0 0 10px">Python “New Game” starter (copy & run)</h3>
        <pre><code># game.py — super tiny loop
import time

running = True
player_x = 0

print("Welcome to The New Game of Python!")
print("Use Ctrl+C to quit.")

try:
    while running:
        player_x += 1
        print(f"Tick… player at {player_x}")
        time.sleep(0.5)
except KeyboardInterrupt:
    print("\nGoodbye from Dev Irshad!")
</code></pre>
        <p style="color:var(--muted); margin-top:10px">Save as <code>game.py</code>, then run <code class="kbd">python game.py</code>.</p>
      </div>
    </section>

    <section id="get-started" style="margin-top:28px">
      <div class="grid">
        <div class="card">
          <h3>Quick Start</h3>
          <ol style="margin:0; padding-left:16px">
            <li>Download this HTML file and rename it to <code>index.html</code>.</li>
            <li>Create <code>game.py</code> with the snippet above.</li>
            <li>Open <code>index.html</code> in your browser to show the landing page.</li>
            <li>Run your Python file with <code class="kbd">python game.py</code>.</li>
          </ol>
        </div>
        <div class="card">
          <h3>Customize</h3>
          <ul style="margin:0; padding-left:16px">
            <li>Change colors by editing the <code>:root</code> CSS variables.</li>
            <li>Swap the logo text (<code>Py</code>) with your initials.</li>
            <li>Add screenshots or GIFs of your game inside the Demo card.</li>
          </ul>
        </div>
      </div>
    </section>

    <footer class="container">
      <p>© <span id="year"></span> Dev Irshad · Built with pure HTML & CSS · Ready for your Python game.</p>
    </footer>
  </main>

  <script>
    // Optional niceties: dynamic year + playful key combo
    document.getElementById('year').textContent = new Date().getFullYear();
    let keys = [];
    window.addEventListener('keydown', (e) => {
      keys.push(e.key.toLowerCase());
      if(keys.slice(-2).join('') === 'gs'){
        location.hash = '#get-started';
      }
      if(keys.length > 2) keys = keys.slice(-2);
    });
  </script>
</body>
</html>
