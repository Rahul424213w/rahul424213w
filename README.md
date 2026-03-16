<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Rahul A K — GitHub Profile README</title>
  <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Mono:wght@400;500&family=Manrope:wght@400;500;600&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --navy:       #0d1321;
      --navy2:      #131d33;
      --navy3:      #1a2540;
      --navy4:      #243460;
      --blue:       #3a5aad;
      --blue-light: #5b7fd4;
      --blue-pale:  #c4d4f5;
      --teal:       #1d9e75;
      --teal-pale:  #6ed4b5;
      --amber:      #d4900a;
      --amber-pale: #f5c842;
      --red:        #e05252;
      --surface:    #f4f6f9;
      --card:       #ffffff;
      --card2:      #f7f9fd;
      --border:     #dde3ee;
      --border2:    #c8d2e8;
      --text1:      #1a2540;
      --text2:      #3d4f72;
      --text3:      #6b7fa8;
      --text4:      #9aabcc;
      --mono:       'DM Mono', monospace;
      --sans:       'Manrope', sans-serif;
      --display:    'Syne', sans-serif;
    }

    body {
      font-family: var(--sans);
      background: var(--surface);
      color: var(--text1);
      min-height: 100vh;
      padding: 2rem 1rem 4rem;
    }

    .page {
      max-width: 780px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    /* HERO */
    .hero {
      background: var(--navy);
      border-radius: 16px;
      padding: 2.5rem 2rem 2rem;
      position: relative;
      overflow: hidden;
    }

    .hero::before {
      content: '';
      position: absolute;
      top: -60px; right: -60px;
      width: 280px; height: 280px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(58,90,173,0.18) 0%, transparent 70%);
      pointer-events: none;
    }

    .hero::after {
      content: '';
      position: absolute;
      bottom: -40px; left: -40px;
      width: 200px; height: 200px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(29,158,117,0.1) 0%, transparent 70%);
      pointer-events: none;
    }

    .hero-inner {
      display: flex;
      gap: 1.5rem;
      align-items: center;
      position: relative;
      z-index: 1;
    }

    .avatar {
      width: 80px; height: 80px;
      border-radius: 50%;
      background: var(--navy3);
      border: 2px solid var(--blue);
      display: flex; align-items: center; justify-content: center;
      font-family: var(--mono);
      font-size: 22px; font-weight: 500;
      color: var(--blue-pale);
      flex-shrink: 0;
      letter-spacing: -1px;
    }

    .hero-name {
      font-family: var(--display);
      font-size: 30px;
      font-weight: 800;
      color: #eef1f8;
      line-height: 1.1;
      margin-bottom: 4px;
    }

    .hero-role {
      font-size: 13px;
      color: var(--text4);
      margin-bottom: 14px;
      letter-spacing: 0.01em;
    }

    .hero-badges { display: flex; flex-wrap: wrap; gap: 6px; }

    .hbadge {
      font-size: 11px;
      font-weight: 600;
      padding: 4px 11px;
      border-radius: 20px;
      letter-spacing: 0.03em;
    }

    .hb-blue  { background: #1b2f5e; color: #93b8f5; border: 1px solid #2d4a8a; }
    .hb-teal  { background: #0e3328; color: #5fcfaa; border: 1px solid #165c47; }
    .hb-amber { background: #3a2700; color: #f5c842; border: 1px solid #6a4800; }
    .hb-red   { background: #3a1212; color: #f59393; border: 1px solid #6a2020; }

    .hero-links {
      display: flex;
      gap: 10px;
      margin-top: 1.5rem;
      padding-top: 1.5rem;
      border-top: 1px solid rgba(255,255,255,0.07);
      flex-wrap: wrap;
      position: relative; z-index: 1;
    }

    .hlink {
      font-size: 12px;
      font-weight: 500;
      padding: 6px 14px;
      border-radius: 8px;
      border: 1px solid rgba(255,255,255,0.1);
      background: rgba(255,255,255,0.05);
      color: var(--text4);
      text-decoration: none;
      display: flex; align-items: center; gap: 6px;
      transition: all 0.2s;
      cursor: pointer;
    }

    .hlink:hover { background: rgba(58,90,173,0.25); color: var(--blue-pale); border-color: var(--blue); }

    .hlink-dot { width: 6px; height: 6px; border-radius: 50%; }

    /* CARDS */
    .card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 1.5rem;
    }

    .slabel {
      font-family: var(--display);
      font-size: 10px;
      font-weight: 700;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--blue);
      margin-bottom: 1rem;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .slabel::after {
      content: '';
      flex: 1;
      height: 1px;
      background: var(--border);
    }

    /* ABOUT */
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 8px;
    }

    .about-item {
      display: flex;
      gap: 10px;
      align-items: flex-start;
      font-size: 13.5px;
      color: var(--text2);
      line-height: 1.5;
      padding: 10px 12px;
      background: var(--card2);
      border: 1px solid var(--border);
      border-radius: 8px;
    }

    .ai-icon { font-size: 15px; flex-shrink: 0; }
    .about-item b { color: var(--text1); font-weight: 600; }

    .portfolio-row {
      display: flex;
      align-items: center;
      gap: 10px;
      margin-top: 8px;
      padding: 12px 14px;
      background: #f0f4ff;
      border: 1px solid #c4d4f5;
      border-radius: 8px;
      font-size: 13px;
      color: var(--blue);
      font-weight: 500;
    }

    .portfolio-row span { font-family: var(--mono); font-size: 12px; }

    /* STATS GRID */
    .stats-grid {
      display: grid;
      grid-template-columns: repeat(4, minmax(0, 1fr));
      gap: 10px;
      margin-bottom: 1rem;
    }

    .stat-box {
      background: var(--card2);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 16px 12px;
      text-align: center;
    }

    .stat-box .sn {
      font-family: var(--display);
      font-size: 26px;
      font-weight: 800;
      line-height: 1;
      margin-bottom: 4px;
    }

    .stat-box .sl {
      font-size: 10px;
      font-weight: 600;
      color: var(--text3);
      text-transform: uppercase;
      letter-spacing: 0.07em;
    }

    /* ACTIVITY BARS */
    .act-row {
      display: flex;
      align-items: center;
      gap: 10px;
      margin-bottom: 10px;
    }

    .act-label {
      font-size: 12px;
      font-weight: 500;
      color: var(--text2);
      width: 100px;
      flex-shrink: 0;
    }

    .act-bar-bg {
      flex: 1;
      height: 7px;
      background: var(--border);
      border-radius: 99px;
      overflow: hidden;
    }

    .act-bar { height: 100%; border-radius: 99px; }

    .act-pct {
      font-family: var(--mono);
      font-size: 11px;
      color: var(--text3);
      width: 36px;
      text-align: right;
      flex-shrink: 0;
    }

    /* TECH STACK */
    .tech-col { display: flex; flex-direction: column; gap: 1rem; }

    .tech-group h4 {
      font-size: 10px;
      font-weight: 700;
      color: var(--text3);
      text-transform: uppercase;
      letter-spacing: 0.08em;
      margin-bottom: 8px;
    }

    .pills { display: flex; flex-wrap: wrap; gap: 5px; }

    .pill {
      font-family: var(--mono);
      font-size: 11px;
      padding: 4px 10px;
      border-radius: 5px;
      background: var(--card2);
      border: 1px solid var(--border);
      color: var(--text1);
      transition: all 0.15s;
      cursor: default;
    }

    .pill:hover { background: #e8eefb; border-color: var(--blue); color: var(--blue); }

    /* LANG BARS */
    .lang-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }

    .lang-item { display: flex; flex-direction: column; gap: 5px; }

    .lang-meta { display: flex; justify-content: space-between; }

    .lang-name { font-size: 12px; font-weight: 600; color: var(--text2); }
    .lang-pct  { font-family: var(--mono); font-size: 11px; color: var(--text3); }

    .lang-bar-bg { height: 5px; background: var(--border); border-radius: 99px; overflow: hidden; }
    .lang-bar    { height: 100%; border-radius: 99px; }

    /* SKILLS */
    .skills-row { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }

    .skill-item { display: flex; flex-direction: column; gap: 5px; }

    .skill-meta { display: flex; justify-content: space-between; align-items: center; }

    .skill-name { font-size: 12.5px; font-weight: 600; color: var(--text2); }

    .skill-lvl {
      font-size: 10px; font-weight: 600;
      padding: 1px 7px; border-radius: 99px;
    }

    .lvl-pro { background: #e0f5ee; color: #0f6e56; }
    .lvl-int { background: #e8eefb; color: var(--blue); }
    .lvl-beg { background: #fff3cd; color: var(--amber); }

    .skill-bar-bg { height: 5px; background: var(--border); border-radius: 99px; overflow: hidden; }
    .skill-bar    { height: 100%; border-radius: 99px; }

    /* PROJECTS */
    .proj-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }

    .proj {
      background: var(--card2);
      border: 1px solid var(--border);
      border-left: 3px solid var(--blue);
      border-radius: 0 10px 10px 0;
      padding: 16px;
      transition: all 0.2s;
    }

    .proj:hover { border-left-color: var(--teal); background: #f0f4ff; }
    .proj-featured { border-left-color: var(--amber); }

    .proj-header {
      display: flex;
      align-items: flex-start;
      justify-content: space-between;
      gap: 8px;
      margin-bottom: 6px;
    }

    .proj-title {
      font-family: var(--display);
      font-size: 14px;
      font-weight: 700;
      color: var(--text1);
    }

    .proj-tag {
      font-size: 10px; font-weight: 600;
      padding: 2px 8px; border-radius: 99px;
      white-space: nowrap; flex-shrink: 0;
    }

    .pt-web  { background: #e8eefb; color: var(--blue); }
    .pt-ai   { background: #e0f5ee; color: var(--teal); }
    .pt-hack { background: #fff3cd; color: var(--amber); }

    .proj-desc {
      font-size: 12.5px; color: var(--text2);
      line-height: 1.55; margin-bottom: 10px;
    }

    .proj-chips { display: flex; gap: 5px; flex-wrap: wrap; }

    .proj-chip {
      font-family: var(--mono);
      font-size: 10px; padding: 2px 8px; border-radius: 4px;
      background: rgba(58,90,173,0.08);
      color: var(--blue);
      border: 1px solid rgba(58,90,173,0.15);
    }

    /* TIMELINE */
    .timeline { display: flex; flex-direction: column; }

    .tl-item {
      display: flex; gap: 14px;
      position: relative; padding-bottom: 20px;
    }

    .tl-item:last-child { padding-bottom: 0; }

    .tl-left {
      display: flex; flex-direction: column;
      align-items: center; flex-shrink: 0; width: 28px;
    }

    .tl-dot {
      width: 12px; height: 12px; border-radius: 50%;
      background: var(--blue);
      border: 2px solid var(--card);
      box-shadow: 0 0 0 2px var(--blue);
      flex-shrink: 0; z-index: 1;
    }

    .tl-line {
      flex: 1; width: 1px;
      background: var(--border2); margin-top: 4px;
    }

    .tl-item:last-child .tl-line { display: none; }

    .tl-content { flex: 1; padding-top: 0; }

    .tl-title {
      font-family: var(--display);
      font-size: 14px; font-weight: 700;
      color: var(--text1); margin-bottom: 2px;
    }

    .tl-meta { font-size: 11px; color: var(--text3); margin-bottom: 5px; font-weight: 500; }

    .tl-desc { font-size: 12.5px; color: var(--text2); line-height: 1.55; }

    /* CONNECT */
    .connect-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; }

    .conn-card {
      display: flex; flex-direction: column;
      align-items: center; gap: 8px;
      padding: 18px 12px;
      background: var(--card2);
      border: 1px solid var(--border);
      border-radius: 10px;
      text-decoration: none; color: var(--text2);
      transition: all 0.2s; cursor: pointer;
    }

    .conn-card:hover { border-color: var(--blue); background: #f0f4ff; color: var(--blue); }

    .conn-icon {
      width: 40px; height: 40px; border-radius: 10px;
      display: flex; align-items: center; justify-content: center;
      font-size: 18px;
    }

    .conn-name { font-size: 12px; font-weight: 600; }
    .conn-handle { font-family: var(--mono); font-size: 10px; color: var(--text4); }

    /* FACT */
    .fact-box {
      display: flex; gap: 14px; align-items: flex-start;
      background: var(--navy);
      border-radius: 12px; padding: 1.25rem 1.5rem;
    }

    .fact-q {
      font-family: var(--display);
      font-size: 36px; font-weight: 800;
      color: var(--blue); line-height: 1; flex-shrink: 0;
    }

    .fact-text {
      font-size: 14px; color: #8a9bbf;
      line-height: 1.7; font-style: italic;
    }

    .fact-text b { color: var(--blue-pale); font-style: normal; }

    /* FOOTER */
    .footer {
      text-align: center; font-size: 11px;
      color: var(--text4); padding-top: 0.5rem;
    }

    .footer span { font-family: var(--mono); color: var(--blue); }

    /* LAYOUT HELPERS */
    .two-col { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }

    /* ANIMATIONS */
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(16px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    .page > * { animation: fadeUp 0.5s ease both; }
    .page > *:nth-child(1) { animation-delay: 0.05s; }
    .page > *:nth-child(2) { animation-delay: 0.12s; }
    .page > *:nth-child(3) { animation-delay: 0.18s; }
    .page > *:nth-child(4) { animation-delay: 0.24s; }
    .page > *:nth-child(5) { animation-delay: 0.30s; }
    .page > *:nth-child(6) { animation-delay: 0.36s; }
    .page > *:nth-child(7) { animation-delay: 0.42s; }
    .page > *:nth-child(8) { animation-delay: 0.48s; }
    .page > *:nth-child(9) { animation-delay: 0.54s; }

    @media (max-width: 600px) {
      .two-col, .proj-grid, .about-grid, .connect-grid, .lang-grid, .skills-row { grid-template-columns: 1fr; }
      .stats-grid { grid-template-columns: repeat(2, 1fr); }
      .hero-inner { flex-direction: column; align-items: flex-start; }
    }
  </style>
</head>
<body>
<div class="page">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-inner">
      <div class="avatar">RA</div>
      <div style="flex:1;">
        <div class="hero-name">Rahul A K</div>
        <div class="hero-role">Computer Science Engineering Student &nbsp;·&nbsp; Belagavi, Karnataka, India</div>
        <div class="hero-badges">
          <span class="hbadge hb-blue">Web Development</span>
          <span class="hbadge hb-teal">AI &amp; Systems</span>
          <span class="hbadge hb-amber">DSA</span>
          <span class="hbadge hb-red">Open Source</span>
        </div>
      </div>
    </div>
    <div class="hero-links">
      <a class="hlink" href="https://rahul424213w.github.io/My-Portfolio/" target="_blank">
        <div class="hlink-dot" style="background:#5b7fd4;"></div> Portfolio
      </a>
      <a class="hlink" href="https://github.com/Rahul424213w" target="_blank">
        <div class="hlink-dot" style="background:#f0f6fc;"></div> GitHub
      </a>
      <a class="hlink" href="#" target="_blank">
        <div class="hlink-dot" style="background:#0a66c2;"></div> LinkedIn
      </a>
      <a class="hlink" href="mailto:rahul@example.com">
        <div class="hlink-dot" style="background:#f5c842;"></div> Email
      </a>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="card">
    <div class="slabel">About Me</div>
    <div class="about-grid">
      <div class="about-item"><span class="ai-icon">🎓</span><span>CSE student passionate about <b>building real-world tech products</b> that solve problems</span></div>
      <div class="about-item"><span class="ai-icon">💻</span><span>Focused on <b>Web Development, AI,</b> and <b>System Design</b></span></div>
      <div class="about-item"><span class="ai-icon">📚</span><span>Actively improving <b>DSA</b> skills and advanced development patterns</span></div>
      <div class="about-item"><span class="ai-icon">🏆</span><span>Participated in <b>3+ hackathons</b> — love building under pressure</span></div>
      <div class="about-item"><span class="ai-icon">🔬</span><span>Exploring <b>Machine Learning</b> and practical AI applications</span></div>
      <div class="about-item"><span class="ai-icon">🌱</span><span>Currently learning <b>TypeScript, Next.js</b> and cloud deployment</span></div>
    </div>
    <div class="portfolio-row">
      🌐 <span>rahul424213w.github.io/My-Portfolio</span>
    </div>
  </div>

  <!-- STATS -->
  <div class="card">
    <div class="slabel">GitHub Stats</div>
    <div class="stats-grid">
      <div class="stat-box">
        <div class="sn" style="color:var(--blue);">5+</div>
        <div class="sl">Projects</div>
      </div>
      <div class="stat-box">
        <div class="sn" style="color:var(--teal);">3+</div>
        <div class="sl">Hackathons</div>
      </div>
      <div class="stat-box">
        <div class="sn" style="color:var(--amber);">500+</div>
        <div class="sl">Commits</div>
      </div>
      <div class="stat-box">
        <div class="sn" style="color:var(--red);">⚡</div>
        <div class="sl">Active Streak</div>
      </div>
    </div>
    <div style="margin-top:1.25rem;">
      <div style="font-size:11px; font-weight:600; color:var(--text3); text-transform:uppercase; letter-spacing:.08em; margin-bottom: 12px;">Weekly Activity Split</div>
      <div class="act-row">
        <div class="act-label">Coding</div>
        <div class="act-bar-bg"><div class="act-bar" style="width:82%; background:var(--blue);"></div></div>
        <div class="act-pct">82%</div>
      </div>
      <div class="act-row">
        <div class="act-label">Learning</div>
        <div class="act-bar-bg"><div class="act-bar" style="width:70%; background:var(--teal);"></div></div>
        <div class="act-pct">70%</div>
      </div>
      <div class="act-row">
        <div class="act-label">Code Review</div>
        <div class="act-bar-bg"><div class="act-bar" style="width:55%; background:var(--amber);"></div></div>
        <div class="act-pct">55%</div>
      </div>
      <div class="act-row">
        <div class="act-label">Open Source</div>
        <div class="act-bar-bg"><div class="act-bar" style="width:38%; background:var(--red);"></div></div>
        <div class="act-pct">38%</div>
      </div>
    </div>
  </div>

  <!-- TECH STACK + LANGUAGES -->
  <div class="two-col">

    <div class="card">
      <div class="slabel">Tech Stack</div>
      <div class="tech-col">
        <div class="tech-group">
          <h4>Languages</h4>
          <div class="pills">
            <span class="pill">Python</span><span class="pill">Java</span>
            <span class="pill">JavaScript</span><span class="pill">C++</span><span class="pill">C</span>
          </div>
        </div>
        <div class="tech-group">
          <h4>Frontend</h4>
          <div class="pills">
            <span class="pill">React</span><span class="pill">HTML5</span>
            <span class="pill">CSS3</span><span class="pill">Tailwind</span>
          </div>
        </div>
        <div class="tech-group">
          <h4>Backend</h4>
          <div class="pills">
            <span class="pill">Node.js</span><span class="pill">Express</span><span class="pill">REST API</span>
          </div>
        </div>
        <div class="tech-group">
          <h4>Database &amp; Cloud</h4>
          <div class="pills">
            <span class="pill">MongoDB</span><span class="pill">Firebase</span><span class="pill">SQL</span>
          </div>
        </div>
        <div class="tech-group">
          <h4>DevTools</h4>
          <div class="pills">
            <span class="pill">Git</span><span class="pill">GitHub</span>
            <span class="pill">Linux</span><span class="pill">VS Code</span>
          </div>
        </div>
      </div>
    </div>

    <div style="display:flex; flex-direction:column; gap:1rem;">
      <div class="card">
        <div class="slabel">Top Languages</div>
        <div class="lang-grid">
          <div class="lang-item">
            <div class="lang-meta"><span class="lang-name">JavaScript</span><span class="lang-pct">38%</span></div>
            <div class="lang-bar-bg"><div class="lang-bar" style="width:38%; background:var(--amber);"></div></div>
          </div>
          <div class="lang-item">
            <div class="lang-meta"><span class="lang-name">Python</span><span class="lang-pct">27%</span></div>
            <div class="lang-bar-bg"><div class="lang-bar" style="width:27%; background:var(--blue);"></div></div>
          </div>
          <div class="lang-item">
            <div class="lang-meta"><span class="lang-name">Java</span><span class="lang-pct">18%</span></div>
            <div class="lang-bar-bg"><div class="lang-bar" style="width:18%; background:var(--teal);"></div></div>
          </div>
          <div class="lang-item">
            <div class="lang-meta"><span class="lang-name">C++</span><span class="lang-pct">11%</span></div>
            <div class="lang-bar-bg"><div class="lang-bar" style="width:11%; background:var(--red);"></div></div>
          </div>
          <div class="lang-item">
            <div class="lang-meta"><span class="lang-name">HTML/CSS</span><span class="lang-pct">6%</span></div>
            <div class="lang-bar-bg"><div class="lang-bar" style="width:6%; background:#9b59b6;"></div></div>
          </div>
        </div>
      </div>

      <div class="card">
        <div class="slabel">Skill Levels</div>
        <div class="skills-row">
          <div class="skill-item">
            <div class="skill-meta"><span class="skill-name">HTML/CSS</span><span class="skill-lvl lvl-pro">Proficient</span></div>
            <div class="skill-bar-bg"><div class="skill-bar" style="width:88%; background:var(--teal);"></div></div>
          </div>
          <div class="skill-item">
            <div class="skill-meta"><span class="skill-name">JavaScript</span><span class="skill-lvl lvl-pro">Proficient</span></div>
            <div class="skill-bar-bg"><div class="skill-bar" style="width:82%; background:var(--amber);"></div></div>
          </div>
          <div class="skill-item">
            <div class="skill-meta"><span class="skill-name">React</span><span class="skill-lvl lvl-int">Intermediate</span></div>
            <div class="skill-bar-bg"><div class="skill-bar" style="width:70%; background:var(--blue);"></div></div>
          </div>
          <div class="skill-item">
            <div class="skill-meta"><span class="skill-name">Python</span><span class="skill-lvl lvl-int">Intermediate</span></div>
            <div class="skill-bar-bg"><div class="skill-bar" style="width:72%; background:var(--blue);"></div></div>
          </div>
          <div class="skill-item">
            <div class="skill-meta"><span class="skill-name">Node.js</span><span class="skill-lvl lvl-int">Intermediate</span></div>
            <div class="skill-bar-bg"><div class="skill-bar" style="width:65%; background:var(--teal);"></div></div>
          </div>
          <div class="skill-item">
            <div class="skill-meta"><span class="skill-name">DSA</span><span class="skill-lvl lvl-beg">Learning</span></div>
            <div class="skill-bar-bg"><div class="skill-bar" style="width:50%; background:var(--amber);"></div></div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="card">
    <div class="slabel">Featured Projects</div>
    <div class="proj-grid">
      <div class="proj proj-featured">
        <div class="proj-header">
          <div class="proj-title">🚍 College Bus Tracking</div>
          <span class="proj-tag pt-web">Web</span>
        </div>
        <div class="proj-desc">Real-time bus location tracking with live ETA prediction using Google Maps API. Helps students plan commutes with up-to-the-minute arrival data.</div>
        <div class="proj-chips">
          <span class="proj-chip">React</span><span class="proj-chip">Node.js</span>
          <span class="proj-chip">Maps API</span><span class="proj-chip">Firebase</span>
        </div>
      </div>
      <div class="proj">
        <div class="proj-header">
          <div class="proj-title">🔎 TruthLens</div>
          <span class="proj-tag pt-ai">AI</span>
        </div>
        <div class="proj-desc">Information credibility analyzer that evaluates sources and flags misleading content. Combines NLP techniques with fact-checking heuristics.</div>
        <div class="proj-chips">
          <span class="proj-chip">Python</span><span class="proj-chip">NLP</span><span class="proj-chip">REST API</span>
        </div>
      </div>
      <div class="proj">
        <div class="proj-header">
          <div class="proj-title">🌐 Portfolio Website</div>
          <span class="proj-tag pt-web">Web</span>
        </div>
        <div class="proj-desc">Fully responsive developer portfolio with smooth animations, project showcases, and a contact form. Built with performance and accessibility in mind.</div>
        <div class="proj-chips">
          <span class="proj-chip">HTML/CSS</span><span class="proj-chip">JavaScript</span><span class="proj-chip">GitHub Pages</span>
        </div>
      </div>
      <div class="proj">
        <div class="proj-header">
          <div class="proj-title">🧠 Hackathon Projects</div>
          <span class="proj-tag pt-hack">Hackathon</span>
        </div>
        <div class="proj-desc">Multiple innovative solutions built under tight deadlines — spanning health tech, education, and civic tools across 3+ competitive events.</div>
        <div class="proj-chips">
          <span class="proj-chip">Various</span><span class="proj-chip">Rapid Prototyping</span>
        </div>
      </div>
    </div>
  </div>

  <!-- TIMELINE -->
  <div class="card">
    <div class="slabel">Experience &amp; Education</div>
    <div class="timeline">
      <div class="tl-item">
        <div class="tl-left"><div class="tl-dot"></div><div class="tl-line"></div></div>
        <div class="tl-content">
          <div class="tl-title">B.E. Computer Science Engineering</div>
          <div class="tl-meta">University · 2022 – Present</div>
          <div class="tl-desc">Studying core CS fundamentals: Data Structures, Algorithms, OS, DBMS, Computer Networks, and Software Engineering.</div>
        </div>
      </div>
      <div class="tl-item">
        <div class="tl-left"><div class="tl-dot" style="background:var(--teal);box-shadow:0 0 0 2px var(--teal);"></div><div class="tl-line"></div></div>
        <div class="tl-content">
          <div class="tl-title">Full-Stack Web Developer</div>
          <div class="tl-meta">Self-taught / Projects · 2023 – Present</div>
          <div class="tl-desc">Built multiple full-stack applications using React, Node.js, Express, and MongoDB. Deployed on GitHub Pages and Firebase.</div>
        </div>
      </div>
      <div class="tl-item">
        <div class="tl-left"><div class="tl-dot" style="background:var(--amber);box-shadow:0 0 0 2px var(--amber);"></div><div class="tl-line"></div></div>
        <div class="tl-content">
          <div class="tl-title">Hackathon Participant</div>
          <div class="tl-meta">Multiple Events · 2023 – Present</div>
          <div class="tl-desc">Competed in 3+ hackathons — built time-critical solutions in 24–48 hour sprints across health tech, AI, and civic categories.</div>
        </div>
      </div>
      <div class="tl-item">
        <div class="tl-left"><div class="tl-dot" style="background:var(--red);box-shadow:0 0 0 2px var(--red);"></div></div>
        <div class="tl-content">
          <div class="tl-title">DSA &amp; Competitive Programming</div>
          <div class="tl-meta">LeetCode / HackerRank · Ongoing</div>
          <div class="tl-desc">Actively solving DSA problems to strengthen problem-solving fundamentals — arrays, linked lists, trees, and dynamic programming.</div>
        </div>
      </div>
    </div>
  </div>

  <!-- CONNECT -->
  <div class="card">
    <div class="slabel">Connect With Me</div>
    <div class="connect-grid">
      <a class="conn-card" href="https://rahul424213w.github.io/My-Portfolio/" target="_blank">
        <div class="conn-icon" style="background:#e8eefb;">🌐</div>
        <div class="conn-name">Portfolio</div>
        <div class="conn-handle">rahul424213w.github.io</div>
      </a>
      <a class="conn-card" href="https://github.com/Rahul424213w" target="_blank">
        <div class="conn-icon" style="background:#f0f3fa;">🐙</div>
        <div class="conn-name">GitHub</div>
        <div class="conn-handle">@Rahul424213w</div>
      </a>
      <a class="conn-card" href="#" target="_blank">
        <div class="conn-icon" style="background:#e6f0ff;">💼</div>
        <div class="conn-name">LinkedIn</div>
        <div class="conn-handle">Add your handle</div>
      </a>
    </div>
  </div>

  <!-- QUOTE -->
  <div class="fact-box">
    <div class="fact-q">"</div>
    <div class="fact-text">
      I love <b>turning ideas into real, working products</b> — from concept sketches to deployed code. Every project is a chance to learn something new and leave something useful behind.
    </div>
  </div>

  <div class="footer">
    ⭐ Star a repo if you find it useful &nbsp;·&nbsp; Built with <span>HTML + CSS</span> · Rahul A K © 2025
  </div>

</div>
</body>
</html>
