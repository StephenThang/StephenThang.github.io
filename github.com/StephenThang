<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Stephen Vanlian Thang | Cybersecurity Portfolio</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400;500;700&family=Syne:wght@400;700;800&display=swap" rel="stylesheet" />
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --bg: #0a0c0f;
      --bg-card: #0d1117;
      --bg-surface: #161b22;
      --border: #30363d;
      --border-dim: #21262d;
      --text: #c9d1d9;
      --text-bright: #e6edf3;
      --text-muted: #8b949e;
      --text-dim: #484f58;
      --accent: #1f6feb;
      --accent-light: #58a6ff;
      --green: #3fb950;
    }

    html { scroll-behavior: smooth; }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: 'JetBrains Mono', monospace;
      font-size: 14px;
      line-height: 1.7;
    }

    ::-webkit-scrollbar { width: 4px; }
    ::-webkit-scrollbar-track { background: var(--bg); }
    ::-webkit-scrollbar-thumb { background: var(--accent); border-radius: 2px; }

    a { color: var(--accent-light); text-decoration: none; }
    a:hover { color: var(--accent); }

    .container { max-width: 920px; margin: 0 auto; padding: 0 2rem; }

    /* ── NAV ── */
    nav {
      position: sticky; top: 0; z-index: 100;
      background: rgba(10,12,15,0.92);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid var(--border-dim);
      padding: 0.9rem 0;
    }
    .nav-inner {
      max-width: 920px; margin: 0 auto; padding: 0 2rem;
      display: flex; align-items: center; justify-content: space-between;
    }
    .nav-logo { font-family: 'Syne', sans-serif; font-weight: 800; font-size: 1.05rem; color: var(--text-bright); letter-spacing: -0.5px; }
    .nav-logo span { color: var(--accent); }
    nav ul { list-style: none; display: flex; gap: 1.75rem; }
    nav ul a { color: var(--text-muted); font-size: 11px; letter-spacing: 1.2px; text-transform: uppercase; transition: color 0.2s; }
    nav ul a:hover { color: var(--accent-light); }
    .nav-resume {
      background: transparent; border: 1px solid var(--border);
      color: var(--text-muted); font-family: 'JetBrains Mono', monospace;
      font-size: 11px; padding: 5px 14px; border-radius: 5px; cursor: pointer;
      transition: all 0.2s; letter-spacing: 0.5px;
    }
    .nav-resume:hover { border-color: var(--accent-light); color: var(--accent-light); }

    /* ── HERO ── */
    .hero {
      min-height: 92vh; display: flex; align-items: center;
      padding: 5rem 0 4rem;
      border-bottom: 1px solid var(--border-dim);
    }
    .terminal-window {
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: 12px; width: 100%; overflow: hidden;
      box-shadow: 0 0 60px rgba(31,111,235,0.06);
    }
    .terminal-bar {
      background: var(--bg-surface); padding: 10px 16px;
      display: flex; align-items: center; gap: 8px;
      border-bottom: 1px solid var(--border);
    }
    .dot { width: 12px; height: 12px; border-radius: 50%; }
    .dot.r { background: #ff5f57; }
    .dot.y { background: #febc2e; }
    .dot.g { background: #28c840; }
    .tbar-title { margin-left: 8px; color: var(--text-muted); font-size: 12px; }
    .terminal-body { padding: 2.5rem; }
    .t-line { color: var(--text-muted); font-size: 13px; margin-bottom: 0.2rem; }
    .t-prompt { color: var(--green); }
    .t-path { color: var(--accent-light); }
    .t-cmd { color: var(--text-bright); }
    .hero-name {
      font-family: 'Syne', sans-serif; font-weight: 800;
      font-size: clamp(2.2rem, 5.5vw, 3.8rem);
      color: var(--text-bright); line-height: 1.08;
      margin: 1.1rem 0 0.4rem; letter-spacing: -1.5px;
    }
    .hero-name .accent { color: var(--accent); }
    .hero-sub { color: var(--text-muted); font-size: 13px; margin-bottom: 1.6rem; }
    .hero-badges { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 1.8rem; }
    .badge {
      background: var(--bg-surface); border: 1px solid var(--border);
      padding: 4px 11px; border-radius: 4px; font-size: 11px; color: var(--text-muted);
    }
    .badge.hi { border-color: var(--accent); color: var(--accent-light); }
    .cta-row { display: flex; gap: 12px; flex-wrap: wrap; margin-top: 1.6rem; }
    .btn {
      padding: 9px 22px; border-radius: 7px;
      font-family: 'JetBrains Mono', monospace; font-size: 12px;
      cursor: pointer; transition: all 0.2s; display: inline-block;
    }
    .btn-primary { background: var(--accent); color: #fff; border: 1px solid var(--accent); }
    .btn-primary:hover { background: #388bfd; border-color: #388bfd; color: #fff; }
    .btn-ghost { background: transparent; color: var(--text-muted); border: 1px solid var(--border); }
    .btn-ghost:hover { border-color: var(--text-muted); color: var(--text-bright); }
    .cursor { display: inline-block; width: 8px; height: 15px; background: var(--green); vertical-align: middle; animation: blink 1s step-end infinite; }
    @keyframes blink { 50% { opacity: 0; } }

    /* ── SECTIONS ── */
    section { padding: 5.5rem 0; border-bottom: 1px solid var(--border-dim); }
    .sec-label { font-size: 11px; color: var(--accent); letter-spacing: 2.5px; text-transform: uppercase; margin-bottom: 0.4rem; }
    .sec-title { font-family: 'Syne', sans-serif; font-weight: 700; font-size: 1.9rem; color: var(--text-bright); margin-bottom: 2.5rem; }

    /* ── ABOUT ── */
    .about-grid { display: grid; grid-template-columns: 1.2fr 0.8fr; gap: 3rem; align-items: start; }
    .about-text p { color: var(--text-muted); margin-bottom: 1rem; font-size: 13px; line-height: 1.85; }
    .about-text p strong { color: var(--text); }
    .about-text .gpa { color: var(--accent-light); font-weight: 500; }
    .stat-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
    .stat-card {
      background: var(--bg-card); border: 1px solid var(--border);
      border-radius: 9px; padding: 1.1rem; text-align: center;
    }
    .stat-num { font-family: 'Syne', sans-serif; font-size: 1.9rem; font-weight: 800; color: var(--accent); }
    .stat-lbl { font-size: 11px; color: var(--text-muted); margin-top: 4px; line-height: 1.4; }
    .lang-row { margin-top: 1.5rem; }
    .lang-row h4 { color: var(--accent-light); font-size: 11px; letter-spacing: 1.5px; text-transform: uppercase; margin-bottom: 0.6rem; }
    .lang-tag {
      display: inline-block; background: var(--bg-surface); border: 1px solid var(--border);
      border-radius: 4px; padding: 3px 9px; font-size: 12px; color: var(--text); margin: 3px 3px 3px 0;
    }

    /* ── SKILLS ── */
    .skills-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(210px, 1fr)); gap: 1.75rem; }
    .skill-cat h4 { color: var(--accent-light); font-size: 11px; letter-spacing: 1.5px; text-transform: uppercase; margin-bottom: 0.75rem; padding-bottom: 0.5rem; border-bottom: 1px solid var(--border-dim); }
    .skill-tag {
      display: inline-block; background: var(--bg-surface); border: 1px solid var(--border-dim);
      border-radius: 4px; padding: 3px 9px; font-size: 12px; color: var(--text); margin: 3px 3px 3px 0;
      transition: border-color 0.2s;
    }
    .skill-tag:hover { border-color: var(--accent); color: var(--accent-light); }

    /* ── EXPERIENCE ── */
    .exp-list { display: flex; flex-direction: column; gap: 0; }
    .exp-item {
      display: grid; grid-template-columns: 160px 1fr; gap: 2rem;
      padding: 1.75rem 0; border-bottom: 1px solid var(--border-dim);
    }
    .exp-item:first-child { padding-top: 0; }
    .exp-item:last-child { border-bottom: none; }
    .exp-date { color: var(--accent); font-size: 11px; padding-top: 3px; line-height: 1.6; }
    .exp-role { font-family: 'Syne', sans-serif; color: var(--text-bright); font-weight: 700; font-size: 1rem; margin-bottom: 2px; }
    .exp-org { color: var(--accent-light); font-size: 12px; margin-bottom: 0.6rem; }
    .exp-desc { color: var(--text-muted); font-size: 12px; line-height: 1.85; }
    .exp-desc ul { margin-top: 0.4rem; padding-left: 1.2rem; }
    .exp-desc li { margin-bottom: 0.35rem; }

    /* ── PROJECTS ── */
    .projects-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(270px, 1fr)); gap: 1.5rem; }
    .project-card {
      background: var(--bg-card); border: 1px solid var(--border);
      border-radius: 11px; padding: 1.6rem;
      transition: border-color 0.2s, transform 0.2s;
      display: flex; flex-direction: column;
    }
    .project-card:hover { border-color: var(--accent); transform: translateY(-4px); }
    .proj-header { display: flex; justify-content: space-between; align-items: flex-start; margin-bottom: 0.8rem; }
    .proj-icon { font-size: 22px; }
    .proj-links a { color: var(--text-muted); font-size: 11px; margin-left: 8px; letter-spacing: 0.5px; }
    .proj-links a:hover { color: var(--accent-light); }
    .project-card h3 { font-family: 'Syne', sans-serif; color: var(--text-bright); font-size: 1rem; font-weight: 700; margin-bottom: 0.5rem; }
    .project-card p { color: var(--text-muted); font-size: 12px; line-height: 1.75; margin-bottom: 1rem; flex: 1; }
    .proj-tags { display: flex; flex-wrap: wrap; gap: 6px; margin-top: auto; }
    .proj-tag { background: var(--bg-surface); border: 1px solid var(--border-dim); border-radius: 4px; padding: 2px 8px; font-size: 11px; color: var(--text-muted); }

    /* ── CERTS ── */
    .certs-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 1.25rem; }
    .cert-card {
      background: var(--bg-card); border: 1px solid var(--border);
      border-radius: 10px; padding: 1.25rem 1.4rem;
      display: flex; align-items: flex-start; gap: 1rem;
      transition: border-color 0.2s;
    }
    .cert-card:hover { border-color: var(--accent); }
    .cert-icon { font-size: 22px; margin-top: 2px; flex-shrink: 0; }
    .cert-name { font-family: 'Syne', sans-serif; color: var(--text-bright); font-weight: 700; font-size: 0.9rem; margin-bottom: 3px; }
    .cert-issuer { color: var(--accent-light); font-size: 11px; }
    .cert-date { color: var(--text-dim); font-size: 11px; margin-top: 3px; }

    /* ── CONTACT ── */
    .contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 3rem; }
    .contact-note { color: var(--text-muted); font-size: 13px; line-height: 1.85; margin-bottom: 1.75rem; }
    .contact-note strong { color: var(--text); }
    .contact-links { display: flex; flex-direction: column; gap: 10px; }
    .contact-link {
      display: flex; align-items: center; gap: 14px;
      background: var(--bg-card); border: 1px solid var(--border);
      border-radius: 9px; padding: 0.9rem 1.1rem; transition: border-color 0.2s;
      text-decoration: none;
    }
    .contact-link:hover { border-color: var(--accent); }
    .contact-link .ci { color: var(--accent); font-size: 14px; width: 22px; text-align: center; flex-shrink: 0; }
    .contact-link .cl { color: var(--text-muted); font-size: 11px; letter-spacing: 0.5px; text-transform: uppercase; }
    .contact-link .cv { color: var(--text); font-size: 12px; margin-top: 2px; }
    .contact-form {
      background: var(--bg-card); border: 1px solid var(--border);
      border-radius: 11px; padding: 1.75rem;
    }
    .form-label { color: var(--green); font-size: 12px; margin-bottom: 1rem; }
    .form-input {
      width: 100%; background: var(--bg-surface); border: 1px solid var(--border);
      border-radius: 6px; padding: 9px 13px; color: var(--text);
      font-family: 'JetBrains Mono', monospace; font-size: 12px;
      margin-bottom: 10px; outline: none; transition: border-color 0.2s;
    }
    .form-input:focus { border-color: var(--accent); }
    .form-textarea { resize: vertical; min-height: 90px; }
    .form-btn {
      width: 100%; background: var(--accent); color: #fff; border: none;
      border-radius: 7px; padding: 10px; font-family: 'JetBrains Mono', monospace;
      font-size: 12px; cursor: pointer; transition: background 0.2s; letter-spacing: 0.5px;
    }
    .form-btn:hover { background: #388bfd; }

    /* ── FOOTER ── */
    footer {
      padding: 2.5rem 0; text-align: center;
      color: var(--text-dim); font-size: 11px; letter-spacing: 0.5px; line-height: 1.9;
    }

    /* ── RESPONSIVE ── */
    @media (max-width: 700px) {
      .about-grid, .contact-grid { grid-template-columns: 1fr; }
      .exp-item { grid-template-columns: 1fr; gap: 0.4rem; }
      .stat-grid { grid-template-columns: 1fr 1fr; }
      nav ul { display: none; }
    }
  </style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-inner">
    <div class="nav-logo">s<span>.</span>thang</div>
    <ul>
      <li><a href="#about">about</a></li>
      <li><a href="#skills">skills</a></li>
      <li><a href="#experience">experience</a></li>
      <li><a href="#projects">projects</a></li>
      <li><a href="#certs">certs</a></li>
      <li><a href="#contact">contact</a></li>
    </ul>
    <a href="mailto:svthang@terpmail.umd.edu" class="nav-resume">hire me ↗</a>
  </div>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="container">
    <div class="terminal-window">
      <div class="terminal-bar">
        <div class="dot r"></div><div class="dot y"></div><div class="dot g"></div>
        <span class="tbar-title">~/stephen-thang — bash — 80×24</span>
      </div>
      <div class="terminal-body">
        <div class="t-line"><span class="t-prompt">svthang@sentinel</span><span class="t-path">:~$</span> <span class="t-cmd">cat whoami.txt</span></div>
        <div class="hero-name">Stephen<br><span class="accent">Vanlian Thang</span></div>
        <div class="hero-sub">// cybersecurity analyst · human-centered security · UMD '26</div>
        <div class="hero-badges">
          <span class="badge hi">CEH Certified</span>
          <span class="badge hi">Google Cybersecurity</span>
          <span class="badge hi">DoD Cyber Sentinel × 2</span>
          <span class="badge">B.S. Psychology</span>
          <span class="badge">B.S. Information Science</span>
          <span class="badge">M.S. Information Systems</span>
          <span class="badge">GPA 3.75</span>
          <span class="badge">U.S. Citizen</span>
          <span class="badge">Multilingual × 4</span>
        </div>
        <div class="t-line" style="margin-top:0.5rem;"><span class="t-prompt">svthang@sentinel</span><span class="t-path">:~$</span> <span class="t-cmd">cat mission.txt</span></div>
        <div style="color:var(--text); font-size:13px; margin-top:0.4rem; max-width:640px; line-height:1.85;">
          Bridging psychology and cybersecurity to build systems that are technically secure and humanly resilient.
          Specializing in IoT defense, threat detection, anomaly detection, and social engineering — with a unique
          lens shaped by behavioral science and multilingual communication.
        </div>
        <div class="cta-row">
          <a href="#projects" class="btn btn-primary">view projects</a>
          <a href="#contact" class="btn btn-ghost">get in touch</a>
          <a href="https://www.linkedin.com/in/stephen-thang-743338264/" target="_blank" class="btn btn-ghost">linkedin ↗</a>
          <a href="https://tinyurl.com/yhnntrja" target="_blank" class="btn btn-ghost">github ↗</a>
        </div>
        <div style="margin-top:1.75rem; color:var(--text-dim); font-size:12px;"><span class="cursor"></span></div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="container">
    <div class="sec-label">// 01</div>
    <div class="sec-title">about me</div>
    <div class="about-grid">
      <div class="about-text">
        <p>
          I'm a graduating senior at the <strong>University of Maryland, College Park</strong> completing dual B.S. degrees
          in Psychology and Information Science (Cybersecurity concentration), a plus-one M.S. in Information Systems,
          and triple minors in Asian American Studies, Information Risk Management, and Human Development.
          Major GPA: <span class="gpa">3.75</span>.
        </p>
        <p>
          My background is <strong>genuinely interdisciplinary</strong> — I approach security problems through both a
          technical and behavioral lens. That means I can think about threats the way attackers do, but also understand
          <em>why humans make decisions</em> that create vulnerabilities in the first place.
        </p>
        <p>
          I've competed <strong>twice in the DoD Cyber Sentinel Skills Challenge</strong>, interned at the
          <strong>U.S. Army Research Laboratory</strong>, and built an end-to-end IoT security pipeline for a real
          client externship. I'm actively targeting full-time roles in cybersecurity, data analytics, and information systems.
        </p>
        <div class="lang-row">
          <h4>languages spoken</h4>
          <span class="lang-tag">English</span>
          <span class="lang-tag">Burmese</span>
          <span class="lang-tag">Matu</span>
          <span class="lang-tag">Spanish (elem.)</span>
        </div>
      </div>
      <div>
        <div class="stat-grid">
          <div class="stat-card"><div class="stat-num">3.75</div><div class="stat-lbl">major GPA</div></div>
          <div class="stat-card"><div class="stat-num">2×</div><div class="stat-lbl">DoD Cyber Sentinel</div></div>
          <div class="stat-card"><div class="stat-num">5+</div><div class="stat-lbl">degrees & minors</div></div>
          <div class="stat-card"><div class="stat-num">CEH</div><div class="stat-lbl">ethical hacker cert</div></div>
          <div class="stat-card" style="grid-column: span 2;"><div class="stat-num">0.757</div><div class="stat-lbl">F1 score — anomaly detection (Hydroficient)</div></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="container">
    <div class="sec-label">// 02</div>
    <div class="sec-title">skills & tools</div>
    <div class="skills-grid">
      <div class="skill-cat">
        <h4>offensive security</h4>
        <span class="skill-tag">CEH</span>
        <span class="skill-tag">Metasploit</span>
        <span class="skill-tag">Burp Suite</span>
        <span class="skill-tag">Aircrack-ng</span>
        <span class="skill-tag">Nmap / Zenmap</span>
        <span class="skill-tag">OSINT</span>
        <span class="skill-tag">Social Engineering</span>
        <span class="skill-tag">Phishing Analysis</span>
      </div>
      <div class="skill-cat">
        <h4>blue team & SOC</h4>
        <span class="skill-tag">Splunk</span>
        <span class="skill-tag">SIEM</span>
        <span class="skill-tag">HIDS</span>
        <span class="skill-tag">MITRE ATT&CK</span>
        <span class="skill-tag">Incident Response</span>
        <span class="skill-tag">Wireshark</span>
        <span class="skill-tag">Vulnerability Scanning</span>
      </div>
      <div class="skill-cat">
        <h4>networking & IoT</h4>
        <span class="skill-tag">MQTT</span>
        <span class="skill-tag">TLS / mTLS</span>
        <span class="skill-tag">HMAC</span>
        <span class="skill-tag">Cisco Packet Tracer</span>
        <span class="skill-tag">Kali Linux</span>
        <span class="skill-tag">MitM Defense</span>
        <span class="skill-tag">Replay Attack Defense</span>
      </div>
      <div class="skill-cat">
        <h4>development</h4>
        <span class="skill-tag">Python</span>
        <span class="skill-tag">JavaScript</span>
        <span class="skill-tag">React</span>
        <span class="skill-tag">HTML / CSS</span>
        <span class="skill-tag">Java</span>
        <span class="skill-tag">SQL</span>
        <span class="skill-tag">PowerShell</span>
        <span class="skill-tag">R</span>
        <span class="skill-tag">Bash</span>
      </div>
      <div class="skill-cat">
        <h4>data & ML</h4>
        <span class="skill-tag">Isolation Forest</span>
        <span class="skill-tag">Anomaly Detection</span>
        <span class="skill-tag">Feature Engineering</span>
        <span class="skill-tag">Tableau</span>
        <span class="skill-tag">Excel</span>
        <span class="skill-tag">EDA</span>
        <span class="skill-tag">Visualization</span>
      </div>
      <div class="skill-cat">
        <h4>design & ops</h4>
        <span class="skill-tag">Figma</span>
        <span class="skill-tag">Cognitive Load Design</span>
        <span class="skill-tag">UX Research</span>
        <span class="skill-tag">I/O Psychology</span>
        <span class="skill-tag">Human-Centered Design</span>
      </div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="container">
    <div class="sec-label">// 03</div>
    <div class="sec-title">experience</div>
    <div class="exp-list">

      <div class="exp-item">
        <div class="exp-date">June 2025 –<br>Aug 2025</div>
        <div>
          <div class="exp-role">Data Analytics Intern</div>
          <div class="exp-org">CATT Lab · U.S. Army DEVCOM Army Research Laboratory · College Park, MD</div>
          <div class="exp-desc">
            <ul>
              <li>Collaborated with cross-functional research and engineering teams to analyze operational data and identify decision-making bottlenecks in real-time systems</li>
              <li>Applied exploratory data analysis and visualization techniques to translate complex traffic and incident data into actionable insights for high-stakes environments</li>
              <li>Designed and implemented data-driven interface solutions informed by cognitive load research, improving situational awareness and optimizing user interaction with live data</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="exp-item">
        <div class="exp-date">April 2026</div>
        <div>
          <div class="exp-role">IoT Cyber Defense Extern</div>
          <div class="exp-org">Hydroficient · Remote</div>
          <div class="exp-desc">
            <ul>
              <li>Engineered MQTT/TLS communication security for an IoT water monitoring system, implementing mTLS, HMAC message signing, and sequence counters to defend against replay and MitM attacks</li>
              <li>Developed an anomaly detection pipeline using Isolation Forest achieving an F1 score of 0.757, delivering findings via a custom-branded HTML security dashboard and formal technical report</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="exp-item">
        <div class="exp-date">Jan 2025 –<br>Present</div>
        <div>
          <div class="exp-role">Restaurant Server</div>
          <div class="exp-org">Iron Age Korean Barbeque Steakhouse · Baltimore, MD</div>
          <div class="exp-desc">
            <ul>
              <li>Delivered exceptional customer service across 5+ simultaneous tables in a high-paced dining environment</li>
              <li>Fostered a welcoming atmosphere through active listening and personalized guest interactions</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="exp-item">
        <div class="exp-date">Sept 2022 –<br>Sept 2024</div>
        <div>
          <div class="exp-role">Restaurant Manager</div>
          <div class="exp-org">KPot Korean BBQ & Hotpot · Catonsville, MD</div>
          <div class="exp-desc">
            <ul>
              <li>Oversaw daily financial closeout operations including revenue reconciliation and end-of-day procedures while supervising a team of servers</li>
              <li>Spearheaded customer service initiatives that independently raised the restaurant's Google rating from 4.4 to 4.8, earning recognition from management</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="exp-item">
        <div class="exp-date">Sept 2025</div>
        <div>
          <div class="exp-role">Youth Ambassador Cohort Finalist</div>
          <div class="exp-org">Asian Americans Advancing Justice</div>
          <div class="exp-desc">Represented Asian Americans at a sponsored convention on AI's social impacts, contributing policy-driven insights and demonstrating leadership through advocacy and collaboration with peers and professionals.</div>
        </div>
      </div>

      <div class="exp-item">
        <div class="exp-date">Sept 2023</div>
        <div>
          <div class="exp-role">Outreach Chair</div>
          <div class="exp-org">Myanmar Cultural Association · UMD</div>
          <div class="exp-desc">Initiated collaborations with student organizations, promoted awareness of Myanmar's culture and current events, and demonstrated leadership through event coordination, cross-cultural engagement, and community advocacy.</div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="container">
    <div class="sec-label">// 04</div>
    <div class="sec-title">featured projects</div>
    <div class="projects-grid">

      <div class="project-card">
        <div class="proj-header">
          <span class="proj-icon">🛡️</span>
          <div class="proj-links"><a href="https://tinyurl.com/yhnntrja" target="_blank">github ↗</a></div>
        </div>
        <h3>Hydroficient / Thang Sentinel</h3>
        <p>End-to-end IoT cyber defense system for a smart water monitoring pipeline. Implemented MQTT/TLS, mTLS, HMAC signing, and sequence counters. Built Isolation Forest anomaly detection (F1: 0.757) with a custom HTML security dashboard.</p>
        <div class="proj-tags">
          <span class="proj-tag">Python</span><span class="proj-tag">MQTT</span><span class="proj-tag">mTLS</span>
          <span class="proj-tag">Isolation Forest</span><span class="proj-tag">Kali Linux</span><span class="proj-tag">ML</span>
        </div>
      </div>

      <div class="project-card">
        <div class="proj-header">
          <span class="proj-icon">🏋️</span>
          <div class="proj-links"><a href="https://tinyurl.com/yhnntrja" target="_blank">github ↗</a></div>
        </div>
        <h3>AI Fitness Tracker</h3>
        <p>AI-driven fitness tracker in Python applying data cleaning, feature engineering, and EDA to identify trends in workout behavior and progression. Trained and evaluated ML models to generate personalized performance recommendations.</p>
        <div class="proj-tags">
          <span class="proj-tag">Python</span><span class="proj-tag">Machine Learning</span>
          <span class="proj-tag">Data Analysis</span><span class="proj-tag">Feature Engineering</span>
        </div>
      </div>

      <div class="project-card">
        <div class="proj-header">
          <span class="proj-icon">🔵</span>
          <div class="proj-links"><a href="https://tinyurl.com/yhnntrja" target="_blank">github ↗</a></div>
        </div>
        <h3>Blue Team SOC Lab</h3>
        <p>Applied Blue Team defense strategies in a SOC environment using SIEMs, HIDS, and vulnerability scanning tools. Leveraged MITRE ATT&CK and threat intelligence frameworks to analyze adversary behavior and lead incident response operations.</p>
        <div class="proj-tags">
          <span class="proj-tag">Splunk</span><span class="proj-tag">SIEM</span><span class="proj-tag">MITRE ATT&CK</span>
          <span class="proj-tag">HIDS</span><span class="proj-tag">Incident Response</span>
        </div>
      </div>

      <div class="project-card">
        <div class="proj-header">
          <span class="proj-icon">📋</span>
          <div class="proj-links"><a href="https://tinyurl.com/yhnntrja" target="_blank">report ↗</a></div>
        </div>
        <h3>Port of Baltimore Ransomware Policy Memo</h3>
        <p>Policy analysis and incident response recommendations for a critical infrastructure ransomware scenario, integrating NIST frameworks and real-world threat intelligence for a government-facing audience.</p>
        <div class="proj-tags">
          <span class="proj-tag">Policy</span><span class="proj-tag">NIST</span>
          <span class="proj-tag">Ransomware</span><span class="proj-tag">Critical Infrastructure</span>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- CERTS -->
<section id="certs">
  <div class="container">
    <div class="sec-label">// 05</div>
    <div class="sec-title">certifications</div>
    <div class="certs-grid">
      <div class="cert-card">
        <div class="cert-icon">🏅</div>
        <div>
          <div class="cert-name">Certified Ethical Hacker (CEH)</div>
          <div class="cert-issuer">EC-Council</div>
          <div class="cert-date">June 2025</div>
        </div>
      </div>
      <div class="cert-card">
        <div class="cert-icon">🔐</div>
        <div>
          <div class="cert-name">Intermediate Cybersecurity</div>
          <div class="cert-issuer">CodePath</div>
          <div class="cert-date">December 2025</div>
        </div>
      </div>
      <div class="cert-card">
        <div class="cert-icon">🔍</div>
        <div>
          <div class="cert-name">Cybersecurity & Data Analytics</div>
          <div class="cert-issuer">Google</div>
          <div class="cert-date">September 2023 – Present</div>
        </div>
      </div>
      <div class="cert-card">
        <div class="cert-icon">⚔️</div>
        <div>
          <div class="cert-name">DoD Cyber Sentinel Skills Challenge</div>
          <div class="cert-issuer">Department of Defense</div>
          <div class="cert-date">Competed 2022 & 2023</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="container">
    <div class="sec-label">// 06</div>
    <div class="sec-title">contact</div>
    <div class="contact-grid">
      <div>
        <p class="contact-note">
          Open to <strong>full-time roles</strong> in cybersecurity, data analytics, and information systems.
          Based in the <strong>DMV area</strong>. U.S. Citizen with DoD research experience.
          Actively exploring <strong>SFS-funded graduate programs</strong> at UMBC, JHU, and CMU.
        </p>
        <div class="contact-links">
          <a class="contact-link" href="mailto:svthang@terpmail.umd.edu">
            <span class="ci">@</span>
            <div><div class="cl">email</div><div class="cv">svthang@terpmail.umd.edu</div></div>
          </a>
          <a class="contact-link" href="tel:4102068476">
            <span class="ci">#</span>
            <div><div class="cl">phone</div><div class="cv">Private</div></div>
          </a>
          <a class="contact-link" href="https://www.linkedin.com/in/stephen-thang-743338264" target="_blank">
            <span class="ci">in</span>
            <div><div class="cl">linkedin</div><div class="cv">/in/stephen-thang-743338264</div></div>
          </a>
          <a class="contact-link" href="https://tinyurl.com/yhnntrja" target="_blank">
            <span class="ci">&lt;/&gt;</span>
            <div><div class="cl">github</div><div class="cv">https://github.com/StephenThang</div></div>
          </a>
        </div>
      </div>
      <div class="contact-form">
        <div class="form-label">// send a message</div>
        <input type="text" placeholder="your name" class="form-input" />
        <input type="email" placeholder="your email" class="form-input" />
        <textarea placeholder="your message..." class="form-input form-textarea"></textarea>
        <button class="form-btn" onclick="alert('Thanks for reaching out! I\'ll get back to you soon.')">send_message()</button>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="container">
    <p>Stephen Vanlian Thang · svthang@terpmail.umd.edu · University of Maryland '26</p>
    <p style="margin-top:6px; color:#30363d;">// built with html · css · js · deployed on github pages</p>
  </div>
</footer>

</body>
</html>
