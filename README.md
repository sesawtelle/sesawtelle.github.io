
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
      background: #f0ebe0; color: #2a2318;
      font-family: 'DM Sans', sans-serif; font-weight: 300; overflow-x: hidden;
    }

    /* NAV — logo only */
    nav {
      position: sticky; top: 0; z-index: 100;
      display: flex; align-items: center; justify-content: space-between;
      padding: 1.4rem 2.5rem;
      border-bottom: 2px solid #2a2318;
      background: #f0ebe0;
    }
    .nav-links { display: flex; align-items: center; gap: 2.2rem; }
    .nav-link {
      font-size: 10px; letter-spacing: 0.14em; text-transform: uppercase;
      color: #2a2318; text-decoration: none; transition: color 0.2s;
    }
    .nav-link:hover { color: #4a6640; }
    @media (max-width: 768px) { .nav-links { display: none; } }
    .logo {
      font-family: 'Fraunces', serif; font-size: 1.1rem;
      font-weight: 300; font-style: italic;
      color: #2a2318; text-decoration: none;
    }

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
      content: ''; display: inline-block; width: 20px; height: 2px; background: #4a6640;
    }
    .hero-title {
      font-family: 'Fraunces', serif; font-size: clamp(3rem, 5vw, 4.8rem);
      font-weight: 600; line-height: 1.0; margin-bottom: 0.5rem;
      letter-spacing: -0.02em; color: #2a2318;
    }
    .hero-tagline {
      font-family: 'Fraunces', serif; font-size: clamp(1.1rem, 2vw, 1.5rem);
      font-weight: 300; font-style: italic; color: #2a8c2a; margin-bottom: 1.6rem;
    }
    .hero-sub {
      font-size: 13px; color: #7a6e5a; line-height: 1.85; max-width: 40ch; margin-bottom: 2.5rem;
    }
    .hero-btn {
      display: inline-flex; align-items: center; gap: 0.6rem;
      font-size: 11px; letter-spacing: 0.12em; text-transform: uppercase;
      color: #f0ebe0; background: #2a2318; padding: 0.8rem 2rem;
      text-decoration: none; width: fit-content; font-weight: 400; transition: background 0.2s;
    }
    .hero-btn:hover { background: #4a6640; }
    .hero-right { overflow: hidden; min-height: 480px; }
    .hero-photo { width: 100%; height: 100%; min-height: 480px; object-fit: cover; display: block; }

    /* SECTION BAR */
    .section-bar {
      display: flex; align-items: center; gap: 1.2rem; padding: 1rem 2.5rem;
      border-top: 2px solid #2a2318; border-bottom: 1px solid #c8c0ae; background: #e8e0ce;
    }
    .section-bar-num   { font-size: 10px; letter-spacing: 0.14em; color: #4a6640; text-transform: uppercase; }
    .section-bar-title { font-family: 'Fraunces', serif; font-size: 1.05rem; font-weight: 600; color: #2a2318; }

    /* ABOUT */
    #about {
      display: grid; grid-template-columns: 2fr 1fr; gap: 4rem; padding: 3.5rem 2.5rem;
      border-bottom: 2px solid #2a2318; align-items: start; background: #c8ddb8;
    }
    .about-lead {
      font-family: 'Fraunces', serif; font-size: 1.35rem; font-weight: 300;
      line-height: 1.55; color: #1a2e14;
    }
    .about-lead em { font-style: italic; color: #1e6e1e; }
    .about-sub { margin-top: 1rem; font-size: 13px; color: #3a5a30; line-height: 1.85; max-width: 52ch; }
    .sidebar-item { padding: 0.85rem 0; border-bottom: 1px solid #8ab87a; }
    .sidebar-item:first-child { border-top: 1px solid #8ab87a; }
    .sidebar-key { font-size: 10px; letter-spacing: 0.16em; text-transform: uppercase; color: #2a5c2a; margin-bottom: 0.25rem; }
    .sidebar-val { font-size: 14px; color: #1a2e14; line-height: 1.6; }

    /* SKILLS */
    #skills { border-bottom: 2px solid #2a2318; }
    .skills-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1px; background: #2a2318; }
    .skill-card { padding: 2.5rem 2rem; background: #f0ebe0; transition: background 0.25s; cursor: default; }
    .skill-card:hover { background: #3a7a30; }
    .skill-glyph { font-family: 'Fraunces', serif; font-size: 1.6rem; font-style: italic; color: #4a6640; margin-bottom: 0.6rem; line-height: 1; transition: color 0.25s; }
    .skill-card:hover .skill-glyph { color: #c8ddb8; }
    .skill-name { font-family: 'Fraunces', serif; font-size: 1.1rem; font-weight: 600; color: #2a2318; margin-bottom: 0.5rem; transition: color 0.25s; }
    .skill-card:hover .skill-name { color: #f0ebe0; }
    .skill-desc { font-size: 12px; color: #7a6e5a; line-height: 1.65; transition: color 0.25s; }
    .skill-card:hover .skill-desc { color: #c8ddb8; }

    /* WORK */
    #work { border-bottom: 2px solid #2a2318; }
    .project { padding: 2.8rem 2.5rem; border-bottom: 1px solid #c8dab8; }
    .project:last-child { border-bottom: none; }
    .project-top { display: grid; grid-template-columns: 3rem 1fr; gap: 1.5rem; margin-bottom: 1.8rem; align-items: start; }
    .project-index { font-family: 'Fraunces', serif; font-size: 1.4rem; font-weight: 300; font-style: italic; color: #a8c898; line-height: 1; display: flex; align-items: flex-start; }
    .work-tag { font-size: 9px; letter-spacing: 0.14em; text-transform: uppercase; color: #f0ebe0; background: #3a7a30; padding: 0.3rem 0.8rem; white-space: nowrap; display: inline-block; margin-bottom: 0.6rem; }
    .project-org { font-size: 10px; letter-spacing: 0.16em; text-transform: uppercase; color: #4a6640; margin-bottom: 0.3rem; }
    .project-title { font-family: 'Fraunces', serif; font-size: 1.3rem; font-weight: 300; font-style: italic; color: #2a2318; margin-bottom: 0.7rem; }
    .project-desc { font-size: 14px; color: #7a6e5a; line-height: 1.78; }
    /* Instagram grid */
    .project-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 0.6rem; }
    .project-grid-link { display: block; overflow: hidden; aspect-ratio: 1 / 1; }
    .project-grid-link img { width: 100%; height: 100%; object-fit: cover; display: block; transition: transform 0.35s; }
    .project-grid-link:hover img { transform: scale(1.04); }
    /* Instagram profile screenshot */
    .project-desc-row { display: grid; grid-template-columns: 1fr 260px; gap: 2rem; align-items: start; }
    .project-profile-img { width: 100%; display: block; border: 1px solid #c8c0ae; }
    /* Social profile cards */
    .social-cards { display: flex; flex-direction: column; gap: 0.35rem; }
    .ig-card-link { display: block; text-decoration: none; }
    .ig-card-link:hover .ig-profile-card { border-color: #4a6640; }
    .ig-profile-card { border: 1px solid #c8c0ae; padding: 0.55rem 0.8rem; background: #f0ebe0; transition: border-color 0.2s; }
    .ig-profile-header { display: flex; align-items: center; gap: 0.6rem; padding-bottom: 0.4rem; border-bottom: 1px solid #c8c0ae; margin-bottom: 0.35rem; }
    .ig-avatar { width: 24px; height: 24px; display: flex; align-items: center; justify-content: center; flex-shrink: 0; }
    .ig-handle { font-size: 10px; font-weight: 400; letter-spacing: 0.06em; color: #2a2318; margin-bottom: 0.15rem; }
    .ig-platform { font-size: 8px; letter-spacing: 0.14em; text-transform: uppercase; color: #7a6e5a; }
    .ig-stats { display: flex; justify-content: space-around; text-align: center; }
    .ig-stat { padding: 0.15rem 0.5rem; border-right: 1px solid #c8c0ae; flex: 1; }
    .ig-stat:last-child { border-right: none; }
    .ig-stat-num { font-family: 'Fraunces', serif; font-size: 0.88rem; font-weight: 600; color: #2a2318; display: block; line-height: 1.2; }
    .ig-stat-label { font-size: 7.5px; letter-spacing: 0.12em; text-transform: uppercase; color: #7a6e5a; display: block; margin-top: 0.1rem; }
    /* YouTube layout */
    .project-layout { display: grid; grid-template-columns: 1fr 1fr; gap: 3rem; align-items: center; }
    .project-img-link { display: block; overflow: hidden; border: 1px solid #c8c0ae; }
    .project-img-link img { width: 100%; display: block; transition: transform 0.35s; }
    .project-img-link:hover img { transform: scale(1.03); }

    /* CONTACT */
    #contact {
      display: grid; grid-template-columns: 1fr 1fr; gap: 4rem; padding: 3.5rem 2.5rem;
      border-bottom: 2px solid #2a2318; align-items: center; background: #e8e0ce;
    }
    .contact-intro { font-family: 'Fraunces', serif; font-size: clamp(1.6rem, 2.5vw, 2.2rem); font-weight: 300; line-height: 1.3; margin-bottom: 1rem; color: #2a2318; }
    .contact-intro em { font-style: italic; color: #2a8c2a; }
    .contact-sub { font-size: 13px; color: #7a6e5a; line-height: 1.8; }
    .contact-links { display: flex; flex-direction: column; }
    .contact-link { display: flex; justify-content: space-between; align-items: center; padding: 1.2rem 0; border-bottom: 1px solid #c8c0ae; text-decoration: none; color: #2a2318; transition: color 0.2s; }
    .contact-link:first-child { border-top: 1px solid #c8c0ae; }
    .contact-link:hover { color: #4a6640; }
    .contact-link-label { font-size: 13px; }
    .contact-link-type { font-size: 10px; letter-spacing: 0.14em; text-transform: uppercase; color: #4a6640; }

    /* CONTACT FORM */
    .contact-form { display: flex; flex-direction: column; gap: 1rem; }
    .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
    .form-field { display: flex; flex-direction: column; gap: 0.35rem; }
    .form-field label { font-size: 10px; letter-spacing: 0.16em; text-transform: uppercase; color: #4a6640; }
    .form-field input,
    .form-field textarea {
      background: #f0ebe0; border: 1px solid #c8c0ae; color: #2a2318;
      font-family: 'DM Sans', sans-serif; font-size: 13px; font-weight: 300;
      padding: 0.75rem 1rem; outline: none; transition: border-color 0.2s; resize: none; width: 100%;
    }
    .form-field input:focus,
    .form-field textarea:focus { border-color: #4a6640; }
    .form-field input::placeholder,
    .form-field textarea::placeholder { color: #b0a890; }
    .form-submit {
      display: inline-flex; align-items: center; gap: 0.6rem; justify-content: center;
      font-size: 11px; letter-spacing: 0.12em; text-transform: uppercase;
      color: #f0ebe0; background: #2a2318; padding: 0.85rem 2rem;
      border: none; cursor: pointer; font-family: 'DM Sans', sans-serif; font-weight: 400;
      transition: background 0.2s; width: 100%;
    }
    .form-submit:hover { background: #4a6640; }
    .form-success {
      display: none; font-size: 13px; color: #2a8c2a; padding: 0.75rem 1rem;
      border: 1px solid #8ab87a; background: #c8ddb820; text-align: center;
    }

    /* SITE WRAPPER */
    .site-wrap { max-width: 1140px; margin: 0 auto; }

    /* FOOTER */
    footer {
      border-top: 2px solid #2a2318; padding: 1.2rem 2.5rem;
      display: flex; justify-content: space-between;
      font-size: 10px; letter-spacing: 0.1em; color: #9a9080; text-transform: uppercase; background: #f0ebe0;
    }

    /* SCROLL REVEAL */
    .reveal { opacity: 0; transform: translateY(16px); transition: opacity 0.6s ease, transform 0.6s ease; }
    .reveal.visible { opacity: 1; transform: none; }

    /* RESPONSIVE */
    @media (max-width: 768px) {
      nav { padding: 1.2rem 1.5rem; }
      #hero { grid-template-columns: 1fr; }
      .hero-left { padding: 3.5rem 1.5rem 2.5rem; border-right: none; }
      .hero-right, .hero-photo { min-height: 300px; }
      #about { grid-template-columns: 1fr; gap: 2rem; padding: 2.5rem 1.5rem; }
      .skills-grid { grid-template-columns: 1fr; }
      .project { padding: 2rem 1.5rem; }
      .project-grid { gap: 0.4rem; }
      .project-desc-row { grid-template-columns: 1fr; }
      .project-layout { grid-template-columns: 1fr; gap: 1.5rem; }
      #contact { grid-template-columns: 1fr; gap: 2rem; padding: 2.5rem 1.5rem; }
      .section-bar { padding: 0.9rem 1.5rem; }
      footer { flex-direction: column; gap: 0.4rem; text-align: center; }
    }
  </style>
</head>
<body>

<div class="site-wrap">

  <section id="hero">
    <div class="hero-left">
      <p style="font-family: 'Fraunces', serif; font-size: 2.2rem; font-weight: 600; color: #4a6640; margin-bottom: 1rem; letter-spacing: -0.01em;">Portfolio</p>
      <h1 class="hero-title" style="color: #7a4a1a;">Sarah Sawtelle</h1>
      <div class="sidebar-item">
        <div class="sidebar-key">Location</div>
        <div class="sidebar-val">San Francisco, CA</div>
      </div>
      <div class="sidebar-item">
        <div class="sidebar-key">About Me</div>
        <div class="sidebar-val">Informal science educator who crafts stories that spark awe and appreciation for the natural world. I work with conservation organizations, parks, museums, and cultural institutions throughout the Bay Area and beyond. Let me help you by creating compelling social media posts, inspiring interpretive signs, or lively educational programs. I also have experience in volunteer coordination, project management, and public speaking.</div>
      </div>
      <div class="sidebar-item">
        <div class="sidebar-key">Available For</div>
        <div class="sidebar-val">Freelance & Contract</div>
      </div>
    </div>
    <div class="hero-right">
      <img class="hero-photo" src="hero.jpg" alt="Interior of the San Francisco Conservatory of Flowers — Giant Victoria water lily pads floating in the tropical pond">
    </div>
  </section>

  <section id="skills" class="reveal">
    <div class="skills-grid">
      <a href="#work" style="text-decoration: none; color: inherit; display: contents;">
      <div class="skill-card">
        <div class="skill-glyph">◈</div>
        <div class="skill-name">Social Media</div>
        <div class="skill-desc">Visual storytelling across Instagram, Facebook, YouTube, and more. Original photography, video, design, and writing to share your organization's story.</div>
      </div>
      </a>
      <a href="#signs" style="text-decoration: none; color: inherit; display: contents;">
      <div class="skill-card">
        <div class="skill-glyph">◉</div>
        <div class="skill-name">Interpretive Sign Development</div>
        <div class="skill-desc">Educational signs for museums, parks, and gardens.</div>
      </div>
      </a>
      <a href="#storytelling" style="text-decoration: none; color: inherit; display: contents;">
      <div class="skill-card">
        <div class="skill-glyph">◎</div>
        <div class="skill-name">Science Storytelling</div>
        <div class="skill-desc">Translating natural history and ecology into engaging programs for broad audiences.</div>
      </div>
      </a>
    </div>
  </section>

  <div class="section-bar reveal">
    <span class="section-bar-title">Social Media</span>
  </div>
  <section id="work" class="reveal">

    <!-- Project 01: Instagram -->
    <div class="project">
      <div class="project-top" style="grid-template-columns: 3rem 1fr 260px;">
        <span class="project-index"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="28" height="28" fill="none" stroke="#a8c898" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M11 20A7 7 0 0 1 9.8 6.1C15.5 5 17 4.48 19 2c1 2 2 4.18 2 8 0 5.5-4.78 10-10 10Z"/><path d="M2 21c0-3 1.85-5.36 5.08-6C9.5 14.52 12 13 13 12"/></svg></span>
        <div>
          <h2 style="font-family: 'Fraunces', serif; font-size: 1.6rem; font-weight: 600; color: #2a2318; margin-top: -0.2rem; margin-bottom: 0.5rem; line-height: 1;">San Francisco Conservatory of Flowers</h2>
          <div class="project-desc">
              <b>January 2021 – December 2022 · Interim Communications Manager</b>
              <ul style="margin-top: 0.7rem; padding-left: 1.2em; display: flex; flex-direction: column; gap: 0.5rem;">
                <li>Took dazzling photos and videos of tropical plants, shared alongside their botanical backstories on Instagram, YouTube, and Facebook.</li>
                <li>Filmed reels that took viewers behind-the-scenes to dive underwater with Giant Water Lilies, and witness the ephemeral night bloom of a cactus flower.</li>
                <li>Used Hootsuite to create content calendar, schedule posts, and manage posting across multiple platforms.</li>
                <li>Coordinated with events, retail, horticulture and operations teams to share news from across the organization with more than 60,000 followers.</li>
              </ul>
            </div>
          </div>
            <div class="social-cards">
              <!-- Instagram -->
              <a class="ig-card-link" href="https://www.instagram.com/conservatoryofflowers/" target="_blank" rel="noopener">
              <div class="ig-profile-card">
                <div class="ig-profile-header">
                  <div class="ig-avatar">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24">
                      <defs>
                        <radialGradient id="ig-g" cx="30%" cy="107%" r="150%">
                          <stop offset="0%" stop-color="#fdf497"/>
                          <stop offset="45%" stop-color="#fd5949"/>
                          <stop offset="60%" stop-color="#d6249f"/>
                          <stop offset="90%" stop-color="#285AEB"/>
                        </radialGradient>
                      </defs>
                      <rect width="24" height="24" rx="5.5" fill="url(#ig-g)"/>
                      <circle cx="12" cy="12" r="4.5" fill="none" stroke="#fff" stroke-width="1.8"/>
                      <circle cx="17.5" cy="6.5" r="1.1" fill="#fff"/>
                    </svg>
                  </div>
                  <div>
                    <div class="ig-handle">@conservatoryofflowers</div>
                    <div class="ig-platform">Instagram</div>
                  </div>
                </div>
                <div class="ig-stats">
                  <div class="ig-stat"><span class="ig-stat-num">660</span><span class="ig-stat-label">Posts</span></div>
                  <div class="ig-stat"><span class="ig-stat-num">67K</span><span class="ig-stat-label">Followers</span></div>
                </div>
              </div>
              </a>
              <!-- YouTube -->
              <a class="ig-card-link" href="https://www.youtube.com/@ConservatoryofFlowers" target="_blank" rel="noopener">
              <div class="ig-profile-card">
                <div class="ig-profile-header">
                  <div class="ig-avatar">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24">
                      <rect width="24" height="24" rx="5" fill="#FF0000"/>
                      <polygon points="10,7.5 10,16.5 18,12" fill="#fff"/>
                    </svg>
                  </div>
                  <div>
                    <div class="ig-handle">Conservatory of Flowers</div>
                    <div class="ig-platform">YouTube</div>
                  </div>
                </div>
                <div class="ig-stats">
                  <div class="ig-stat" style="border-right: none;"><span class="ig-stat-num">1K</span><span class="ig-stat-label">Subscribers</span></div>
                </div>
              </div>
              </a>
              <!-- Facebook -->
              <a class="ig-card-link" href="https://www.facebook.com/ConservatoryofFlowers" target="_blank" rel="noopener">
              <div class="ig-profile-card">
                <div class="ig-profile-header">
                  <div class="ig-avatar">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24">
                      <rect width="24" height="24" rx="5" fill="#1877F2"/>
                      <path d="M13.5 8H15V5.5h-1.5C11.57 5.5 10 7.07 10 9v1.5H8V13h2v8h3v-8h2l.5-2.5H13V9c0-.28.22-.5.5-.5z" fill="#fff"/>
                    </svg>
                  </div>
                  <div>
                    <div class="ig-handle">@conservatoryofflowers</div>
                    <div class="ig-platform">Facebook</div>
                  </div>
                </div>
                <div class="ig-stats">
                  <div class="ig-stat" style="border-right: none;"><span class="ig-stat-num">23K</span><span class="ig-stat-label">Followers</span></div>
                </div>
              </div>
              </a>
            </div>
      </div>
      <div class="project-grid">
        <a class="project-grid-link" href="https://www.instagram.com/p/CQuWaavLb33/" target="_blank" rel="noopener">
          <img src="images/work-01.png" alt="Bat Flower trivia post — Instagram @ SF Conservatory of Flowers" loading="lazy">
        </a>
        <a class="project-grid-link" href="https://www.instagram.com/p/Chk3u_SDijd/?hl=en" target="_blank" rel="noopener">
          <img src="images/work-02.png" alt="Instagram post — SF Conservatory of Flowers" loading="lazy">
        </a>
        <a class="project-grid-link" href="https://www.instagram.com/p/CcGPQgtp826/?hl=en&img_index=1" target="_blank" rel="noopener">
          <img src="images/work-03.png" alt="Instagram post — SF Conservatory of Flowers" loading="lazy">
        </a>
        <a class="project-grid-link" href="https://www.instagram.com/p/CeEmW9vlS5r/?hl=en" target="_blank" rel="noopener">
          <img src="images/work-04.png" alt="Instagram post — SF Conservatory of Flowers" loading="lazy">
        </a>
        <a class="project-grid-link" href="https://www.instagram.com/p/Ci0N9EjJzFF/?hl=en" target="_blank" rel="noopener">
          <img src="images/work-05.png" alt="Instagram post — SF Conservatory of Flowers" loading="lazy">
        </a>
        <a class="project-grid-link" href="https://www.instagram.com/p/CezZZv6jnNj/?hl=en" target="_blank" rel="noopener">
          <img src="images/work-06.png" alt="Instagram post — SF Conservatory of Flowers" loading="lazy">
        </a>
      </div>
      <div style="padding-top: 1.8rem; padding-left: 4.5rem;">
        <div class="project-layout" style="gap: 2rem; align-items: start;">
          <div>
            <h3 class="project-title" style="font-family: 'Fraunces', serif; font-size: 1.1rem; font-weight: 300; font-style: italic; color: #2a2318; margin-bottom: 0.3rem;">YouTube Live — Corpse Flower Bloom</h3>
            <ul class="project-desc" style="padding-left: 1.2em; display: flex; flex-direction: column; gap: 0.5rem;">
              <li>Produced and streamed a series of YouTube Live educational programs that attracted over 5,000 viewers to learn about Corpse Flower natural history and conservation.</li>
              <li>Moderated online livestream of Corpse Flower bloom that drew 60,000+ viewers.</li>
            </ul>
          </div>
          <a class="project-img-link" href="https://www.youtube.com/watch?v=ACjMx4KxkaI" target="_blank" rel="noopener" style="align-self: start; max-width: 75%;">
            <img src="https://images.squarespace-cdn.com/content/v1/68cb081869dddd79cbb02fc0/cec56368-a745-47da-be9a-7c0e766388af/Screenshot+2025-09-18+at+9.13.02%E2%80%AFAM.png" alt="YouTube Live — Corpse Flower Bloom at SF Conservatory of Flowers" loading="lazy">
          </a>
        </div>
      </div>
    </div>

    <!-- Project 02: Secrets of Golden Gate Park -->
    <div class="project">
      <div class="project-top">
        <span class="project-index"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="28" height="28" fill="none" stroke="#a8c898" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M5 21c.5 -4.5 2.5 -8 7 -10"/><path d="M9 18c6.218 0 10.5 -3.288 11 -12v-2h-4.014c-9 0 -11.986 4 -12 9c0 1 0 3 2 5h3z"/></svg></span>
        <div>
          <h2 style="font-family: 'Fraunces', serif; font-size: 1.6rem; font-weight: 600; color: #2a2318; margin-top: -0.2rem; margin-bottom: 0.5rem; line-height: 1;">Secret Golden Gate Park</h2>
          <div class="project-desc-row">
            <div class="project-desc">
              <b>February – April 2026 · Freelance Social Media Manager</b>
              <ul style="margin-top: 0.7rem; padding-left: 1.2em; display: flex; flex-direction: column; gap: 0.5rem;">
                <li>Created and posted Instagram reels, stories and posts in support of the release of <em>Golden Gate Park: A Local's Guide</em> and related book events.</li>
                <li>Collaborated to develop brand style for a client with a preference for bold, eye-popping and text-intensive posts.</li>
                <li>Integrated @secretgoldengatepark Instagram with Canva, Metricool and Linktree.</li>
              </ul>
            </div>
            <div class="social-cards">
              <a class="ig-card-link" href="https://www.instagram.com/secretgoldengatepark/" target="_blank" rel="noopener">
              <div class="ig-profile-card">
                <div class="ig-profile-header">
                  <div class="ig-avatar">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24">
                      <defs>
                        <radialGradient id="ig-g2" cx="30%" cy="107%" r="150%">
                          <stop offset="0%" stop-color="#fdf497"/>
                          <stop offset="45%" stop-color="#fd5949"/>
                          <stop offset="60%" stop-color="#d6249f"/>
                          <stop offset="90%" stop-color="#285AEB"/>
                        </radialGradient>
                      </defs>
                      <rect width="24" height="24" rx="5.5" fill="url(#ig-g2)"/>
                      <circle cx="12" cy="12" r="4.5" fill="none" stroke="#fff" stroke-width="1.8"/>
                      <circle cx="17.5" cy="6.5" r="1.1" fill="#fff"/>
                    </svg>
                  </div>
                  <div>
                    <div class="ig-handle">@secretgoldengatepark</div>
                    <div class="ig-platform">Instagram</div>
                  </div>
                </div>
                <div class="ig-stats">
                  <div class="ig-stat" style="border-right: none;"><span class="ig-stat-num">227</span><span class="ig-stat-label">Followers</span></div>
                </div>
              </div>
              </a>
            </div>
          </div>
        </div>
      </div>
      <div class="project-grid">
        <a class="project-grid-link" href="https://www.instagram.com/p/DVJtoNpFbdt/" target="_blank" rel="noopener">
          <img src="images/ggp-01.png" alt="Instagram post — Secrets of Golden Gate Park" loading="lazy" style="object-position: top;">
        </a>
        <a class="project-grid-link" href="https://www.instagram.com/p/DVUCEhYFP6a/?img_index=1" target="_blank" rel="noopener">
          <img src="images/ggp-02.png" alt="Instagram post — Secrets of Golden Gate Park" loading="lazy" style="object-position: top;">
        </a>
        <a class="project-grid-link" href="https://www.instagram.com/stories/highlights/18434294539112364/" target="_blank" rel="noopener">
          <img src="images/ggp-03.png" alt="Instagram post — Secrets of Golden Gate Park" loading="lazy" style="object-position: center 30%;">
        </a>
        <a class="project-grid-link" href="https://www.instagram.com/p/DWeb8zajKOp/" target="_blank" rel="noopener">
          <img src="images/ggp-04.png" alt="Instagram post — Secrets of Golden Gate Park" loading="lazy" style="object-position: bottom;">
        </a>
        <a class="project-grid-link" href="https://www.instagram.com/p/DVFtcj7gGx7/?img_index=1" target="_blank" rel="noopener">
          <img src="images/ggp-05.png" alt="Instagram post — Secrets of Golden Gate Park" loading="lazy" style="object-position: top;">
        </a>
        <a class="project-grid-link" href="https://www.instagram.com/p/DVXs45vjTk7/" target="_blank" rel="noopener">
          <img src="images/ggp-06.png" alt="Instagram post — Secrets of Golden Gate Park" loading="lazy" style="object-position: top;">
        </a>
      </div>
    </div>

  </section>

  <div class="section-bar reveal">
    <span class="section-bar-title">Interpretive Sign Development</span>
  </div>

  <section id="signs" class="reveal">
    <div class="project">
      <div class="project-top">
        <span class="project-index"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="28" height="28" fill="none" stroke="#a8c898" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M5 21c.5 -4.5 2.5 -8 7 -10"/><path d="M9 18c6.218 0 10.5 -3.288 11 -12v-2h-4.014c-9 0 -11.986 4 -12 9c0 1 0 3 2 5h3z"/></svg></span>
        <div>
          <h2 style="font-family: 'Fraunces', serif; font-size: 1.6rem; font-weight: 600; color: #2a2318; margin-top: -0.2rem; margin-bottom: 0.5rem; line-height: 1;">Gardens of Golden Gate Park &amp; Conservatory of Flowers</h2>
          <p class="project-desc"><b>2019 – 2024 · Interpretation and Engagement Manager</b></p>
        </div>
      </div>
      <div class="project-grid">
        <a class="project-grid-link" href="images/sign-01.png" target="_blank" rel="noopener">
          <img src="images/sign-01.png" alt="Interpretive sign — Gardens of Golden Gate Park / Conservatory of Flowers" loading="lazy" style="transform: scale(1.4); transform-origin: left 28%;">
        </a>
        <a class="project-grid-link" href="images/sign-02.png" target="_blank" rel="noopener">
          <img src="images/sign-02.png" alt="Interpretive sign — Gardens of Golden Gate Park / Conservatory of Flowers" loading="lazy" style="transform: scale(3); transform-origin: right center;">
        </a>
        <a class="project-grid-link" href="images/sign-03.png" target="_blank" rel="noopener">
          <img src="images/sign-03.png" alt="Interpretive sign — Gardens of Golden Gate Park / Conservatory of Flowers" loading="lazy">
        </a>
        <a class="project-grid-link" href="images/sign-04.png" target="_blank" rel="noopener">
          <img src="images/sign-04.png" alt="Interpretive sign — Gardens of Golden Gate Park / Conservatory of Flowers" loading="lazy">
        </a>
        <a class="project-grid-link" href="images/sign-05.jpg" target="_blank" rel="noopener">
          <img src="images/sign-05.jpg" alt="Interpretive sign — Gardens of Golden Gate Park / Conservatory of Flowers" loading="lazy" style="transform: scale(2.2); transform-origin: right center;">
        </a>
        <a class="project-grid-link" href="images/sign-06.png" target="_blank" rel="noopener">
          <img src="images/sign-06.png" alt="Interpretive sign — Gardens of Golden Gate Park / Conservatory of Flowers" loading="lazy" style="transform: scale(1.6); transform-origin: right bottom;">
        </a>
      </div>
    </div>
  </section>

  <div class="section-bar reveal">
    <span class="section-bar-title">Science Storytelling</span>
  </div>

  <section id="storytelling" class="reveal">
    <div class="project">
      <p class="project-desc">Content coming soon.</p>
    </div>
  </section>

  <div class="section-bar reveal">
    <span class="section-bar-title">Get in Touch</span>
  </div>
  <section id="contact" class="reveal">
    <div>
      <p class="contact-intro">Let's make something<br><em>worth seeing.</em></p>
      <p class="contact-sub">Whether you need social content, interpretive signage, or science communication design, I'd love to hear about your project.</p>
    </div>
    <form class="contact-form" id="contact-form" onsubmit="submitForm(event)" novalidate>
      <div class="form-row">
        <div class="form-field">
          <label for="cf-name">Name</label>
          <input type="text" id="cf-name" name="name" placeholder="Your name" required>
        </div>
        <div class="form-field">
          <label for="cf-email">Email</label>
          <input type="email" id="cf-email" name="email" placeholder="your@email.com" required>
        </div>
      </div>
      <div class="form-field">
        <label for="cf-subject">Subject</label>
        <input type="text" id="cf-subject" name="subject" placeholder="Project type or enquiry">
      </div>
      <div class="form-field">
        <label for="cf-message">Message</label>
        <textarea id="cf-message" name="message" rows="5" placeholder="Tell me about your project…" required></textarea>
      </div>
      <div class="form-success" id="form-success">Thank you — I'll be in touch soon.</div>
      <button type="submit" class="form-submit">Send Message →</button>
    </form>
  </section>

  <footer>
    <span>© 2026 Sarah Sawtelle</span>
    <span>Natural History · Science Communication · Environmental Design</span>
  </footer>
</div>

  <script>
    function submitForm(e) {
      e.preventDefault();
      const form = document.getElementById('contact-form');
      const success = document.getElementById('form-success');
      const btn = form.querySelector('.form-submit');
      // Basic validation
      if (!form.checkValidity()) { form.reportValidity(); return; }
      btn.textContent = 'Sending…';
      btn.disabled = true;
      // Opens default mail client with pre-filled fields
      const name    = encodeURIComponent(document.getElementById('cf-name').value);
      const subject = encodeURIComponent(document.getElementById('cf-subject').value || 'Portfolio Enquiry');
      const message = encodeURIComponent('From: ' + document.getElementById('cf-name').value + '\n\n' + document.getElementById('cf-message').value);
      window.location.href = 'mailto:sarah.e.sawtelle@gmail.com?subject=' + subject + '&body=' + message;
      setTimeout(() => {
        success.style.display = 'block';
        form.reset();
        btn.textContent = 'Send Message →';
        btn.disabled = false;
      }, 800);
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

