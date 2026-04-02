<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Honey Sharma – GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=Space+Mono:wght@400;700&family=DM+Sans:ital,wght@0,300;0,400;0,600;1,300&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #0a0c10;
    --surface: #111318;
    --surface2: #181c23;
    --border: #1e2330;
    --gold: #f5c842;
    --gold2: #e0a820;
    --cyan: #00e5ff;
    --purple: #b57bee;
    --green: #39d353;
    --text: #e8ecf4;
    --muted: #6b7485;
    --accent: #ff6b6b;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Sans', sans-serif;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* ── HERO ── */
  .hero {
    position: relative;
    width: 100%;
    height: 260px;
    overflow: hidden;
    background: linear-gradient(135deg, #0d0f14 0%, #1a0a2e 40%, #0a1628 100%);
  }
  .hero-content {
    position: absolute;
    inset: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    z-index: 2;
  }
  .hero h1 {
    font-family: 'Syne', sans-serif;
    font-size: clamp(2.8rem, 6vw, 5rem);
    font-weight: 800;
    letter-spacing: -0.02em;
    background: linear-gradient(90deg, var(--gold) 0%, #fff 50%, var(--cyan) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    animation: shimmer 4s ease-in-out infinite;
    background-size: 200%;
  }
  @keyframes shimmer {
    0%, 100% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
  }
  .hero .sub {
    font-family: 'Space Mono', monospace;
    font-size: 0.82rem;
    color: var(--gold);
    letter-spacing: 0.18em;
    text-transform: uppercase;
    margin-top: 6px;
    opacity: 0.85;
  }

  /* grid dots bg */
  .hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background-image: radial-gradient(circle, rgba(245,200,66,.12) 1px, transparent 1px);
    background-size: 28px 28px;
    z-index: 1;
  }

  /* wave bottom */
  .wave-bottom {
    position: absolute;
    bottom: 0; left: 0; width: 100%;
    z-index: 3;
  }

  /* ── AVATAR BADGE ── */
  .avatar-row {
    display: flex;
    align-items: center;
    gap: 18px;
    padding: 30px 40px 0;
    position: relative;
    z-index: 10;
    margin-top: -38px;
  }
  .avatar {
    width: 76px; height: 76px;
    border-radius: 50%;
    border: 3px solid var(--gold);
    background: linear-gradient(135deg, #1a0a2e, #0a1628);
    display: flex; align-items: center; justify-content: center;
    font-size: 2rem;
    box-shadow: 0 0 20px rgba(245,200,66,.35);
    flex-shrink: 0;
  }
  .avatar-info h2 {
    font-family: 'Syne', sans-serif;
    font-size: 1.35rem;
    font-weight: 700;
    color: var(--text);
  }
  .avatar-info p {
    font-size: 0.78rem;
    color: var(--muted);
    margin-top: 2px;
  }
  .badge {
    display: inline-flex; align-items: center; gap: 5px;
    background: rgba(245,200,66,.1);
    border: 1px solid rgba(245,200,66,.3);
    border-radius: 20px;
    padding: 3px 10px;
    font-size: 0.68rem;
    font-family: 'Space Mono', monospace;
    color: var(--gold);
    margin-top: 5px;
  }
  .badge::before { content: '●'; font-size: 0.5rem; color: var(--green); }

  /* ── MAIN GRID ── */
  .container { padding: 28px 40px 60px; max-width: 900px; margin: 0 auto; }

  /* ── ABOUT ── */
  .about-box {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px 24px;
    margin-bottom: 24px;
    font-size: 0.88rem;
    line-height: 1.7;
    color: #b0b8cc;
    position: relative;
    overflow: hidden;
  }
  .about-box::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 3px; height: 100%;
    background: linear-gradient(180deg, var(--gold), var(--purple));
    border-radius: 3px 0 0 3px;
  }
  .about-box strong { color: var(--gold); }

  /* ── QUICK LINKS ── */
  .links-row {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-bottom: 24px;
  }
  .link-chip {
    display: inline-flex; align-items: center; gap: 6px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 6px 14px;
    font-size: 0.75rem;
    font-family: 'Space Mono', monospace;
    color: var(--muted);
    text-decoration: none;
    transition: all 0.2s;
    cursor: default;
  }
  .link-chip:hover { border-color: var(--gold); color: var(--gold); }
  .link-chip .icon { font-size: 0.9rem; }

  /* ── STATS CARDS ── */
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 14px;
    margin-bottom: 24px;
  }
  .stat-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 18px 16px;
    text-align: center;
    transition: transform 0.2s, border-color 0.2s;
    position: relative;
    overflow: hidden;
  }
  .stat-card:hover { transform: translateY(-3px); border-color: var(--gold); }
  .stat-card::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--gold), var(--cyan));
    opacity: 0;
    transition: opacity 0.2s;
  }
  .stat-card:hover::after { opacity: 1; }
  .stat-card .num {
    font-family: 'Syne', sans-serif;
    font-size: 2rem;
    font-weight: 800;
    color: var(--gold);
    line-height: 1;
  }
  .stat-card .label {
    font-size: 0.68rem;
    color: var(--muted);
    margin-top: 4px;
    text-transform: uppercase;
    letter-spacing: 0.1em;
  }

  /* ── SECTION HEADER ── */
  .section-header {
    display: flex;
    align-items: center;
    gap: 10px;
    margin: 28px 0 14px;
    font-family: 'Syne', sans-serif;
    font-size: 1rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--text);
  }
  .section-header::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--border), transparent);
  }
  .section-header .dot { color: var(--gold); font-size: 1.2rem; }

  /* ── TECH STACK ── */
  .tech-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(96px, 1fr));
    gap: 10px;
    margin-bottom: 10px;
  }
  .tech-pill {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 10px 8px;
    text-align: center;
    font-size: 0.72rem;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    transition: all 0.2s;
    display: flex; flex-direction: column; align-items: center; gap: 5px;
    cursor: default;
  }
  .tech-pill .ti { font-size: 1.4rem; }
  .tech-pill:hover {
    border-color: var(--cyan);
    color: var(--cyan);
    background: rgba(0,229,255,.05);
    transform: scale(1.04);
  }

  /* ── SKILLS TAGS ── */
  .skills-cloud {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 10px;
  }
  .skill-tag {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 4px 12px;
    font-size: 0.71rem;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    transition: all 0.18s;
    cursor: default;
  }
  .skill-tag:hover {
    background: rgba(181,123,238,.12);
    border-color: var(--purple);
    color: var(--purple);
  }

  /* ── PROJECTS ── */
  .projects-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 14px;
    margin-bottom: 10px;
  }
  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 18px 20px;
    transition: all 0.2s;
    position: relative;
    overflow: hidden;
  }
  .project-card:hover { border-color: var(--purple); transform: translateY(-2px); }
  .project-card .proj-icon { font-size: 1.6rem; margin-bottom: 8px; }
  .project-card h4 {
    font-family: 'Syne', sans-serif;
    font-size: 0.92rem;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 6px;
  }
  .project-card p { font-size: 0.76rem; color: var(--muted); line-height: 1.6; }
  .project-card .stack {
    margin-top: 10px;
    display: flex; flex-wrap: wrap; gap: 5px;
  }
  .stack-chip {
    background: rgba(181,123,238,.12);
    border: 1px solid rgba(181,123,238,.25);
    border-radius: 4px;
    padding: 2px 7px;
    font-size: 0.62rem;
    color: var(--purple);
    font-family: 'Space Mono', monospace;
  }

  /* ── LANGUAGE BAR ── */
  .lang-section {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 18px 22px;
    margin-bottom: 24px;
  }
  .lang-bar-wrap {
    display: flex;
    height: 8px;
    border-radius: 4px;
    overflow: hidden;
    margin: 12px 0;
    gap: 2px;
  }
  .lang-seg {
    border-radius: 4px;
    transition: filter 0.2s;
  }
  .lang-seg:hover { filter: brightness(1.3); }
  .lang-legend {
    display: flex; flex-wrap: wrap; gap: 14px;
  }
  .lang-item {
    display: flex; align-items: center; gap: 6px;
    font-size: 0.72rem; color: var(--muted);
    font-family: 'Space Mono', monospace;
  }
  .lang-dot { width: 8px; height: 8px; border-radius: 50%; }

  /* ── SNAKE ANIMATION ── */
  .snake-section {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px 24px;
    margin-bottom: 24px;
    overflow: hidden;
  }
  .snake-section h3 {
    font-family: 'Space Mono', monospace;
    font-size: 0.72rem;
    color: var(--muted);
    margin-bottom: 14px;
    text-transform: uppercase;
    letter-spacing: 0.12em;
  }
  #snakeCanvas {
    display: block;
    width: 100%;
    border-radius: 6px;
    cursor: none;
  }

  /* ── CONNECT ICONS ── */
  .connect-row {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-bottom: 10px;
  }
  .connect-btn {
    display: inline-flex; align-items: center; gap: 8px;
    padding: 8px 16px;
    border-radius: 8px;
    font-size: 0.72rem;
    font-family: 'Space Mono', monospace;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    border: none;
    cursor: pointer;
    transition: all 0.2s;
    text-decoration: none;
    color: #000;
  }
  .connect-btn:hover { transform: translateY(-2px); filter: brightness(1.12); }
  .btn-li  { background: #0a66c2; color: #fff; }
  .btn-ig  { background: linear-gradient(45deg,#f09433,#e6683c,#dc2743,#cc2366,#bc1888); color: #fff; }
  .btn-lc  { background: #ffa116; color: #000; }
  .btn-web { background: var(--gold); color: #000; }
  .btn-gh  { background: #e8ecf4; color: #0a0c10; }

  /* ── FOOTER ── */
  .footer {
    text-align: center;
    padding: 30px 20px 20px;
    font-size: 0.68rem;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    border-top: 1px solid var(--border);
  }
  .footer span { color: var(--gold); }

  /* ── SCROLL REVEAL ── */
  .reveal { opacity: 0; transform: translateY(22px); transition: all 0.55s cubic-bezier(.22,1,.36,1); }
  .reveal.shown { opacity: 1; transform: translateY(0); }
</style>
</head>
<body>

<!-- HERO -->
<div class="hero">
  <div class="hero-content">
    <h1>Honey Sharma</h1>
    <div class="sub">Co-Founder @ Throne8 &nbsp;·&nbsp; Bhopal, India</div>
  </div>
  <svg class="wave-bottom" viewBox="0 0 900 70" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg">
    <path d="M0,40 C150,80 350,0 500,40 C650,80 800,10 900,40 L900,70 L0,70 Z" fill="#0a0c10"/>
  </svg>
</div>

<!-- AVATAR ROW -->
<div class="avatar-row reveal">
  <div class="avatar">👑</div>
  <div class="avatar-info">
    <h2>Honey Sharma</h2>
    <p>Building India's AI-First Professional Networking Platform</p>
    <div class="badge">Available for Partnerships &amp; Collabs</div>
  </div>
</div>

<!-- MAIN CONTENT -->
<div class="container">

  <!-- ABOUT -->
  <div class="about-box reveal">
    Co-Founder at <strong>Throne8</strong> — building secure, scalable, AI-driven professional networking solutions. 
    I work at the intersection of <strong>AI, cloud infrastructure, and product-led growth</strong>, empowering students, professionals, and founders to grow through <strong>meaningful connections — not noise</strong>. 
    Passionate about backend systems, verified trust networks, and building in public. 📍 Bhopal, India &nbsp;|&nbsp; 🏗️ Founded 2025
  </div>

  <!-- QUICK LINKS -->
  <div class="links-row reveal">
    <a class="link-chip" href="https://www.throne8.com"><span class="icon">🌐</span> throne8.com</a>
    <a class="link-chip" href="https://www.linkedin.com/in/honey-sharma-228451249"><span class="icon">🔗</span> LinkedIn</a>
    <a class="link-chip" href="https://drive.google.com/file/d/1C7zHe96yw5km0LsVojZoPeFDagTXquiS/view"><span class="icon">📄</span> Resume</a>
    <a class="link-chip"><span class="icon">📰</span> TechSparks Newsletter · 1.6K subscribers</a>
    <a class="link-chip"><span class="icon">📍</span> Bhopal, Madhya Pradesh</a>
  </div>

  <!-- STATS -->
  <div class="section-header reveal"><span class="dot">◆</span> Highlights</div>
  <div class="stats-grid reveal">
    <div class="stat-card">
      <div class="num">7.6K</div>
      <div class="label">LinkedIn Followers</div>
    </div>
    <div class="stat-card">
      <div class="num">500+</div>
      <div class="label">Connections</div>
    </div>
    <div class="stat-card">
      <div class="num">1.6K</div>
      <div class="label">Newsletter Subs</div>
    </div>
    <div class="stat-card">
      <div class="num">Feb '25</div>
      <div class="label">Throne8 Founded</div>
    </div>
    <div class="stat-card">
      <div class="num">1,611</div>
      <div class="label">Company Followers</div>
    </div>
    <div class="stat-card">
      <div class="num">B.Tech</div>
      <div class="label">CS – OGI Bhopal</div>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="section-header reveal"><span class="dot">◆</span> Tech Stack</div>
  <div class="tech-grid reveal">
    <div class="tech-pill"><span class="ti">⚛️</span>React.js</div>
    <div class="tech-pill"><span class="ti">🅰️</span>Angular</div>
    <div class="tech-pill"><span class="ti">🔷</span>TypeScript</div>
    <div class="tech-pill"><span class="ti">🌊</span>Tailwind</div>
    <div class="tech-pill"><span class="ti">🔴</span>Redux</div>
    <div class="tech-pill"><span class="ti">🟢</span>Node.js</div>
    <div class="tech-pill"><span class="ti">🚂</span>Express.js</div>
    <div class="tech-pill"><span class="ti">🐦</span>NestJS</div>
    <div class="tech-pill"><span class="ti">🍃</span>MongoDB</div>
    <div class="tech-pill"><span class="ti">🐬</span>MySQL</div>
    <div class="tech-pill"><span class="ti">☁️</span>AWS</div>
    <div class="tech-pill"><span class="ti">🐳</span>Docker</div>
    <div class="tech-pill"><span class="ti">⎈</span>Kubernetes</div>
    <div class="tech-pill"><span class="ti">🧠</span>TensorFlow</div>
    <div class="tech-pill"><span class="ti">⛓️</span>Blockchain</div>
    <div class="tech-pill"><span class="ti">🔐</span>JWT Auth</div>
  </div>

  <!-- SKILLS -->
  <div class="section-header reveal"><span class="dot">◆</span> Skills</div>
  <div class="skills-cloud reveal">
    <span class="skill-tag">Entrepreneurship</span>
    <span class="skill-tag">Startup Leadership</span>
    <span class="skill-tag">Product Strategy</span>
    <span class="skill-tag">Backend Architecture</span>
    <span class="skill-tag">DevOps & Cloud (AWS)</span>
    <span class="skill-tag">Go-to-Market Strategy</span>
    <span class="skill-tag">System Design</span>
    <span class="skill-tag">Microservices</span>
    <span class="skill-tag">REST APIs</span>
    <span class="skill-tag">AI Foundations</span>
    <span class="skill-tag">Blockchain Concepts</span>
    <span class="skill-tag">Business Development</span>
    <span class="skill-tag">MERN Stack</span>
    <span class="skill-tag">MEAN Stack</span>
    <span class="skill-tag">CI/CD Pipelines</span>
    <span class="skill-tag">Leadership</span>
    <span class="skill-tag">Networking Platforms</span>
    <span class="skill-tag">React Native</span>
    <span class="skill-tag">Next.js</span>
    <span class="skill-tag">Redis</span>
    <span class="skill-tag">Terraform</span>
    <span class="skill-tag">Passport.js</span>
    <span class="skill-tag">Communication</span>
  </div>

  <!-- PROJECTS -->
  <div class="section-header reveal"><span class="dot">◆</span> Featured Projects</div>
  <div class="projects-grid reveal">
    <div class="project-card">
      <div class="proj-icon">📧</div>
      <h4>Email Application</h4>
      <p>Scalable email platform with real-time UI, optimized API flows, and seamless UX.</p>
      <div class="stack">
        <span class="stack-chip">React</span>
        <span class="stack-chip">Redux Toolkit</span>
        <span class="stack-chip">Axios</span>
        <span class="stack-chip">Tailwind</span>
        <span class="stack-chip">Vite</span>
      </div>
    </div>
    <div class="project-card">
      <div class="proj-icon">📌</div>
      <h4>Booking Application</h4>
      <p>Secure service booking system with authentication, role management and REST APIs.</p>
      <div class="stack">
        <span class="stack-chip">MERN</span>
        <span class="stack-chip">JWT</span>
        <span class="stack-chip">REST API</span>
        <span class="stack-chip">MongoDB</span>
      </div>
    </div>
    <div class="project-card">
      <div class="proj-icon">👑</div>
      <h4>Throne8 Platform</h4>
      <p>India's AI-First professional networking platform with verified trust systems and mentorship engine.</p>
      <div class="stack">
        <span class="stack-chip">AI/ML</span>
        <span class="stack-chip">NestJS</span>
        <span class="stack-chip">AWS</span>
        <span class="stack-chip">Blockchain</span>
      </div>
    </div>
    <div class="project-card">
      <div class="proj-icon">📰</div>
      <h4>TechSparks Newsletter</h4>
      <p>Weekly tech insights delivered to 1,691 subscribers covering trends, tools, and innovation.</p>
      <div class="stack">
        <span class="stack-chip">Content</span>
        <span class="stack-chip">Growth</span>
        <span class="stack-chip">LinkedIn</span>
      </div>
    </div>
  </div>

  <!-- LANGUAGE BARS -->
  <div class="section-header reveal"><span class="dot">◆</span> Most Used Languages</div>
  <div class="lang-section reveal">
    <div class="lang-bar-wrap">
      <div class="lang-seg" style="width:38%; background:#3178c6;" title="TypeScript 38%"></div>
      <div class="lang-seg" style="width:22%; background:#f0db4f;" title="JavaScript 22%"></div>
      <div class="lang-seg" style="width:14%; background:#68a063;" title="Node.js 14%"></div>
      <div class="lang-seg" style="width:12%; background:#e0234e;" title="NestJS 12%"></div>
      <div class="lang-seg" style="width:8%; background:#47a248;" title="MongoDB 8%"></div>
      <div class="lang-seg" style="width:6%; background:#ff9900;" title="AWS/DevOps 6%"></div>
    </div>
    <div class="lang-legend">
      <div class="lang-item"><div class="lang-dot" style="background:#3178c6;"></div>TypeScript 38%</div>
      <div class="lang-item"><div class="lang-dot" style="background:#f0db4f;"></div>JavaScript 22%</div>
      <div class="lang-item"><div class="lang-dot" style="background:#68a063;"></div>Node.js 14%</div>
      <div class="lang-item"><div class="lang-dot" style="background:#e0234e;"></div>NestJS 12%</div>
      <div class="lang-item"><div class="lang-dot" style="background:#47a248;"></div>MongoDB 8%</div>
      <div class="lang-item"><div class="lang-dot" style="background:#ff9900;"></div>AWS/DevOps 6%</div>
    </div>
  </div>

  <!-- CONTRIBUTION SNAKE -->
  <div class="section-header reveal"><span class="dot">◆</span> Contribution Graph</div>
  <div class="snake-section reveal">
    <h3>🐍 snake eating my contributions...</h3>
    <canvas id="snakeCanvas" width="820" height="90"></canvas>
  </div>

  <!-- CONNECT -->
  <div class="section-header reveal"><span class="dot">◆</span> Connect With Me</div>
  <div class="connect-row reveal">
    <a class="connect-btn btn-li" href="https://www.linkedin.com/in/honey-sharma-228451249">🔗 LinkedIn</a>
    <a class="connect-btn btn-ig" href="https://instagram.com/honey__sharma__02">📸 Instagram</a>
    <a class="connect-btn btn-web" href="https://www.throne8.com">👑 Throne8</a>
    <a class="connect-btn btn-gh" href="https://github.com/honey9876">🐙 GitHub</a>
  </div>

</div>

<div class="footer">
  Made with <span>♥</span> by Honey Sharma &nbsp;·&nbsp; Co-Founder @ Throne8 &nbsp;·&nbsp; Bhopal, India &nbsp;·&nbsp; <span>2025 – Present</span>
</div>

<script>
// ── SCROLL REVEAL ──
const reveals = document.querySelectorAll('.reveal');
const observer = new IntersectionObserver((entries) => {
  entries.forEach((e, i) => {
    if (e.isIntersecting) {
      setTimeout(() => e.target.classList.add('shown'), 60 * [...reveals].indexOf(e.target) % 5);
      observer.unobserve(e.target);
    }
  });
}, { threshold: 0.1 });
reveals.forEach(el => observer.observe(el));

// ── SNAKE CANVAS ──
const canvas = document.getElementById('snakeCanvas');
const ctx = canvas.getContext('2d');

const COLS = 52, ROWS = 6;
const CELL = Math.floor(canvas.width / COLS);
canvas.height = ROWS * CELL;

// generate fake commit grid
const grid = [];
for (let r = 0; r < ROWS; r++) {
  grid[r] = [];
  for (let c = 0; c < COLS; c++) {
    const v = Math.random();
    grid[r][c] = v < 0.35 ? 0 : v < 0.55 ? 1 : v < 0.72 ? 2 : v < 0.87 ? 3 : 4;
  }
}

// shade map
const shades = ['#161b22', '#0e4429', '#006d32', '#26a641', '#39d353'];

// snake state
let snake = [{r: 2, c: 0}];
for (let i = 1; i < 8; i++) snake.push({r: 2, c: -i});
let dir = {dr: 0, dc: 1};
let eaten = new Set();
let frame = 0;

function drawGrid() {
  for (let r = 0; r < ROWS; r++) {
    for (let c = 0; c < COLS; c++) {
      const key = `${r},${c}`;
      const v = eaten.has(key) ? 0 : grid[r][c];
      ctx.fillStyle = shades[v];
      ctx.beginPath();
      ctx.roundRect(c * CELL + 1, r * CELL + 1, CELL - 2, CELL - 2, 2);
      ctx.fill();
    }
  }
}

function drawSnake() {
  snake.forEach((seg, i) => {
    if (seg.c < 0 || seg.c >= COLS || seg.r < 0 || seg.r >= ROWS) return;
    const isHead = i === 0;
    ctx.fillStyle = isHead ? '#b57bee' : `rgba(181,123,238,${0.9 - i * 0.05})`;
    ctx.beginPath();
    ctx.roundRect(seg.c * CELL + 1, seg.r * CELL + 1, CELL - 2, CELL - 2, isHead ? 3 : 2);
    ctx.fill();
    // eyes on head
    if (isHead) {
      ctx.fillStyle = '#fff';
      const ex = seg.c * CELL + CELL * 0.65;
      const ey = seg.r * CELL + CELL * 0.3;
      ctx.beginPath(); ctx.arc(ex, ey, 1.5, 0, Math.PI * 2); ctx.fill();
    }
  });
}

function nextCell(r, c) {
  // find a target cell with commits
  for (let dc = 1; dc <= COLS; dc++) {
    const nc = c + dc;
    if (nc >= COLS) {
      // wrap: go down a row
      return {dr: 1, dc: 0};
    }
    const key = `${r},${nc}`;
    if (!eaten.has(key) && grid[r][nc] > 0) return {dr: 0, dc: 1};
  }
  return {dr: 0, dc: 1};
}

function step() {
  frame++;
  if (frame % 3 !== 0) { requestAnimationFrame(loop); return; }

  const head = snake[0];
  
  // smart pathfinding: prefer cells with commits
  let nd = dir;
  const ahead = {r: head.r + dir.dr, c: head.c + dir.dc};
  
  // if out of row or eaten, try to go down
  if (ahead.c >= COLS) {
    nd = {dr: 1, dc: 0};
  } else if (ahead.r >= ROWS) {
    // reset
    snake = [{r: 0, c: -1}];
    for (let i = 1; i < 8; i++) snake.push({r: 0, c: -1 - i});
    eaten.clear();
    dir = {dr: 0, dc: 1};
    requestAnimationFrame(loop); return;
  } else {
    const key = `${ahead.r},${ahead.c}`;
    if (eaten.has(key) || grid[ahead.r][ahead.c] === 0) {
      // try same row scanning
      let found = false;
      for (let dc = 1; dc <= COLS - head.c; dc++) {
        const nc = head.c + dc;
        const nk = `${head.r},${nc}`;
        if (!eaten.has(nk) && grid[head.r][nc] > 0) { nd = {dr: 0, dc: 1}; found = true; break; }
      }
      if (!found && head.r + 1 < ROWS) nd = {dr: 1, dc: 0};
    }
  }
  
  dir = nd;
  const newHead = {r: head.r + dir.dr, c: head.c + dir.dc};
  snake.unshift(newHead);

  const eatKey = `${newHead.r},${newHead.c}`;
  if (newHead.r >= 0 && newHead.c >= 0 && newHead.c < COLS && !eaten.has(eatKey) && grid[newHead.r] && grid[newHead.r][newHead.c] > 0) {
    eaten.add(eatKey);
  } else {
    snake.pop();
  }

  requestAnimationFrame(loop);
}

function loop() {
  ctx.clearRect(0, 0, canvas.width, canvas.height);
  drawGrid();
  drawSnake();
  step();
}

loop();
</script>
</body>
</html>
