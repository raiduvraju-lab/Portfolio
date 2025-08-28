<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Raidu V Raju – Portfolio</title>
  <meta name="description" content="Portfolio of Raidu V Raju – B.Sc in Artificial Intelligence & Robotics. Python, HTML, CSS, Power BI. Projects, skills, certificates, and contact." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg: #0b0d10;
      --panel: #11151a;
      --panel-2: #141a21;
      --text: #e8f0ff;
      --muted: #a6b0c3;
      --brand: #7c3aed; /* violet-600 */
      --brand-2: #22d3ee; /* cyan-400 */
      --accent: #38bdf8; /* sky-400 */
      --ok: #22c55e;
      --warning: #f59e0b;
      --ring: 0 0 0 3px rgba(124,58,237,.25);
    }
    *{box-sizing: border-box}
    html{scroll-behavior: smooth}
    body{
      margin:0; font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, "Helvetica Neue", Arial, "Noto Sans", "Apple Color Emoji", "Segoe UI Emoji";
      background: radial-gradient(1200px 800px at 10% -10%, rgba(124,58,237,.15), transparent 60%),
                  radial-gradient(1200px 800px at 110% 10%, rgba(34,211,238,.12), transparent 60%),
                  var(--bg);
      color: var(--text);
    }
    .container{max-width:1100px; margin:0 auto; padding: 0 20px}
    header{
      position: sticky; top:0; z-index: 50; backdrop-filter: saturate(140%) blur(10px);
      background: linear-gradient(180deg, rgba(11,13,16,.85), rgba(11,13,16,.55));
      border-bottom: 1px solid rgba(255,255,255,.06);
    }
    nav{display:flex; align-items:center; justify-content:space-between; gap:16px; padding: 14px 0}
    .brand{display:flex; align-items:center; gap:12px; text-decoration:none; color:var(--text)}
    .logo{width:36px; height:36px; border-radius:12px; background: linear-gradient(135deg, var(--brand), var(--brand-2)); display:grid; place-items:center; font-weight:800}
    .logo span{filter: drop-shadow(0 2px 8px rgba(124,58,237,.6));}
    .navlinks{display:flex; gap: 18px; flex-wrap:wrap}
    .navlinks a{color:var(--muted); text-decoration:none; font-weight:600; padding:8px 12px; border-radius:12px}
    .navlinks a:hover{color:var(--text); background: rgba(124,58,237,.15)}
    .btn{display:inline-flex; align-items:center; gap:10px; text-decoration:none; color:white; background: linear-gradient(135deg, var(--brand), var(--accent));
      padding:10px 16px; border-radius:14px; font-weight:700; border: 1px solid rgba(255,255,255,.08); box-shadow: 0 10px 25px rgba(124,58,237,.25)}
    .ghost{background: transparent; border:1px solid rgba(255,255,255,.15); color: var(--text)}
    .row{display:grid; grid-template-columns: 1.2fr 1fr; gap:32px}
    .card{background: linear-gradient(180deg, rgba(255,255,255,.04), rgba(255,255,255,.02)); border:1px solid rgba(255,255,255,.08);
      border-radius: 20px; padding: 22px; box-shadow: 0 12px 40px rgba(0,0,0,.35)}
    .chip{display:inline-block; padding:8px 12px; border-radius:999px; background: rgba(124,58,237,.15); border:1px solid rgba(124,58,237,.35); color:#e9ddff; font-weight:700; margin:6px 6px 0 0}
    .kpi{display:grid; grid-template-columns: repeat(3, 1fr); gap:14px}
    .kpi .stat{padding:16px; border-radius:16px; background: linear-gradient(180deg, rgba(20,26,33,.9), rgba(17,21,26,.7)); border:1px solid rgba(255,255,255,.06); text-align:center}
    .hero{padding: 40px 0 28px}
    .hero h1{font-size: clamp(28px, 5vw, 52px); line-height:1.05; margin: 8px 0}
    .hero p{color: var(--muted); font-size: clamp(14px, 2.1vw, 18px)}
    section{padding: 28px 0}
    h2{font-size:clamp(20px, 2.6vw, 30px); margin:0 0 12px}
    .grid{display:grid; gap:16px}
    .grid.two{grid-template-columns: repeat(2, minmax(0,1fr))}
    .grid.three{grid-template-columns: repeat(3, minmax(0,1fr))}
    .project-card{position:relative; overflow:hidden}
    .project-card .badge{position:absolute; top:12px; right:12px; background: rgba(34,211,238,.15); color:#ccf7ff; border:1px solid rgba(34,211,238,.35); padding:6px 10px; border-radius:999px; font-size:12px; font-weight:700}
    .timeline{position:relative; padding-left:24px}
    .timeline::before{content:""; position:absolute; left:7px; top:0; bottom:0; width:2px; background: linear-gradient(var(--brand), transparent)}
    .tl-item{position:relative; margin:12px 0; padding-left:14px}
    .tl-item::before{content:""; position:absolute; left:-3px; top:10px; width:12px; height:12px; background: linear-gradient(135deg, var(--brand), var(--brand-2)); border-radius:999px; box-shadow: 0 0 0 4px rgba(124,58,237,.15)}
    footer{border-top: 1px solid rgba(255,255,255,.08); margin-top: 28px; padding: 28px 0 56px; color: var(--muted)}
    .contact a{color: var(--text)}
    .sr-only{position:absolute; width:1px; height:1px; padding:0; overflow:hidden; clip:rect(0,0,0,0); white-space:nowrap; border:0}
    .toggle{cursor:pointer; border:none; padding:10px 12px; border-radius:12px; color:var(--text); background: transparent; border:1px solid rgba(255,255,255,.15)}
    .toggle:focus{outline:none; box-shadow: var(--ring)}
    @media (max-width: 900px){
      .row{grid-template-columns: 1fr;}
      .grid.two{grid-template-columns: 1fr}
      .grid.three{grid-template-columns: 1fr}
    }
  </style>
  <script>
    // Dark mode is default; this lets users toggle a higher-contrast “ink” mode
    const THEME_KEY = 'rv-theme';
    function applyTheme(t){
      document.documentElement.dataset.theme = t;
      if(t==='ink'){
        document.documentElement.style.setProperty('--bg', '#09090b');
        document.documentElement.style.setProperty('--panel', '#0b0b0e');
        document.documentElement.style.setProperty('--panel-2', '#0d0d12');
        document.documentElement.style.setProperty('--text', '#fafafa');
        document.documentElement.style.setProperty('--muted', '#c9c9d1');
      } else {
        document.documentElement.style.removeProperty('--bg');
        document.documentElement.style.removeProperty('--panel');
        document.documentElement.style.removeProperty('--panel-2');
        document.documentElement.style.removeProperty('--text');
        document.documentElement.style.removeProperty('--muted');
      }
    }
    function initTheme(){
      const saved = localStorage.getItem(THEME_KEY);
      if(saved) applyTheme(saved);
    }
    function toggleTheme(){
      const now = document.documentElement.dataset.theme==='ink' ? 'dark' : 'ink';
      localStorage.setItem(THEME_KEY, now); applyTheme(now);
    }
    document.addEventListener('DOMContentLoaded', initTheme);
  </script>
  <script type="application/ld+json">
  {
    "@context":"https://schema.org",
    "@type":"Person",
    "name":"Raidu V Raju",
    "email":"mailto:raiduvraju@gmail.com",
    "telephone":"+91-9556588353",
    "sameAs":["https://www.linkedin.com/in/raiduvraju"],
    "jobTitle":"B.Sc Artificial Intelligence & Robotics (Student)",
    "knowsAbout":["Python","HTML","CSS","Power BI"],
    "address":{
      "@type":"PostalAddress",
      "addressLocality":"Bheden, Bargarh",
      "addressRegion":"Odisha",
      "postalCode":"768104",
      "streetAddress":"At: Ganthiapali, Po: Papanga"
    }
  }
  </script>
</head>
<body>
  <header>
    <div class="container">
      <nav>
        <a class="brand" href="#top" aria-label="Home">
          <div class="logo" aria-hidden="true"><span>RV</span></div>
          <div>
            <strong style="display:block; letter-spacing:.3px">Raidu V Raju</strong>
            <small style="color:var(--muted)">AI & Robotics Undergraduate</small>
          </div>
        </a>
        <div class="navlinks">
          <a href="#about">About</a>
          <a href="#skills">Skills</a>
          <a href="#education">Education</a>
          <a href="#projects">Projects</a>
          <a href="#certs">Certificates</a>
          <a href="#contact">Contact</a>
          <button class="toggle" onclick="toggleTheme()" title="Toggle theme">🌓</button>
        </div>
      </nav>
    </div>
  </header>

  <main id="top" class="container">
    <!-- HERO -->
    <section class="hero row">
      <div class="card">
        <span class="chip" title="Location">Bheden · Bargarh · Odisha</span>
        <h1>Building practical solutions with <span style="background: linear-gradient(135deg, var(--brand), var(--brand-2)); -webkit-background-clip:text; background-clip:text; color:transparent">Python & Data</span>.</h1>
        <p>
          Ambitious B.Sc student in Artificial Intelligence & Robotics—quick to adapt, collaborative, and detail‑oriented. Seeking opportunities to learn, build, and contribute to real‑world projects.
        </p>
        <div style="display:flex; gap:12px; flex-wrap:wrap; margin-top:18px">
          <a class="btn" href="https://www.linkedin.com/in/raiduvraju" target="_blank" rel="noopener">LinkedIn</a>
          <a class="btn ghost" href="Raidu-V-Raju-.pdf" download>Download Resume (PDF)</a>
          <a class="btn ghost" href="#contact">Hire Me</a>
        </div>
        <div class="kpi" style="margin-top:16px">
          <div class="stat"><div style="font-weight:900; font-size:22px">4</div><div style="color:var(--muted)">Languages</div></div>
          <div class="stat"><div style="font-weight:900; font-size:22px">5+</div><div style="color:var(--muted)">Certificates</div></div>
          <div class="stat"><div style="font-weight:900; font-size:22px">1</div><div style="color:var(--muted)">Featured Project</div></div>
        </div>
      </div>
      <aside class="card">
        <h2>At a glance</h2>
        <div class="grid">
          <div><strong>Email</strong><br><a href="mailto:raiduvraju@gmail.com">raiduvraju@gmail.com</a></div>
          <div><strong>Phone</strong><br><a href="tel:+919556588353">+91 95565 88353</a></div>
          <div><strong>Location</strong><br>At: Ganthiapali, Po: Papanga, Bheden, Bargarh, Odisha 768104</div>
          <div><strong>Open to</strong><br>Internships · Entry‑level roles · Freelance</div>
        </div>
        <div style="margin-top:14px">
          <span class="chip">Python</span>
          <span class="chip">HTML</span>
          <span class="chip">CSS</span>
          <span class="chip">Power BI</span>
        </div>
      </aside>
    </section>

    <!-- ABOUT -->
    <section id="about">
      <h2>Profile</h2>
      <div class="card">
        <p style="margin:0">As an ambitious student pursuing a B.Sc in Artificial Intelligence & Robotics, I aim to leverage adaptability, teamwork, and honesty to grow alongside forward‑thinking organizations. I enjoy building clean, reliable systems and learning out loud.</p>
      </div>
    </section>

    <!-- SKILLS -->
    <section id="skills">
      <h2>Skills</h2>
      <div class="grid two">
        <div class="card">
          <strong>Core</strong>
          <div style="margin-top:10px">
            <span class="chip">Python</span>
            <span class="chip">HTML</span>
            <span class="chip">CSS</span>
            <span class="chip">Power BI</span>
          </div>
        </div>
        <div class="card">
          <strong>Soft</strong>
          <div style="margin-top:10px">
            <span class="chip">Teamwork</span>
            <span class="chip">Problem Solving</span>
            <span class="chip">Adaptability</span>
            <span class="chip">Communication</span>
          </div>
        </div>
      </div>
    </section>

    <!-- EDUCATION -->
    <section id="education">
      <h2>Education</h2>
      <div class="card timeline">
        <div class="tl-item">
          <strong>B.Sc – Artificial Intelligence & Robotics</strong>
          <div style="color:var(--muted)">Aditya Degree College, Kakinada</div>
        </div>
        <div class="tl-item">
          <strong>Intermediate</strong>
          <div style="color:var(--muted)">Sri Sai Aditya Junior College, Kakinada</div>
        </div>
        <div class="tl-item">
          <strong>Matriculation</strong>
          <div style="color:var(--muted)">Dhatukpali High School, Dhatukpali</div>
        </div>
      </div>
    </section>

    <!-- PROJECTS -->
    <section id="projects">
      <h2>Projects</h2>
      <div class="grid">
        <article class="card project-card">
          <span class="badge">Python · HTML · CSS · JS</span>
          <h3 style="margin-top:4px">Super Market Bill Generation</h3>
          <p>
            Console‑based billing system to manage item catalog, compute totals, apply discounts and taxes, and generate invoices with robust error handling for invalid inputs.
          </p>
          <div style="display:flex; gap:10px; flex-wrap:wrap">
            <a class="btn ghost" href="#" onclick="alert('Demo not linked yet. Replace # with your repo or demo URL!'); return false;">View Demo</a>
            <a class="btn" href="#" onclick="alert('Repo not linked yet. Replace # with your GitHub URL!'); return false;">Source Code</a>
          </div>
        </article>
      </div>
    </section>

    <!-- CERTIFICATIONS -->
    <section id="certs">
      <h2>Certificates</h2>
      <div class="card">
        <div class="grid three">
          <div><span class="chip">Mepro</span></div>
          <div><span class="chip">Infosys – Basics of Python</span></div>
          <div><span class="chip">Cisco – Problem Solving (C, Python)</span></div>
          <div><span class="chip">edX – Business Writing Techniques</span></div>
        </div>
      </div>
    </section>

    <!-- LANGUAGES -->
    <section id="languages">
      <h2>Languages</h2>
      <div class="card">
        <span class="chip">English</span>
        <span class="chip">Hindi</span>
        <span class="chip">Telugu</span>
        <span class="chip">Oriya</span>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact">
      <h2>Contact</h2>
      <div class="card contact">
        <p style="margin-top:0">Have an opportunity, collaboration, or project? Let’s talk.</p>
        <div class="grid two">
          <div>
            <strong>Email</strong><br>
            <a href="mailto:raiduvraju@gmail.com">raiduvraju@gmail.com</a>
          </div>
          <div>
            <strong>Phone</strong><br>
            <a href="tel:+919556588353">+91 95565 88353</a>
          </div>
          <div>
            <strong>LinkedIn</strong><br>
            <a target="_blank" rel="noopener" href="https://www.linkedin.com/in/raiduvraju">linkedin.com/in/raiduvraju</a>
          </div>
          <div>
            <strong>Address</strong><br>
            At: Ganthiapali, Po: Papanga, Bheden, Bargarh, Odisha 768104
          </div>
        </div>
      </div>
    </section>

  </main>

  <footer>
    <div class="container" style="display:flex; align-items:center; justify-content:space-between; gap:12px; flex-wrap:wrap">
      <div>© <span id="y"></span> Raidu V Raju. All rights reserved.</div>
      <div style="display:flex; gap:10px">
        <a class="btn ghost" href="#top" aria-label="Back to top">↑ Top</a>
      </div>
    </div>
    <script>document.getElementById('y').textContent = new Date().getFullYear()</script>
  </footer>
</body>
</html>
