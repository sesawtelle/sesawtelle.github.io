EDIT 3-30 5:10PM
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
    .sidebar-val { font-size: 12px; color: #1a2e14; line-height: 1.6; }

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
    .project-index { font-family: 'Fraunces', serif; font-size: 1.4rem; font-weight: 300; font-style: italic; color: #a8c898; line-height: 1; padding-top: 0.1rem; }
    .work-tag { font-size: 9px; letter-spacing: 0.14em; text-transform: uppercase; color: #f0ebe0; background: #3a7a30; padding: 0.3rem 0.8rem; white-space: nowrap; display: inline-block; margin-bottom: 0.6rem; }
    .project-org { font-size: 10px; letter-spacing: 0.16em; text-transform: uppercase; color: #4a6640; margin-bottom: 0.3rem; }
    .project-title { font-family: 'Fraunces', serif; font-size: 1.3rem; font-weight: 300; font-style: italic; color: #2a2318; margin-bottom: 0.7rem; }
    .project-desc { font-size: 12px; color: #7a6e5a; line-height: 1.78; max-width: 62ch; }
    /* Instagram grid */
    .project-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 0.6rem; }
    .project-grid-link { display: block; overflow: hidden; aspect-ratio: 1 / 1; }
    .project-grid-link img { width: 100%; height: 100%; object-fit: cover; display: block; transition: transform 0.35s; }
    .project-grid-link:hover img { transform: scale(1.04); }
    /* Instagram profile screenshot */
    .project-desc-row { display: grid; grid-template-columns: 1fr 260px; gap: 2rem; align-items: start; }
    .project-profile-img { width: 100%; display: block; border: 1px solid #c8c0ae; }
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

  <nav>
    <a class="logo" href="#hero">Sarah Sawtelle</a>
    <div class="nav-links">
      <a class="nav-link" href="#skills">Skills</a>
      <a class="nav-link" href="#work">Work</a>
      <a class="nav-link" href="#contact">Contact</a>
    </div>
  </nav>

  <section id="hero">
    <div class="hero-left">
      <p class="hero-kicker">Portfolio — Social Media & Interpretation</p>
      <h1 class="hero-title">Sarah<br>Sawtelle</h1>
      <div class="sidebar-item">
        <div class="sidebar-key">Location</div>
        <div class="sidebar-val">San Francisco, CA</div>
      </div>
      <div class="sidebar-item">
        <div class="sidebar-key">Specialties</div>
        <div class="sidebar-val">Social Media Content Creation & Management<br>Interpretive Sign Creation<br>Educational Program Development<br>Volunteer Management</div>
      </div>
      <div class="sidebar-item">
        <div class="sidebar-key">Available For</div>
        <div class="sidebar-val">Freelance & Contract</div>
      </div>
      <a href="#work" class="hero-btn">View Work →</a>
    </div>
    <div class="hero-right">
      <img class="hero-photo" src="hero.jpg" alt="Interior of the San Francisco Conservatory of Flowers — Giant Victoria water lily pads floating in the tropical pond">
    </div>
  </section>

  <div class="section-bar reveal">
    <span class="section-bar-num">01 —</span>
    <span class="section-bar-title">Skills & Specialisms</span>
  </div>
  <section id="skills" class="reveal">
    <div class="skills-grid">
      <div class="skill-card">
        <div class="skill-glyph">◈</div>
        <div class="skill-name">Social Media</div>
        <div class="skill-desc">Visual storytelling across Instagram, Facebook, YouTube, and more. Original photography, video, design, and writing to share your organization's story.</div>
      </div>
      <div class="skill-card">
        <div class="skill-glyph">◉</div>
        <div class="skill-name">Interpretive Sign Design</div>
        <div class="skill-desc">Educational signs for museums, parks, and gardens.</div>
      </div>
      <div class="skill-card">
        <div class="skill-glyph">◎</div>
        <div class="skill-name">Science Storytelling</div>
        <div class="skill-desc">Translating natural history and ecology into engaging programs for broad audiences.</div>
      </div>
    </div>
  </section>

  <div class="section-bar reveal">
    <span class="section-bar-num">02 —</span>
    <span class="section-bar-title">Selected Work</span>
  </div>
  <section id="work" class="reveal">

    <!-- Project 01: Instagram -->
    <div class="project">
      <div class="project-top">
        <span class="project-index">01</span>
        <div>
          <span class="work-tag">Instagram</span>
          <span class="work-tag" style="background: #2a5c28;">Facebook</span>
          <span class="work-tag" style="background: #5a9a4a;">Youtube</span>
          <div class="project-org">San Francisco Conservatory of Flowers</div>
          <h3 class="project-title">Connecting People & Plants</h3>
          <div class="project-desc-row">
            <div class="project-desc">
              <b>January 2021 – December 2022</b>
              <ul style="margin-top: 0.7rem; padding-left: 1.2em; display: flex; flex-direction: column; gap: 0.5rem;">
                <li>Managed the San Francisco Conservatory of Flowers Instagram for two years while serving as Communications Manager.</li>
                <li>Shared dazzling photos of tropical plants alongside their remarkable botanical backstories.</li>
                <li>Behind-the-scenes reels brought viewers underwater to see the undersides of iconic Giant Water Lilies, and the ephemeral night bloom of a cactus flower.</li>
                <li>Utilized the HootSuite platform to manage a content calendar and cross-posting capabilities.</li>
                <li>Coordinated with events, retail, horticulture and operations teams to share news from across the organization with more than 60,000 followers.</li>
              </ul>
            </div>
            <img class="project-profile-img" src="instagram-profile.jpg" alt="@conservatoryofflowers Instagram profile — 66.8K followers">
          </div>
        </div>
      </div>
      <div class="project-grid">
        <a class="project-grid-link" href="https://www.instagram.com/p/CQuWaavLb33/" target="_blank" rel="noopener">
          <img src="https://images.squarespace-cdn.com/content/v1/68cb081869dddd79cbb02fc0/6c77f3b1-41ea-46dd-ba12-b6807887276d/Screenshot+2025-09-17+at+12.39.24%E2%80%AFPM.png" alt="Bat Flower trivia post — Instagram @ SF Conservatory of Flowers" loading="lazy">
        </a>
        <a class="project-grid-link" href="https://www.instagram.com/p/Chk3u_SDijd/?hl=en" target="_blank" rel="noopener">
          <img src="https://images.squarespace-cdn.com/content/v1/68cb081869dddd79cbb02fc0/1758211017494-FUJ0SUV9HGEZHLXDQ5K7/Screenshot%252B2025-09-18%252Bat%252B8.39.17%2525E2%252580%2525AFAM.png" alt="Instagram post — SF Conservatory of Flowers" loading="lazy">
        </a>
        <a class="project-grid-link" href="https://www.instagram.com/p/CcGPQgtp826/?hl=en&img_index=1" target="_blank" rel="noopener">
          <img src="https://images.squarespace-cdn.com/content/v1/68cb081869dddd79cbb02fc0/1758210426850-WMN5P2XOHETDHEGPMJV1/Screenshot%2B2025-09-18%2Bat%2B8.46.24%25E2%2580%25AFAM.png" alt="Instagram post — SF Conservatory of Flowers" loading="lazy">
        </a>
        <a class="project-grid-link" href="https://www.instagram.com/p/CeEmW9vlS5r/?hl=en" target="_blank" rel="noopener">
          <img src="https://images.squarespace-cdn.com/content/v1/68cb081869dddd79cbb02fc0/1758211246811-XZ6XOYRC3KETKZ0N45LQ/Screenshot%252B2025-09-17%252Bat%252B12.46.15%2525E2%252580%2525AFPM.png" alt="Instagram post — SF Conservatory of Flowers" loading="lazy">
        </a>
        <a class="project-grid-link" href="https://www.instagram.com/p/Ci0N9EjJzFF/?hl=en" target="_blank" rel="noopener">
          <img src="https://images.squarespace-cdn.com/content/v1/68cb081869dddd79cbb02fc0/1758210882585-Q2R8I1TFIB2TPID11L9D/Screenshot%2B2025-09-18%2Bat%2B8.50.25%25E2%2580%25AFAM.png" alt="Instagram post — SF Conservatory of Flowers" loading="lazy">
        </a>
        <a class="project-grid-link" href="https://www.instagram.com/p/CezZZv6jnNj/?hl=en" target="_blank" rel="noopener">
          <img src="https://images.squarespace-cdn.com/content/v1/68cb081869dddd79cbb02fc0/1758210284067-P33HN3L7OHUKGKPLR8MQ/Screenshot%252B2025-09-17%252Bat%252B12.46.41%2525E2%252580%2525AFPM.png" alt="Instagram post — SF Conservatory of Flowers" loading="lazy">
        </a>
      </div>
    </div>

    <!-- Project 02: YouTube -->
    <div class="project">
      <div class="project-top">
        <span class="project-index">02</span>
        <div>
          <span class="work-tag">Video</span>
          <div class="project-org">San Francisco Conservatory of Flowers</div>
          <h3 class="project-title">YouTube Live — Corpse Flower Bloom</h3>
        </div>
      </div>
      <div class="project-layout">
        <p class="project-desc">There is no event that brings more visitors to the garden than a bloom of the Corpse Flower. An impending bloom during a pandemic-era garden closure led me to make a quick pivot towards online programming. I envisioned and produced a series of YouTube Live programs that featured Conservatory staff and volunteers sharing the story of the Corpse Flower — its fascinating natural history and the role of botanical gardens in conservation. The bloom was even pollinated live on camera. An event that would normally bring thousands of visitors through the Conservatory's doors instead reached thousands of viewers across the world.</p>
        <a class="project-img-link" href="https://www.youtube.com/watch?v=ACjMx4KxkaI" target="_blank" rel="noopener">
          <img src="https://images.squarespace-cdn.com/content/v1/68cb081869dddd79cbb02fc0/cec56368-a745-47da-be9a-7c0e766388af/Screenshot+2025-09-18+at+9.13.02%E2%80%AFAM.png" alt="YouTube Live — Corpse Flower Bloom at SF Conservatory of Flowers" loading="lazy">
        </a>
      </div>
    </div>

  </section>

  <div class="section-bar reveal">
    <span class="section-bar-num">03 —</span>
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

