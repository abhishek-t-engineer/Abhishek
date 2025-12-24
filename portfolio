<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>Electronics Engineer Portfolio — Embedded Systems & Power Electronics</title>
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <meta name="description" content="Electronics Engineer portfolio — embedded systems, STM32, IoT, motor control, PCB design." />
  <style>
    /* ===== variables (keep these first so avatar uses them) ===== */
    :root{
      /* Default = DARK THEME (high contrast, readable) */
      --bg: radial-gradient(circle at 10% 0%, #020617 0, #020617 55%, #000000 100%);
      --card: #020617;
      --card-soft: #020617;

      /* EV blue accents */
      --accent: #38bdf8;
      --accent-2: #0ea5e9;
      --accent-soft: rgba(56,189,248,0.16);

      /* Text colors */
      --text: #e5e7eb;
      --muted:#9ca3af;

      /* Borders & radii */
      --border:#1f2937; 
      --radius-lg:18px;
      --radius-xl:26px;

      /* Shadow, focus, glass */
      --shadow-soft:0 18px 40px rgba(15,23,42,0.80);
      --focus: 0 0 0 3px rgba(56,189,248,0.40);
      --glass: rgba(15,23,42,0.75);
      --glass-strong: rgba(15,23,42,0.90);

      /* Chips / tags */
      --chip-bg: rgba(15,23,42,0.9);
      --chip-border:#334155;
    }

    /* Light theme overrides - HIGHLY READABLE */
    :root[data-theme="light"]{
      /* Soft light background */
      --bg: radial-gradient(circle at 0% 0%, #e0f2fe 0, #f9fafb 45%, #e5e7eb 100%);

      /* Cards */
      --card: #ffffff;
      --card-soft: #f9fafb;

      /* Accents */
      --accent: #2563eb;
      --accent-2: #0ea5e9;
      --accent-soft: rgba(37,99,235,0.14);

      /* Text colors */
      --text: #0f172a;
      --muted: #475569;

      /* Borders & shadows */
      --border: #e2e8f0;
      --shadow-soft: 0 18px 40px rgba(15,23,42,0.08);

      /* Glass effects */
      --glass: rgba(255,255,255,0.70);
      --glass-strong: rgba(255,255,255,0.96);

      /* Chips / tags on light theme */
      --chip-bg: #e5edff;
      --chip-border: #c7d2fe;

      /* Focus outline */
      --focus: 0 0 0 3px rgba(37,99,235,0.35);

      --radius-lg:18px;
      --radius-xl:26px;
    }

    /* apply background via variable so theme switch is visible */
    *,*::before,*::after{box-sizing:border-box}
    html,body{height:100%}

    body {
      margin:0;
      font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      background: var(--bg);
      color: var(--text);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.5;
      min-height:100%;
    }

    a{color:var(--accent); text-decoration:none}
    a:focus{outline: none; box-shadow: 0 0 0 4px rgba(56,189,248,0.12); border-radius:6px}
    img{max-width:100%; height:auto; display:block}

    .page{
      max-width:1100px;
      margin:0 auto;
      padding:24px 16px 56px;
    }

    /* ===== Avatar / circular photo with ring ===== */
    .avatar-outer {
      --size: 175px;
      width: var(--size);
      height: var(--size);
      border-radius: 99px;
      padding: 4px;
      display: inline-block;
      background: linear-gradient(135deg, var(--accent), var(--accent-2));
      box-shadow: 0 10px 30px rgba(2,6,23,0.6), 0 2px 8px rgba(0,0,0,0.45);
      transition: transform .18s ease, box-shadow .18s ease;
    }

    .avatar-inner {
      width: 100%;
      height: 100%;
      border-radius: 999px;
      padding: 3px;
      background: var(--card);
      display: block;
      box-sizing: border-box;
    }

    .avatar-inner img{
      width: 100%;
      height: 100%;
      object-fit: cover;
      border-radius: 999px;
      display: block;
      border: 2px solid rgba(255,255,255,0.02);
    }

    .avatar-outer:hover,
    .avatar-outer:focus-within {
      transform: translateY(-6px);
      box-shadow: 0 18px 40px rgba(2,6,23,0.7), 0 6px 18px rgba(0,0,0,0.6);
    }

    @media (max-width: 540px){
      .avatar-outer { --size: 92px; padding:5px; }
    }

    /* Skip link */
    .skip-link {
      position: absolute;
      left: -999px;
      top: auto;
      width: 1px;
      height: 1px;
      overflow: hidden;
    }
    .skip-link:focus {
      left: 16px;
      top: 16px;
      width: auto;
      height: auto;
      padding: 8px 12px;
      border-radius: 8px;
      background: var(--card);
      color: var(--text);
      z-index: 9999;
      box-shadow: 0 6px 20px rgba(2,6,23,0.6);
    }

    /* Header & Nav */
    header{
      position: sticky;
      top:0;
      z-index:30;
      backdrop-filter: blur(12px);
      background: linear-gradient(to bottom, rgba(2,6,23,0.92), rgba(2,6,23,0.24));
      border-bottom: 1px solid rgba(15,23,42,0.85);
    }

    /* Light theme header override */
    [data-theme="light"] header{
      background: linear-gradient(to bottom, rgba(255,255,255,0.96), rgba(248,250,252,0.94));
      border-bottom: 1px solid var(--border);
    }

    .nav{
      max-width:1100px;
      margin:0 auto;
      padding:10px 16px;
      display:flex;
      gap:12px;
      align-items:center;
      justify-content:space-between;
    }
    .brand{
      display:flex;
      gap:12px;
      align-items:center;
    }
    .logo {
      width:42px; height:42px;
      display:inline-grid;
      place-items:center;
      border-radius:10px;
      background:linear-gradient(135deg,var(--accent),var(--accent-2));
      color:#071023;
      font-weight:700;
      box-shadow: 0 8px 22px rgba(56,189,248,0.12);
    }
    .nav-title{
      font-weight:700;
      letter-spacing:0.04em;
      font-size:0.9rem;
      color:var(--muted);
    }
    .nav-links{
      display:flex;
      gap:8px;
      align-items:center;
    }
    .nav-links a{
      padding:8px 12px;
      border-radius:999px;
      background:var(--glass);
      color:var(--muted);
      border:1px solid rgba(55,65,81,0.9);
      font-size:0.79rem;
    }
    .nav-links a[aria-current="page"]{
      color:var(--accent);
      border-color: rgba(56,189,248,0.22);
      background:var(--accent-soft);
    }
    .nav-actions{
      display:flex;
      gap:8px;
      align-items:center;
    }
    .icon-btn{
      display:inline-grid;
      place-items:center;
      width:40px;height:40px;
      border-radius:10px;
      background:var(--glass);
      border:1px solid rgba(55,65,81,0.9);
      color:var(--muted);
      cursor:pointer;
    }
    .icon-btn:focus{box-shadow: var(--focus); outline: none}

    /* Mobile nav toggle */
    .mobile-toggle{display:none}
    @media (max-width:880px){
      .nav-links{display:none}
      .mobile-toggle{display:inline-grid}
    }

    /* ====== HERO ====== */
    .hero{
      display:grid;
      grid-template-columns:minmax(0,2fr) minmax(0,1.6fr);
      gap:24px;
      margin-top:28px;
      margin-bottom:24px;
      align-items:center;
    }

    .card{
      background: var(--card);
      border-radius:var(--radius-xl);
      border:1px solid var(--border);
      padding:20px;
      box-shadow:var(--shadow-soft);
    }

    .hero-left{ padding:20px; border-radius:var(--radius-xl); }
    .pill{
      display:inline-flex; align-items:center; gap:10px;
      padding:6px 12px; border-radius:999px; background:var(--accent-soft);
      border:1px solid rgba(56,189,248,0.30); color:var(--accent);
      font-size:0.78rem; letter-spacing:0.08em; text-transform:uppercase;
      margin-bottom:12px;
    }
    .pill-dot{ width:8px; height:8px; border-radius:99px; background:var(--accent); box-shadow:0 0 9px rgba(56,189,248,0.85);}

    .hero-title{ font-size: clamp(1.9rem, 4vw, 2.4rem); font-weight:700; margin-bottom:8px }
    .hero-subtitle{ color:var(--muted); font-size:0.94rem; max-width:640px; margin-bottom:16px }

    .hero-tags{ display:flex; flex-wrap:wrap; gap:8px; margin-bottom:14px }
    .tag{
      font-size:0.78rem;
      padding:6px 10px;
      border-radius:999px;
      color:var(--muted);
      background:var(--chip-bg);
      border:1px solid var(--chip-border);
    }

    .hero-actions{ display:flex; gap:10px; flex-wrap:wrap }
    .btn{
      display:inline-flex; align-items:center; gap:8px; padding:10px 16px; border-radius:999px;
      font-weight:600; cursor:pointer; text-decoration:none; border:1px solid transparent;
    }
    .btn-primary{
      background: linear-gradient(135deg,var(--accent),var(--accent-2));
      color: #071023; box-shadow: 0 12px 30px rgba(56,189,248,0.25); border-color: rgba(56,189,248,0.18);
    }
    .btn-primary:hover{ transform: translateY(-2px) }
    .btn-ghost{ background: var(--glass-strong); color:var(--muted); border:1px solid rgba(55,65,81,0.9) }
    .btn-ghost:hover{ color:var(--accent); border-color: rgba(56,189,248,0.22) }

    .hero-right{ padding:18px; display:flex; flex-direction:column; gap:12px; border-radius:var(--radius-xl) }

    .badges{ display:flex; gap:8px; flex-wrap:wrap; margin-top:6px }
    .badge-soft{
      padding:6px 10px;
      border-radius:999px;
      background:var(--chip-bg);
      border:1px dashed var(--chip-border);
      color:var(--muted);
      font-size:0.82rem;
    }

    /* Sections */
    section{ margin-top:28px }
    .section-title{ font-size:1.05rem; font-weight:600; display:inline-flex; gap:8px; align-items:center; margin-bottom:6px }
    .section-title span{ width:7px; height:20px; border-radius:999px; background: linear-gradient(to bottom,var(--accent),transparent) }
    .section-subtitle{ font-size:0.86rem; color:var(--muted); margin-bottom:12px }

    /* Skills */
    .skills-grid{ display:grid; grid-template-columns:repeat(auto-fit,minmax(200px,1fr)); gap:12px; font-size:0.9rem }
    .skills-grid ul{ list-style:none; padding-left:0 }
    .skills-grid li{ margin-bottom:8px; color:var(--muted) }
    .skills-grid li::before{ content:"▹"; color:var(--accent); margin-right:8px }

    /* Projects */
    .projects-grid{ display:grid; grid-template-columns:repeat(auto-fit,minmax(260px,1fr)); gap:14px }
    .project-card{
      padding:14px;
      border-radius:var(--radius-lg);
      background:var(--card-soft);
      border:1px solid var(--border);
      box-shadow: var(--shadow-soft);
    }
    .project-meta{ font-size:0.71rem; color:var(--muted); text-transform:uppercase; letter-spacing:0.12em; margin-bottom:6px }
    .project-title{ font-weight:600; margin-bottom:6px; font-size:0.96rem }
    .project-card li{ margin-bottom:6px; color:var(--muted); font-size:0.88rem }

    /* Tools & Achievements */
    .two-col{ display:grid; grid-template-columns:minmax(0,1.3fr) minmax(0,1fr); gap:14px }
    .pill-list{ display:flex; gap:8px; flex-wrap:wrap }
    .pill-list span{
      padding:6px 10px;
      border-radius:999px;
      background:var(--chip-bg);
      border:1px solid var(--chip-border);
      color:var(--muted);
      font-size:0.86rem;
    }

    /* Contact */
    .contact-grid{ display:grid; grid-template-columns:minmax(0,1.1fr) minmax(0,1.1fr); gap:14px; align-items:flex-start }
    .contact-list{ list-style:none; padding-left:0; color:var(--muted); font-size:0.9rem }
    .contact-label{ font-size:0.78rem; text-transform:uppercase; color:var(--muted); letter-spacing:0.12em; display:block }
    .contact-value{ color:var(--text); font-size:0.92rem }

    footer{ margin-top:32px; font-size:0.78rem; color:var(--muted); text-align:center; padding-top:12px; border-top:1px solid rgba(15,23,42,0.9) }

    /* Focus / accessibility */
    a:focus, button:focus, input:focus{ outline: none; box-shadow: var(--focus); border-radius:8px }
    :focus{ scroll-margin-top: 80px }

    /* Responsive */
    @media (max-width:840px){
      .hero{ grid-template-columns: 1fr }
      .hero-right{ order:-1 }
      .two-col, .contact-grid{ grid-template-columns: 1fr }
    }

    /* Print */
    @media print{
      body{ background: #fff; color:#111; }
      header, .hero-actions, .nav-actions, .icon-btn{ display:none }
      .page{ padding:0; max-width:100% }
      .card{ box-shadow:none; border:1px solid #ddd; background:#fff }
    }

    /* Reduced motion */
    @media (prefers-reduced-motion: reduce){
      *{ transition:none !important; animation:none !important; }
    }
  </style>
</head>
<body>
  <a class="skip-link" href="#main">Skip to content</a>

  <header role="banner" aria-label="Main header">
    <nav class="nav" role="navigation" aria-label="Primary navigation">
      <div class="brand">
        <div class="logo" aria-hidden="true">ECE</div>
        <div>
          <div class="nav-title">R & D Engineer</div>
        </div>
      </div>

      <div class="nav-links" role="menubar" aria-label="Main links">
        <a href="#about" role="menuitem">About</a>
        <a href="#skills" role="menuitem">Skills</a>
        <a href="#projects" role="menuitem">Projects</a>
        <a href="#tools" role="menuitem">Tools</a>
        <a href="#contact" role="menuitem">Contact</a>
      </div>

      <div class="nav-actions" aria-hidden="false">
        <!-- Download Resume -->
        <a class="btn btn-ghost" href="Abhishek CV.pdf" download aria-label="Download resume">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" style="vertical-align:middle" xmlns="http://www.w3.org/2000/svg">
            <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z" stroke="currentColor" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M14 2v6h6" stroke="currentColor" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
          <span style="font-size:0.86rem">Resume</span>
        </a>

        <!-- Theme toggle -->
        <button class="icon-btn" id="themeToggle" aria-label="Toggle theme" title="Toggle theme">
          <svg id="themeIcon" width="18" height="18" viewBox="0 0 24 24" fill="none" aria-hidden="true">
            <path d="M12 3v2M12 19v2M4.2 4.2l1.4 1.4M18.4 18.4l1.4 1.4M1 12h2M21 12h2M4.2 19.8l1.4-1.4M18.4 5.6l1.4-1.4" stroke="currentColor" stroke-width="1.4" stroke-linecap="round" stroke-linejoin="round"/>
            <circle cx="12" cy="12" r="3" stroke="currentColor" stroke-width="1.4" />
          </svg>
        </button>

        <!-- Mobile toggle -->
        <button class="icon-btn mobile-toggle" id="navToggle" aria-label="Open menu" aria-expanded="false" aria-controls="mobileMenu">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="none" aria-hidden="true">
            <path d="M4 6h16M4 12h16M4 18h16" stroke="currentColor" stroke-width="1.6" stroke-linecap="round"/>
          </svg>
        </button>
      </div>
    </nav>

    <!-- Mobile menu (hidden on desktop) -->
    <div id="mobileMenu" style="display:none; padding:12px 16px; border-top:1px solid var(--border); background:var(--card);">
      <div style="display:flex; flex-direction:column; gap:8px; max-width:1100px; margin:0 auto;">
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a href="#tools">Tools</a>
        <a href="#contact">Contact</a>
      </div>
    </div>
  </header>

  <main id="main" class="page" role="main" aria-labelledby="aboutHeading">
    <!-- HERO / ABOUT -->
    <section class="hero" id="about" aria-labelledby="aboutHeading">
      <div class="hero-left card">
        <figure style="margin:0 0 12px 0; display:flex; align-items:center; gap:12px;">
          <a href="abhi.jpeg" target="_blank" rel="noopener" aria-label="Open full-size photo">
            <span class="avatar-outer" tabindex="0">
              <span class="avatar-inner"> 
                <img src="abhi.jpeg" alt="ABHISHEK T — Electronics Engineer" loading="lazy" width="5800" height="5800">
              </span>
            </span>
          </a>
          <figcaption style="font-size:1.70rem; color:var(--text);">
            <strong style="display:block;">ABHISHEK T</strong>
            <span style="color:var(--muted); font-size:1.40rem;">Electronics Engineer</span>
          </figcaption>
        </figure>

        <div>
          <h3 style="font-size:0.95rem; margin:0 0 6px 0;">Profile</h3>
          <p style="margin:0; color:var(--muted); font-size:0.9rem;">
            Electronics & Communication Engineer with expertise in circuit design, embedded systems, and motor control. 
            Skilled in Arduino development and analog circuit design and layout.
          </p>
        </div>

        <div>
          <h3 style="font-size:0.95rem; margin:12px 0 6px 0;">What I Work On</h3>
          <div class="badges" aria-hidden="true">
            <span class="badge-soft">Arduino / ESP32</span>
            <span class="badge-soft">BLDC & DC Motor Control</span>
            <span class="badge-soft">Electronics board testing</span>
            <span class="badge-soft">Research & Development in electrical vehicles</span>
          </div>
        </div>

        <div>
          <h3 style="font-size:0.95rem; margin:12px 0 6px 0;">Career Goals</h3>
          <p style="margin:0; color:var(--muted); font-size:0.9rem;">
            I am pursuing a professional trajectory as an Electronics Engineer with a dedicated focus on advanced electronics development and research within the Electric Vehicle domain. My expertise encompasses embedded systems, power electronics, and next-generation EV technologies. I aspire to contribute to the creation of intelligent, reliable, and highly efficient electric mobility solutions that elevate both performance and sustainability.
          </p>
        </div>
      </div>

      <aside class="hero-right card" aria-label="Profile summary">
        <h1 id="aboutHeading" class="hero-title">Research and Development Engineer in EV Technology</h1>
        <p class="hero-subtitle">
          I design and build electronic systems using microcontrollers, sensors, and power electronics.
          I enjoy turning ideas into working prototypes with simple, reliable, and efficient hardware and EV technologies.
        </p>

        <div class="hero-tags" aria-hidden="true">
          <span class="tag">Embedded Systems</span>
          <span class="tag">Microcontrollers</span>
          <span class="tag">Analog Circuit and Layout</span>
          <span class="tag">PCB Design</span>
          <span class="tag">Power Electronics</span>
        </div>

        <div class="hero-actions" role="group" aria-label="Primary actions">
          <a href="#projects" class="btn btn-primary">View Projects</a>
          <a href="#contact" class="btn btn-ghost">Get in Touch</a>
        </div>
      </aside>
    </section>

    <!-- SKILLS -->
    <section id="skills" aria-labelledby="skillsHeading">
      <h2 id="skillsHeading" class="section-title"><span aria-hidden="true"></span>Core Skills</h2>
      <p class="section-subtitle">Hands-on skills in electronics, embedded systems, and hardware design.</p>

      <div class="card">
        <div class="skills-grid" role="list">
          <ul role="list">
            <li>Embedded Systems (Arduino, ESP32)</li>
            <li>Real-time interfacing with sensors</li>
            <li>Communication protocols (UART, SPI, I2C, CAN)</li>
          </ul>
          <ul role="list">
            <li>Power electronics & motor control (BLDC, DC motors)</li>
            <li>Basic battery management concepts (BMS)</li>
          </ul>
          <ul role="list">
            <li>PCB design and layout for small boards</li>
            <li>Circuit simulation and testing</li>
            <li>Hardware design and soldering</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- PROJECTS -->
    <section id="projects" aria-labelledby="projectsHeading">
      <h2 id="projectsHeading" class="section-title"><span aria-hidden="true"></span>Selected Projects</h2>
      <p class="section-subtitle">A few projects that showcase my skills in embedded systems, IoT, and power electronics.</p>

      <div class="projects-grid" role="list">
        <article class="project-card" role="listitem" aria-labelledby="p1">
          <div class="project-meta">Embedded system</div>
          <h3 id="p1" class="project-title">Automatic Door Locking System using RFID Card and Keychain</h3>
          <ul>
            <li>Built using ESP32 with Wi-Fi connectivity for door locking control.</li>
            <li>Integrated sensors to control door access and allow only authorized individuals to enter.</li>
            <li>Real-time monitoring and control in an automatic locking system.</li>
          </ul>
        </article>

        <article class="project-card" role="listitem" aria-labelledby="p3">
          <div class="project-meta">Embedded system</div>
          <h3 id="p3" class="project-title">Agriculture Robot (Farm Bot BT) using a Bluetooth Controller</h3>
          <ul>
            <li>Used microcontroller to interface ultrasonic, IR, and fire sensors.</li>
            <li>Robot is controlled wirelessly using a Bluetooth mobile app or controller.</li>
            <li>Performs tasks like soil checking, seed dropping, spraying, or moving tools.</li>
            <li>Helps farmers operate from a distance, reducing manual work and saving time.</li>
          </ul>
        </article>

        <article class="project-card" role="listitem" aria-labelledby="p4">
          <div class="project-meta">Embedded system</div>
          <h3 id="p4" class="project-title">Smart Solar-Powered Robot with Integrated Environmental and Crop Monitoring</h3>
          <ul>
            <li>Runs on solar energy, reducing external power needs and improving sustainability.</li>
            <li>Built-in sensors measure temperature, humidity, and sunlight to monitor farm conditions.</li>
            <li>Collects data on crop growth and detects early issues to help improve yield.</li>
          </ul>
        </article>
      </div>
    </section>

    <!-- TOOLS & ACHIEVEMENTS -->
    <section id="tools" aria-labelledby="toolsHeading">
      <h2 id="toolsHeading" class="section-title"><span aria-hidden="true"></span>Tools, Software & Achievements</h2>
      <p class="section-subtitle">Software and platforms I work with, plus highlights from projects & learning.</p>

      <div class="two-col">
        <div class="card">
          <h3 style="font-size:0.95rem; margin-bottom:8px;">Tools & Software</h3>
          <div class="pill-list" aria-hidden="true">
            <span>Multisim</span>
            <span>LTspice</span>
            <span>Arduino IDE</span>
            <span>Keil uVision</span>
            <span>VS Code</span>
            <span>KiCad</span>
            <span>EasyEDA</span>
            <span>MATLAB / Simulink</span>
          </div>
        </div>
        </section>

        <section>
        <div class="card achievements">
          <h3 style="font-size:0.95rem; margin-bottom:8px;">Achievements & Certifications</h3>
          <ul>
            <li>Developed multiple IoT and embedded systems prototypes as part of academic projects.</li>
            <li>Participated in hardware design and testing activities focused on real-time embedded solutions.</li>
            <li>Completed online courses in embedded systems, analog circuit and layout design, and PCB design.</li>
            <li>Share electronics content and R&D updates related to electric vehicles on LinkedIn to help others learn.</li>
            <li>Completed “VLSI for Beginners” from the National Institute of Electronics and Information Technology (NIELIT), Calicut.</li>
            <li>Completed “Introduction to MATLAB & Simulink” from the National Institute of Electronics and Information Technology (NIELIT), Calicut.</li>
            <li>Completed “Embedded System for Beginners” from the National Institute of Electronics and Information Technology (NIELIT), Calicut.</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" aria-labelledby="contactHeading">
      <h2 id="contactHeading" class="section-title"><span aria-hidden="true"></span>Contact & Links</h2>
      <p class="section-subtitle">Feel free to reach out for collaboration, project ideas, or opportunities in embedded systems and electronics.</p>

      <div class="card contact-grid">
        <div>
          <ul class="contact-list" role="list">
            <li>
              <span class="contact-label">Email</span>
              <span class="contact-value"><a href="mailto:abhiabhi935311@gmail.com">abhiabhi935311@gmail.com</a></span>
            </li>
            <li>
              <span class="contact-label">Phone</span>
              <span class="contact-value"><a href="tel:+919353116837">+91-9353116837</a></span>
            </li>
            <li>
              <span class="contact-label">LinkedIn</span>
              <span class="contact-value">
                <a href="https://www.linkedin.com/in/abhishek-t-9353abhi1802/" target="_blank" rel="noopener">https://www.linkedin.com/in/abhishek-t-9353abhi1802/</a>
              </span>
            </li>
            <li>
              <span class="contact-label">GitHub</span>
              <span class="contact-value">
                <a href="https://github.com/abhishek-t-engineer" target="_blank" rel="noopener">https://github.com/abhishek-t-engineer</a>
              </span>
            </li>
          </ul>
        </div>

        <div>
          <p style="font-size:0.86rem; color:var(--muted); margin-bottom:8px;">I’m looking for roles in:</p>
          <div class="pill-list" aria-hidden="true">
            <span>Embedded Systems</span>
            <span>Hardware / PCB Designs</span>
            <span>Power Electronics</span>
          </div>
        </div>
      </div>
    </section>

    <!-- Optional footer (uncomment if you want it visible)
    <footer>
      © <span id="year"></span> Electronics Engineer Portfolio. Built with HTML &amp; CSS.
    </footer>
    -->
  </main>

  <script>
    // --- utilities: year, smooth scroll, nav toggle, theme toggle ---
    (function(){
      // year (safe check)
      const yearEl = document.getElementById('year');
      if (yearEl) {
        yearEl.textContent = new Date().getFullYear();
      }

      // smooth scroll for internal anchors
      document.querySelectorAll('a[href^="#"]').forEach(a=>{
        a.addEventListener('click', function(e){
          const href = this.getAttribute('href');
          if(!href || href === '#') return;
          const id = href.slice(1);
          const target = document.getElementById(id);
          if(target){
            e.preventDefault();
            target.scrollIntoView({behavior:'smooth', block:'start'});
            // update mobile menu state if open
            closeMobileMenu();
          }
        });
      });

      // mobile nav toggle
      const navToggle = document.getElementById('navToggle');
      const mobileMenu = document.getElementById('mobileMenu');
      function closeMobileMenu(){
        if(navToggle){
          navToggle.setAttribute('aria-expanded','false');
        }
        if(mobileMenu){
          mobileMenu.style.display = 'none';
        }
      }
      function openMobileMenu(){
        if(navToggle){
          navToggle.setAttribute('aria-expanded','true');
        }
        if(mobileMenu){
          mobileMenu.style.display = 'block';
        }
      }
      if(navToggle){
        navToggle.addEventListener('click', ()=>{
          const expanded = navToggle.getAttribute('aria-expanded') === 'true';
          if(expanded) closeMobileMenu(); else openMobileMenu();
        });
      }
      // close on resize to desktop
      window.addEventListener('resize', ()=>{
        if(window.innerWidth > 880) closeMobileMenu();
      });

      // Theme toggle (dark/light) with persistence
      const themeToggle = document.getElementById('themeToggle');
      const root = document.documentElement;
      const THEME_KEY = 'portfolio-theme';

      function applyTheme(theme){
        if(theme === 'light'){
          root.setAttribute('data-theme','light');
          // sun icon
          const icon = document.getElementById('themeIcon');
          if(icon) icon.innerHTML =
            '<path d="M12 2v2M12 20v2M4.2 4.2l1.4 1.4M18.4 18.4l1.4 1.4M1 12h2M21 12h2M4.2 19.8l1.4-1.4M18.4 5.6l1.4-1.4" stroke="currentColor" stroke-width="1.4" stroke-linecap="round" stroke-linejoin="round"/>' +
            '<circle cx="12" cy="12" r="3" stroke="currentColor" stroke-width="1.4"/>';
        } else {
          root.removeAttribute('data-theme');
          // moon icon
          const icon = document.getElementById('themeIcon');
          if(icon) icon.innerHTML =
            '<path d="M21 12.79A9 9 0 1111.21 3 7 7 0 0021 12.79z" stroke="currentColor" stroke-width="1.4" stroke-linecap="round" stroke-linejoin="round" fill="none"/>';
        }
      }

      // detect saved or prefer-dark
      const saved = localStorage.getItem(THEME_KEY);
      if(saved) {
        applyTheme(saved);
      } else {
        const prefersDark = window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches;
        applyTheme(prefersDark ? 'dark' : 'light');
      }

      if(themeToggle){
        themeToggle.addEventListener('click', ()=>{
          const cur = root.getAttribute('data-theme') === 'light' ? 'light' : 'dark';
          const next = cur === 'light' ? 'dark' : 'light';
          applyTheme(next);
          localStorage.setItem(THEME_KEY, next);
        });
      }

      // Accessibility: set focus visible for keyboard users only
      function handleFirstTab(e){
        if(e.key === 'Tab'){
          document.body.classList.add('user-is-tabbing');
          window.removeEventListener('keydown', handleFirstTab);
        }
      }
      window.addEventListener('keydown', handleFirstTab);
    })();
  </script>
</body>
</html>
