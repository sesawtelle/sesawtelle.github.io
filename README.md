<html lang="en">
<head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Sarah Sawtelle — Where Nature meets Narrative</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,600;1,9..144,300;1,9..144,600&family=DM+Sans:wght@300;400&display=swap" rel="stylesheet">
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body {
      background: #f0ebe0;
      color: #2a2318;
      font-family: 'DM Sans', sans-serif;
      font-weight: 300;
      overflow-x: hidden;
    }

    /* NAV */
    nav {
      position: sticky; top: 0; z-index: 100;
      display: flex; justify-content: space-between; align-items: center;
      padding: 1.4rem 2.5rem;
      border-bottom: 2px solid #2a2318;
      background: #f0ebe0;
    }
    .logo {
      font-family: 'Fraunces', serif; font-size: 1.1rem;
      font-weight: 300; font-style: italic;
      color: #2a2318; text-decoration: none;
    }
    .nav-links { display: flex; gap: 2rem; list-style: none; }
    .nav-links a {
      font-size: 11px; letter-spacing: 0.12em; text-transform: uppercase;
      color: #4a6640; text-decoration: none; font-weight: 400; transition: color 0.2s;
    }
    .nav-links a:hover { color: #2a2318; }

   .nav-links li { display: flex; align-items: center; }
   
    /* HERO */
    #hero {
      display: grid; grid-template-columns: 1fr 1fr;
      border-bottom: 2px solid #2a2318; min-height: 480px;
    }
    .hero-left {
      padding: 4rem 2.5rem; border-right: 2px solid #2a2318;
      display: flex; flex-direction: column; justify-content: center;
    }
    .hero-kicker {
      font-size: 10px; letter-spacing: 0.2em; text-transform: uppercase;
      color: #4a6640; margin-bottom: 1.8rem;
      display: flex; align-items: center; gap: 0.7rem;
    }
    .hero-kicker::before {
      content: ''; display: inline-block;
      width: 20px; height: 2px; background: #4a6640;
    }
    .hero-title {
      font-family: 'Fraunces', serif;
      font-size: clamp(3rem, 5vw, 4.8rem);
      font-weight: 600; line-height: 1.0;
      margin-bottom: 0.5rem; letter-spacing: -0.02em; color: #2a2318;
    }
    .hero-tagline {
      font-family: 'Fraunces', serif;
      font-size: clamp(1.1rem, 2vw, 1.5rem);
      font-weight: 300; font-style: italic;
      color: #2a8c2a; margin-bottom: 1.6rem;
    }
    .hero-sub {
      font-size: 13px; color: #7a6e5a;
      line-height: 1.85; max-width: 40ch; margin-bottom: 2.5rem;
    }
    .hero-btn {
      display: inline-flex; align-items: center; gap: 0.6rem;
      font-size: 11px; letter-spacing: 0.12em; text-transform: uppercase;
      color: #f0ebe0; background: #2a2318;
      padding: 0.8rem 2rem; text-decoration: none;
      width: fit-content; font-weight: 400; transition: background 0.2s;
    }
    .hero-btn:hover { background: #4a6640; }
    .hero-right { overflow: hidden; min-height: 480px; background: #e0d9c8; }
    .photo-label {
      display: flex; flex-direction: column;
      align-items: center; justify-content: center; gap: 1rem;
      width: 100%; height: 100%; min-height: 480px;
      background: #e0d9c8; cursor: pointer;
      transition: background 0.2s; border: none;
    }
    .photo-label:hover { background: #d8d0be; }
    .photo-label input[type="file"] { display: none; }
    .photo-preview { width: 100%; height: 100%; min-height: 480px; object-fit: cover; display: block; }
    .ph-icon {
      width: 56px; height: 56px; border: 1.5px solid #b0a890;
      border-radius: 50%; display: flex; align-items: center; justify-content: center;
    }
    .ph-label { font-size: 11px; letter-spacing: 0.14em; text-transform: uppercase; color: #9a9080; }
    .ph-hint  { font-size: 10px; color: #b0a890; letter-spacing: 0.08em; }

    /* SECTION BAR */
    .section-bar {
      display: flex; align-items: center; gap: 1.2rem;
      padding: 1rem 2.5rem;
      border-top: 2px solid #2a2318; border-bottom: 1px solid #c8c0ae;
      background: #e8e0ce;
    }
    .section-bar-num   { font-size: 10px; letter-spacing: 0.14em; color: #4a6640; text-transform: uppercase; }
    .section-bar-title { font-family: 'Fraunces', serif; font-size: 1.05rem; font-weight: 600; color: #2a2318; }

    /* ABOUT — lime green background, two columns */
    #about {
      display: grid; grid-template-columns: 2fr 1fr;
      gap: 4rem; padding: 3.5rem 2.5rem;
      border-bottom: 2px solid #2a2318; align-items: start;
      background: #c8ddb8;
    }
    .about-lead {
      font-family: 'Fraunces', serif;
      font-size: 1.35rem; font-weight: 300; line-height: 1.55; color: #1a2e14;
    }
    .about-lead em { font-style: italic; color: #1e6e1e; }
    .about-sub {
      margin-top: 1rem;
      font-size: 13px; color: #3a5a30; line-height: 1.85; max-width: 52ch;
    }
    .sidebar-item { padding: 0.85rem 0; border-bottom: 1px solid #8ab87a; }
    .sidebar-item:first-child { border-top: 1px solid #8ab87a; }
    .sidebar-key {
      font-size: 10px; letter-spacing: 0.16em; text-transform: uppercase;
      color: #2a5c2a; margin-bottom: 0.25rem;
    }
    .sidebar-val { font-size: 12px; color: #1a2e14; line-height: 1.6; }

    /* SKILLS — bordered squares, flood green on hover */
    #skills { border-bottom: 2px solid #2a2318; }
    .skills-grid {
      display: grid; grid-template-columns: repeat(3, 1fr);
      gap: 1px; background: #2a2318;
      border-bottom: 1px solid #2a2318;
    }
    .skill-card {
      padding: 2.5rem 2rem;
      background: #f0ebe0;
      transition: background 0.25s, color 0.25s;
      cursor: default;
    }
    .skill-card:hover { background: #3a7a30; }
    .skill-glyph {
      font-family: 'Fraunces', serif; font-size: 1.6rem;
      font-style: italic; color: #4a6640;
      margin-bottom: 0.6rem; line-height: 1;
      transition: color 0.25s;
    }
    .skill-card:hover .skill-glyph { color: #c8ddb8; }
    .skill-name {
      font-family: 'Fraunces', serif; font-size: 1.1rem;
      font-weight: 600; color: #2a2318; margin-bottom: 0.5rem;
      transition: color 0.25s;
    }
    .skill-card:hover .skill-name { color: #f0ebe0; }
    .skill-desc {
      font-size: 12px; color: #7a6e5a; line-height: 1.65;
      transition: color 0.25s;
    }
    .skill-card:hover .skill-desc { color: #c8ddb8; }

    /* WORK */
    #work { border-bottom: 2px solid #2a2318; }
    .work-list { display: flex; flex-direction: column; }
    .work-item {
      display: grid; grid-template-columns: auto 1fr auto;
      align-items: center; padding: 1.4rem 2.5rem;
      border-bottom: 1px solid #c8dab8; gap: 1.5rem;
      background: #f0ebe0; transition: background 0.2s;
    }
    .work-item:last-child { border-bottom: none; }
    .work-item:hover { background: #e8f0d8; }
    .work-index {
      font-family: 'Fraunces', serif; font-size: 1.4rem;
      font-weight: 300; font-style: italic; color: #a8c898; min-width: 2rem; line-height: 1;
    }
    .work-title {
      font-family: 'Fraunces', serif; font-size: 1.15rem;
      font-style: italic; font-weight: 300; color: #2a2318; margin-bottom: 0.3rem;
    }
    .work-desc { font-size: 11px; color: #7a6e5a; line-height: 1.6; max-width: 55ch; }
    .work-tag {
      font-size: 9px; letter-spacing: 0.14em; text-transform: uppercase;
      color: #f0ebe0; background: #3a7a30;
      padding: 0.3rem 0.8rem; white-space: nowrap; align-self: start; margin-top: 0.2rem;
    }

    /* CONTACT */
    #contact {
      display: grid; grid-template-columns: 1fr 1fr;
      gap: 4rem; padding: 3.5rem 2.5rem;
      border-bottom: 2px solid #2a2318;
      align-items: center; background: #e8e0ce;
    }
    .contact-intro {
      font-family: 'Fraunces', serif;
      font-size: clamp(1.6rem, 2.5vw, 2.2rem);
      font-weight: 300; line-height: 1.3; margin-bottom: 1rem; color: #2a2318;
    }
    .contact-intro em { font-style: italic; color: #2a8c2a; }
    .contact-sub { font-size: 13px; color: #7a6e5a; line-height: 1.8; }
    .contact-links { display: flex; flex-direction: column; }
    .contact-link {
      display: flex; justify-content: space-between; align-items: center;
      padding: 1.2rem 0; border-bottom: 1px solid #c8c0ae;
      text-decoration: none; color: #2a2318; transition: color 0.2s;
    }
    .contact-link:first-child { border-top: 1px solid #c8c0ae; }
    .contact-link:hover { color: #4a6640; }
    .contact-link-label { font-size: 13px; }
    .contact-link-type {
      font-size: 10px; letter-spacing: 0.14em;
      text-transform: uppercase; color: #4a6640;
    }

    /* FOOTER */
    footer {
      border-top: 2px solid #2a2318; padding: 1.2rem 2.5rem;
      display: flex; justify-content: space-between;
      font-size: 10px; letter-spacing: 0.1em;
      color: #9a9080; text-transform: uppercase; background: #f0ebe0;
    }

    /* SCROLL REVEAL */
    .reveal { opacity: 0; transform: translateY(16px); transition: opacity 0.6s ease, transform 0.6s ease; }
    .reveal.visible { opacity: 1; transform: none; }

    /* RESPONSIVE */
    @media (max-width: 768px) {
      nav { padding: 1.2rem 1.5rem; }
      #hero { grid-template-columns: 1fr; }
      .hero-left { padding: 3.5rem 1.5rem 2.5rem; border-right: none; }
      .hero-right, .photo-label { min-height: 300px; }
      #about { grid-template-columns: 1fr; gap: 2rem; padding: 2.5rem 1.5rem; }
      .skills-grid { grid-template-columns: 1fr; }
      .work-item { grid-template-columns: 2rem 1fr; padding: 1.2rem 1.5rem; }
      .work-tag { display: none; }
      #contact { grid-template-columns: 1fr; gap: 2rem; padding: 2.5rem 1.5rem; }
      .section-bar { padding: 0.9rem 1.5rem; }
      footer { flex-direction: column; gap: 0.4rem; text-align: center; }
    }
  </style>
</head>
<body>

  <nav>
    <a class="logo" href="#hero">Sarah Sawtelle</a>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#work">Work</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <section id="hero">
    <div class="hero-left">
      <p class="hero-kicker">Portfolio — Science Communication & Environmental Design</p>
      <h1 class="hero-title">Sarah<br>Sawtelle</h1>
      <p class="hero-tagline">Where Nature meets Narrative.</p>
      <p class="hero-sub">Social media and interpretive signage rooted in natural history, science communication, and environmental education.</p>
      <a href="#work" class="hero-btn">View Work →</a>
    </div>
    <div class="hero-right">
      <label class="photo-label" id="photo-label">
        <input type="file" accept="image/*" onchange="previewPhoto(event)">
        <div class="ph-icon">
          <svg width="22" height="22" viewBox="0 0 24 24" fill="none">
            <rect x="3" y="5" width="18" height="14" rx="2" stroke="#9a9080" stroke-width="1.2"/>
            <circle cx="12" cy="12" r="3.5" stroke="#9a9080" stroke-width="1.2"/>
            <path d="M8 5l1.5-2h5L16 5" stroke="#9a9080" stroke-width="1.2" stroke-linecap="round"/>
          </svg>
        </div>
        <span class="ph-label">Your Photo Here</span>
        <span class="ph-hint">Click to upload</span>
      </label>
    </div>
  </section>

  <div class="section-bar reveal">
    <span class="section-bar-num">01 —</span>
    <span class="section-bar-title">About</span>
  </div>
  <section id="about" class="reveal">
    <div>
      <p class="about-lead">A designer rooted in <em>natural history</em> and <em>environmental education</em> — translating the complexity of the natural world into stories people want to read.</p>
      <p class="about-sub">Whether on a trail sign or an Instagram feed, I make science accessible, accurate, and beautiful. My work spans parks, museums, conservation nonprofits, and environmental education programs.</p>
    </div>
    <div>
      <div class="sidebar-item">
        <div class="sidebar-key">Location</div>
        <div class="sidebar-val">San Francisco, CA</div>
      </div>
      <div class="sidebar-item">
        <div class="sidebar-key">Specialties</div>
        <div class="sidebar-val">Social Media Design<br>Science Communication<br>Interpretive Sign Design<br>Natural History Program Development</div>
      </div>
      <div class="sidebar-item">
        <div class="sidebar-key">Available For</div>
        <div class="sidebar-val">Freelance & Contract</div>
      </div>
    </div>
  </section>

  <div class="section-bar reveal">
    <span class="section-bar-num">02 —</span>
    <span class="section-bar-title">Skills & Specialisms</span>
  </div>
  <section id="skills" class="reveal">
    <div class="skills-grid">
      <div class="skill-card">
        <div class="skill-glyph">◈</div>
        <div class="skill-name">Social Media Design</div>
        <div class="skill-desc">Feed graphics, stories, reels covers, and campaign assets for Instagram, Facebook, LinkedIn, and more.</div>
      </div>
      <div class="skill-card">
        <div class="skill-glyph">◉</div>
        <div class="skill-name">Interpretive Sign Design</div>
        <div class="skill-desc">Educational and wayfinding signs for parks, trails, and museums — designed for clarity and durability.</div>
      </div>
      <div class="skill-card">
        <div class="skill-glyph">◎</div>
        <div class="skill-name">Science Storytelling</div>
        <div class="skill-desc">Translating natural history and ecology into engaging, accurate visual narratives for broad audiences.</div>
      </div>
    </div>
  </section>

  <div class="section-bar reveal">
    <span class="section-bar-num">03 —</span>
    <span class="section-bar-title">Selected Work</span>
  </div>
  <section id="work" class="reveal">
    <div class="work-list">
      <div class="work-item">
        <span class="work-index">01</span>
        <div>
          <div class="work-title">Nature Trail Interpretive Signs</div>
          <div class="work-desc">Educational wayfinding series for a regional nature preserve — ecology, flora, fauna, and trail information for visitors of all ages.</div>
        </div>
        <span class="work-tag">Signage</span>
      </div>
      <div class="work-item">
        <span class="work-index">02</span>
        <div>
          <div class="work-title">Conservation Nonprofit Social Campaign</div>
          <div class="work-desc">Ongoing social media content design — event promotions, donor campaigns, and brand-consistent story templates.</div>
        </div>
        <span class="work-tag">Social Media</span>
      </div>
      <div class="work-item">
        <span class="work-index">03</span>
        <div>
          <div class="work-title">Natural History Museum Exhibit Panels</div>
          <div class="work-desc">Interpretive panels for a traveling natural history exhibit — dense scientific content made approachable through layout and visual hierarchy.</div>
        </div>
        <span class="work-tag">Signage</span>
      </div>
      <div class="work-item">
        <span class="work-index">04</span>
        <div>
          <div class="work-title">Environmental Education Program Identity</div>
          <div class="work-desc">Visual identity and social rollout for a nature-based education program — launch grid, story highlights, and weekly content templates.</div>
        </div>
        <span class="work-tag">Social Media</span>
      </div>
    </div>
  </section>

  <div class="section-bar reveal">
    <span class="section-bar-num">04 —</span>
    <span class="section-bar-title">Get in Touch</span>
  </div>
  <section id="contact" class="reveal">
    <div>
      <p class="contact-intro">Let's make something<br><em>worth seeing.</em></p>
      <p class="contact-sub">Whether you need social content, interpretive signage, or science communication design, I'd love to hear about your project.</p>
    </div>
    <div class="contact-links">
      <a href="mailto:sarah.e.sawtelle@gmail.com" class="contact-link">
        <span class="contact-link-label">sarah.e.sawtelle@gmail.com</span>
        <span class="contact-link-type">Email →</span>
      </a>
    </div>
  </section>

  <footer>
    <span>© 2026 Sarah Sawtelle</span>
    <span>Natural History · Science Communication · Environmental Design</span>
  </footer>

  <script>
    function previewPhoto(event) {
      const file = event.target.files[0];
      if (!file) return;
      const reader = new FileReader();
      reader.onload = function(e) {
        const label = document.getElementById('photo-label');
        label.innerHTML = '<img class="photo-preview" src="' + e.target.result + '" alt="Sarah Sawtelle">';
      };
      reader.readAsDataURL(file);
    }
    const reveals = document.querySelectorAll('.reveal');
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) { entry.target.classList.add('visible'); observer.unobserve(entry.target); }
      });
    }, { threshold: 0.08 });
    reveals.forEach(el => observer.observe(el));
  </script>
</body>
</html>
