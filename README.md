<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Prakhar Shukla — DevOps Engineer</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400;600;700&family=Syne:wght@400;600;800&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0a0c10;
    --surface: #0f1318;
    --border: #1e2530;
    --accent: #00d4ff;
    --accent2: #7c3aed;
    --accent3: #f59e0b;
    --text: #e2e8f0;
    --muted: #64748b;
    --green: #10b981;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'JetBrains Mono', monospace;
    overflow-x: hidden;
    cursor: none;
  }

  /* Custom cursor */
  .cursor {
    width: 10px; height: 10px;
    background: var(--accent);
    border-radius: 50%;
    position: fixed;
    pointer-events: none;
    z-index: 9999;
    transition: transform 0.1s, opacity 0.3s;
    mix-blend-mode: screen;
  }
  .cursor-ring {
    width: 36px; height: 36px;
    border: 1.5px solid var(--accent);
    border-radius: 50%;
    position: fixed;
    pointer-events: none;
    z-index: 9998;
    transition: all 0.15s ease;
    opacity: 0.5;
  }

  /* Grid BG */
  body::before {
    content: '';
    position: fixed; inset: 0;
    background-image:
      linear-gradient(rgba(0,212,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,212,255,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    z-index: 0;
    pointer-events: none;
  }

  /* Noise overlay */
  body::after {
    content: '';
    position: fixed; inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.04'/%3E%3C/svg%3E");
    z-index: 0;
    pointer-events: none;
    opacity: 0.4;
  }

  .container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 24px;
    position: relative;
    z-index: 1;
  }

  /* ── HEADER ── */
  header {
    padding: 60px 0 40px;
    position: relative;
  }

  .terminal-bar {
    display: flex;
    align-items: center;
    gap: 8px;
    margin-bottom: 32px;
    opacity: 0;
    animation: fadeUp 0.6s ease forwards;
  }
  .dot { width: 12px; height: 12px; border-radius: 50%; }
  .dot.r { background: #ff5f57; }
  .dot.y { background: #ffbd2e; }
  .dot.g { background: #28ca41; }
  .terminal-path {
    margin-left: 12px;
    color: var(--muted);
    font-size: 12px;
    letter-spacing: 0.05em;
  }
  .terminal-path span { color: var(--accent); }

  .hero-name {
    font-family: 'Syne', sans-serif;
    font-size: clamp(48px, 8vw, 96px);
    font-weight: 800;
    line-height: 0.95;
    letter-spacing: -0.02em;
    opacity: 0;
    animation: fadeUp 0.7s ease 0.2s forwards;
  }
  .hero-name .line1 { display: block; color: var(--text); }
  .hero-name .line2 {
    display: block;
    background: linear-gradient(90deg, var(--accent), var(--accent2));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .hero-sub {
    margin-top: 16px;
    color: var(--muted);
    font-size: 13px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    opacity: 0;
    animation: fadeUp 0.7s ease 0.35s forwards;
  }
  .hero-sub em { color: var(--accent3); font-style: normal; }

  .typing-line {
    margin-top: 24px;
    font-size: 14px;
    color: var(--green);
    opacity: 0;
    animation: fadeUp 0.7s ease 0.5s forwards;
  }
  .typing-line::before { content: '$ '; color: var(--muted); }
  .typed-text { }
  .cursor-blink { animation: blink 1s infinite; }

  /* ── ABOUT CARDS ── */
  .section { padding: 60px 0; }
  .section-label {
    font-size: 11px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 24px;
    display: flex;
    align-items: center;
    gap: 12px;
  }
  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  .about-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 16px;
  }

  .about-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 20px;
    position: relative;
    overflow: hidden;
    transition: border-color 0.3s, transform 0.3s;
    opacity: 0;
    transform: translateY(20px);
  }
  .about-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--accent), transparent);
    opacity: 0;
    transition: opacity 0.3s;
  }
  .about-card:hover { border-color: var(--accent); transform: translateY(-2px); }
  .about-card:hover::before { opacity: 1; }

  .about-card .emoji { font-size: 20px; margin-bottom: 10px; display: block; }
  .about-card .label { font-size: 10px; color: var(--muted); letter-spacing: 0.15em; text-transform: uppercase; margin-bottom: 8px; }
  .about-card .value { font-size: 13px; color: var(--text); line-height: 1.6; }
  .about-card .value strong { color: var(--accent); font-weight: 600; }

  /* ── TECH STACK ── */
  .stack-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }

  .stack-badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 6px 12px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 4px;
    font-size: 11px;
    color: var(--text);
    letter-spacing: 0.05em;
    cursor: default;
    transition: all 0.25s;
    opacity: 0;
    transform: scale(0.9);
  }
  .stack-badge:hover {
    border-color: var(--accent);
    color: var(--accent);
    box-shadow: 0 0 12px rgba(0,212,255,0.15);
    transform: scale(1.05);
  }
  .stack-badge .dot-badge {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: currentColor;
    opacity: 0.6;
  }

  /* Categories */
  .stack-category { margin-bottom: 28px; }
  .cat-title {
    font-size: 10px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--accent3);
    margin-bottom: 12px;
    padding-left: 2px;
  }

  /* ── SOCIALS ── */
  .socials-row {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
  }
  .social-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 20px;
    border: 1px solid var(--border);
    border-radius: 6px;
    background: var(--surface);
    color: var(--text);
    text-decoration: none;
    font-size: 12px;
    letter-spacing: 0.08em;
    transition: all 0.25s;
    font-family: 'JetBrains Mono', monospace;
  }
  .social-btn:hover {
    border-color: var(--accent);
    color: var(--accent);
    box-shadow: 0 0 20px rgba(0,212,255,0.1);
  }
  .social-btn svg { width: 16px; height: 16px; }

  /* ── STATS ── */
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
    gap: 16px;
  }
  .stat-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    overflow: hidden;
    transition: border-color 0.3s;
  }
  .stat-card:hover { border-color: var(--accent2); }
  .stat-card img { width: 100%; display: block; }
  .stat-label {
    padding: 10px 16px;
    font-size: 10px;
    color: var(--muted);
    letter-spacing: 0.1em;
    text-transform: uppercase;
  }

  /* ── QUOTE ── */
  .quote-box {
    background: var(--surface);
    border: 1px solid var(--border);
    border-left: 3px solid var(--accent2);
    border-radius: 8px;
    padding: 24px;
    text-align: center;
  }
  .quote-box img { max-width: 400px; width: 100%; }

  /* ── VISITOR ── */
  .visitor-row {
    display: flex;
    justify-content: center;
    padding: 20px 0 60px;
  }
  .visitor-row img { border-radius: 4px; }

  /* ── FOOTER ── */
  footer {
    border-top: 1px solid var(--border);
    padding: 24px 0;
    text-align: center;
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 0.1em;
  }
  footer span { color: var(--accent); }

  /* ── SCROLL PROGRESS ── */
  .progress-bar {
    position: fixed;
    top: 0; left: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--accent), var(--accent2));
    width: 0%;
    z-index: 9999;
    transition: width 0.1s;
  }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
  }
  @keyframes scanline {
    0% { transform: translateY(-100%); }
    100% { transform: translateY(100vh); }
  }

  .scanline {
    position: fixed;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(transparent, rgba(0,212,255,0.05), transparent);
    animation: scanline 6s linear infinite;
    pointer-events: none;
    z-index: 1;
  }

  /* Fade-in on scroll */
  .reveal { opacity: 0; transform: translateY(20px); transition: all 0.6s ease; }
  .reveal.visible { opacity: 1; transform: none; }
</style>
</head>
<body>

<div class="cursor" id="cursor"></div>
<div class="cursor-ring" id="cursorRing"></div>
<div class="progress-bar" id="progressBar"></div>
<div class="scanline"></div>

<div class="container">

  <!-- HEADER -->
  <header>
    <div class="terminal-bar">
      <div class="dot r"></div>
      <div class="dot y"></div>
      <div class="dot g"></div>
      <span class="terminal-path">~/<span>prakhar-shukla</span>/portfolio</span>
    </div>
    <h1 class="hero-name">
      <span class="line1">Prakhar</span>
      <span class="line2">Shukla</span>
    </h1>
    <p class="hero-sub">
      DevOps Engineer Intern &nbsp;·&nbsp; <em>Ex-Network Engineer @ HCL</em> &nbsp;·&nbsp; Lucknow, IN
    </p>
    <div class="typing-line">
      <span class="typed-text" id="typedText"></span><span class="cursor-blink">▊</span>
    </div>
  </header>

  <!-- ABOUT -->
  <section class="section">
    <div class="section-label">About</div>
    <div class="about-grid" id="aboutGrid">

      <div class="about-card">
        <span class="emoji">🔭</span>
        <div class="label">Currently</div>
        <div class="value">Working as <strong>DevOps Engineer Intern</strong></div>
      </div>

      <div class="about-card">
        <span class="emoji">🏢</span>
        <div class="label">Previously</div>
        <div class="value">Network Engineer at <strong>HCL</strong></div>
      </div>

      <div class="about-card">
        <span class="emoji">🤝</span>
        <div class="label">Open to Collaborate</div>
        <div class="value">DevOps automation, CI/CD pipelines, cloud infrastructure & containerized apps</div>
      </div>

      <div class="about-card">
        <span class="emoji">🆘</span>
        <div class="label">Seeking Help With</div>
        <div class="value">Advanced <strong>Kubernetes</strong>, cloud architecture best practices & production-scale deployments</div>
      </div>

      <div class="about-card">
        <span class="emoji">🌱</span>
        <div class="label">Currently Learning</div>
        <div class="value"><strong>Kubernetes</strong>, AWS services, Terraform (IaC) & advanced CI/CD practices</div>
      </div>

      <div class="about-card">
        <span class="emoji">💬</span>
        <div class="label">Ask Me About</div>
        <div class="value">Linux, Networking, Git, CI/CD, Docker & DevOps tools</div>
      </div>

      <div class="about-card">
        <span class="emoji">⚡</span>
        <div class="label">Fun Fact</div>
        <div class="value">I enjoy automating repetitive tasks and optimizing deployments 🚀</div>
      </div>

    </div>
  </section>

  <!-- SOCIALS -->
  <section class="section" style="padding-top:0">
    <div class="section-label reveal">Socials</div>
    <div class="socials-row reveal">
      <a href="https://www.linkedin.com/in/prakhar-shukla-267025191" target="_blank" class="social-btn">
        <svg fill="currentColor" viewBox="0 0 24 24"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        LinkedIn
      </a>
      <a href="mailto:prakharshuklatech@gmail.com" class="social-btn">
        <svg fill="currentColor" viewBox="0 0 24 24"><path d="M24 5.457v13.909c0 .904-.732 1.636-1.636 1.636h-3.819V11.73L12 16.64l-6.545-4.91v9.273H1.636A1.636 1.636 0 010 19.366V5.457c0-2.023 2.309-3.178 3.927-1.964L5.455 4.64 12 9.548l6.545-4.91 1.528-1.145C21.69 2.28 24 3.434 24 5.457z"/></svg>
        Email
      </a>
      <a href="https://github.com/PrakharShukla001" target="_blank" class="social-btn">
        <svg fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.374 0 0 5.373 0 12c0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23A11.509 11.509 0 0112 5.803c1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576C20.566 21.797 24 17.3 24 12c0-6.627-5.373-12-12-12z"/></svg>
        GitHub
      </a>
    </div>
  </section>

  <!-- TECH STACK -->
  <section class="section">
    <div class="section-label reveal">Tech Stack</div>

    <div class="stack-category reveal">
      <div class="cat-title">// Languages</div>
      <div class="stack-grid" id="stack-langs"></div>
    </div>

    <div class="stack-category reveal">
      <div class="cat-title">// Cloud Platforms</div>
      <div class="stack-grid" id="stack-cloud"></div>
    </div>

    <div class="stack-category reveal">
      <div class="cat-title">// DevOps & Infra</div>
      <div class="stack-grid" id="stack-devops"></div>
    </div>

    <div class="stack-category reveal">
      <div class="cat-title">// Servers & Databases</div>
      <div class="stack-grid" id="stack-db"></div>
    </div>

    <div class="stack-category reveal">
      <div class="cat-title">// VCS & Monitoring</div>
      <div class="stack-grid" id="stack-vcs"></div>
    </div>

    <div class="stack-category reveal">
      <div class="cat-title">// Design Tools</div>
      <div class="stack-grid" id="stack-design"></div>
    </div>
  </section>

  <!-- GITHUB STATS -->
  <section class="section">
    <div class="section-label reveal">GitHub Stats</div>
    <div class="stats-grid reveal">
      <div class="stat-card">
        <div class="stat-label">Overview</div>
        <img src="https://github-readme-stats.vercel.app/api?username=PrakharShukla001&theme=codeSTACKr&hide_border=true&include_all_commits=true&count_private=false" alt="GitHub Stats" loading="lazy">
      </div>
      <div class="stat-card">
        <div class="stat-label">Streak</div>
        <img src="https://nirzak-streak-stats.vercel.app/?user=PrakharShukla001&theme=codeSTACKr&hide_border=true" alt="Streak Stats" loading="lazy">
      </div>
      <div class="stat-card">
        <div class="stat-label">Top Languages</div>
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=PrakharShukla001&theme=codeSTACKr&hide_border=true&include_all_commits=true&count_private=false&layout=compact" alt="Top Languages" loading="lazy">
      </div>
    </div>
  </section>

  <!-- QUOTE -->
  <section class="section">
    <div class="section-label reveal">Dev Quote</div>
    <div class="quote-box reveal">
      <img src="https://quotes-github-readme.vercel.app/api?type=vertical&theme=radical" alt="Random Dev Quote" loading="lazy">
    </div>
  </section>

  <!-- VISITOR -->
  <div class="visitor-row reveal">
    <a href="https://visitcount.itsvg.in">
      <img src="https://visitcount.itsvg.in/api?id=PrakharShukla001&icon=2&color=1" alt="Visitor Count">
    </a>
  </div>

</div>

<!-- FOOTER -->
<footer>
  <div class="container">
    <span>Prakhar Shukla</span> &nbsp;·&nbsp; DevOps Engineer &nbsp;·&nbsp; Built with automation in mind 🚀
  </div>
</footer>

<script>
// ── Cursor ──
const cursor = document.getElementById('cursor');
const ring = document.getElementById('cursorRing');
let mx = 0, my = 0, rx = 0, ry = 0;
document.addEventListener('mousemove', e => { mx = e.clientX; my = e.clientY; });
function animateCursor() {
  cursor.style.left = mx - 5 + 'px';
  cursor.style.top  = my - 5 + 'px';
  rx += (mx - rx) * 0.12;
  ry += (my - ry) * 0.12;
  ring.style.left = rx - 18 + 'px';
  ring.style.top  = ry - 18 + 'px';
  requestAnimationFrame(animateCursor);
}
animateCursor();

// ── Scroll Progress ──
const bar = document.getElementById('progressBar');
window.addEventListener('scroll', () => {
  const pct = (window.scrollY / (document.body.scrollHeight - window.innerHeight)) * 100;
  bar.style.width = pct + '%';
});

// ── Typing Effect ──
const lines = [
  'echo "automating the boring stuff..."',
  'kubectl get pods --all-namespaces',
  'terraform apply --auto-approve',
  'docker-compose up -d && echo "deployed!"',
  'git push origin main --force-with-lease',
];
let li = 0, ci = 0, typing = true;
const el = document.getElementById('typedText');
function type() {
  const line = lines[li];
  if (typing) {
    el.textContent = line.slice(0, ci + 1);
    ci++;
    if (ci === line.length) { typing = false; setTimeout(type, 1800); return; }
  } else {
    el.textContent = line.slice(0, ci - 1);
    ci--;
    if (ci === 0) { typing = true; li = (li + 1) % lines.length; }
  }
  setTimeout(type, typing ? 55 : 28);
}
setTimeout(type, 800);

// ── Tech Stack Data ──
const stacks = {
  'stack-langs':  ['Apache Groovy','JavaScript','Python','Bash Script','PowerShell','Java'],
  'stack-cloud':  ['AWS','Azure','Google Cloud','Oracle Cloud','Alibaba Cloud','Cloudflare'],
  'stack-devops': ['Docker','Kubernetes','Terraform','Jenkins','GitHub Actions','Ansible'],
  'stack-db':     ['Apache','Nginx','Apache Tomcat','Apache Maven','MongoDB','MySQL','Redis'],
  'stack-vcs':    ['Git','GitHub','GitLab','Gitpod','Prometheus','Grafana','Jira'],
  'stack-design': ['Canva','Adobe Premiere Pro','Adobe Lightroom','Adobe'],
};

Object.entries(stacks).forEach(([id, items]) => {
  const container = document.getElementById(id);
  items.forEach((name, i) => {
    const badge = document.createElement('span');
    badge.className = 'stack-badge';
    badge.innerHTML = `<span class="dot-badge"></span>${name}`;
    badge.style.animationDelay = i * 0.05 + 's';
    container.appendChild(badge);
    setTimeout(() => {
      badge.style.transition = 'opacity 0.4s ease, transform 0.4s ease, border-color 0.25s, color 0.25s, box-shadow 0.25s';
      badge.style.opacity = '1';
      badge.style.transform = 'scale(1)';
    }, 500 + i * 60);
  });
});

// ── About Cards ──
const cards = document.querySelectorAll('.about-card');
cards.forEach((c, i) => {
  setTimeout(() => {
    c.style.transition = 'opacity 0.5s ease, transform 0.5s ease, border-color 0.3s';
    c.style.opacity = '1';
    c.style.transform = 'translateY(0)';
  }, 300 + i * 80);
});

// ── IntersectionObserver for .reveal ──
const io = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) { e.target.classList.add('visible'); io.unobserve(e.target); }
  });
}, { threshold: 0.12 });
document.querySelectorAll('.reveal').forEach(el => io.observe(el));
</script>
</body>
</html>
