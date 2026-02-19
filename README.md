# https-sampaiorafaelaa.github.io
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Rafaela Almeida Sampaio — 3D Jewelry Designer & AI Specialist</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --gold: #B8964A;
    --gold-light: #D4AF70;
    --gold-pale: #F5EDD6;
    --ink: #1A1714;
    --ink-soft: #3D3530;
    --stone: #F0EBE3;
    --white: #FDFAF6;
    --muted: #8C7B6E;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--white);
    color: var(--ink);
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    display: flex; justify-content: space-between; align-items: center;
    padding: 1.2rem 4rem;
    background: rgba(253,250,246,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid rgba(184,150,74,0.15);
  }
  .nav-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.4rem; font-weight: 300; letter-spacing: 0.15em;
    color: var(--ink); text-decoration: none;
  }
  .nav-logo span { color: var(--gold); }
  .nav-links { display: flex; gap: 2.5rem; list-style: none; }
  .nav-links a {
    font-size: 0.78rem; letter-spacing: 0.12em; text-transform: uppercase;
    color: var(--muted); text-decoration: none; transition: color 0.3s;
  }
  .nav-links a:hover { color: var(--gold); }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    display: grid; grid-template-columns: 1fr 1fr;
    align-items: center;
    padding: 6rem 4rem 4rem;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute; top: -10%; right: -5%;
    width: 55%; height: 110%;
    background: linear-gradient(135deg, var(--gold-pale) 0%, var(--stone) 60%, transparent 100%);
    border-radius: 0 0 0 60%;
    z-index: 0;
  }
  .hero-text { position: relative; z-index: 1; }
  .hero-eyebrow {
    font-size: 0.72rem; letter-spacing: 0.25em; text-transform: uppercase;
    color: var(--gold); margin-bottom: 1.5rem;
    display: flex; align-items: center; gap: 0.8rem;
  }
  .hero-eyebrow::before {
    content: ''; display: block; width: 2.5rem; height: 1px; background: var(--gold);
  }
  .hero h1 {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(3rem, 5vw, 5rem);
    font-weight: 300; line-height: 1.08;
    color: var(--ink); margin-bottom: 0.3rem;
  }
  .hero h1 em {
    font-style: italic; color: var(--gold);
  }
  .hero-title {
    font-size: 0.82rem; letter-spacing: 0.18em; text-transform: uppercase;
    color: var(--muted); margin: 1.2rem 0 2rem;
  }
  .hero-bio {
    font-size: 1rem; line-height: 1.75; color: var(--ink-soft);
    max-width: 480px; margin-bottom: 2.5rem;
  }
  .hero-bio-pt {
    font-size: 0.88rem; line-height: 1.7; color: var(--muted);
    max-width: 480px; margin-bottom: 2.5rem;
    font-style: italic; border-left: 2px solid var(--gold-light); padding-left: 1rem;
  }
  .hero-cta {
    display: flex; gap: 1rem; flex-wrap: wrap;
  }
  .btn-primary {
    padding: 0.85rem 2rem; background: var(--gold);
    color: white; text-decoration: none;
    font-size: 0.78rem; letter-spacing: 0.15em; text-transform: uppercase;
    transition: background 0.3s, transform 0.2s;
  }
  .btn-primary:hover { background: var(--ink); transform: translateY(-2px); }
  .btn-secondary {
    padding: 0.85rem 2rem; border: 1px solid var(--gold);
    color: var(--gold); text-decoration: none;
    font-size: 0.78rem; letter-spacing: 0.15em; text-transform: uppercase;
    transition: all 0.3s;
  }
  .btn-secondary:hover { background: var(--gold); color: white; transform: translateY(-2px); }

  .hero-visual {
    position: relative; z-index: 1;
    display: flex; flex-direction: column; align-items: center; justify-content: center;
  }
  .avatar-ring {
    width: 320px; height: 320px; border-radius: 50%;
    border: 1px solid var(--gold-light);
    display: flex; align-items: center; justify-content: center;
    position: relative;
    animation: rotate-ring 20s linear infinite;
  }
  @keyframes rotate-ring {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
  }
  .avatar-ring::before {
    content: '';
    position: absolute; inset: 8px; border-radius: 50%;
    border: 1px dashed rgba(184,150,74,0.3);
  }
  .avatar-inner {
    width: 260px; height: 260px; border-radius: 50%;
    background: linear-gradient(145deg, var(--gold-pale), var(--stone));
    display: flex; align-items: center; justify-content: center;
    animation: rotate-ring 20s linear reverse infinite;
    font-family: 'Cormorant Garamond', serif;
    font-size: 4rem; font-weight: 300;
    color: var(--gold);
    letter-spacing: -0.02em;
  }
  .hero-stats {
    display: flex; gap: 2rem; margin-top: 2rem;
  }
  .stat { text-align: center; }
  .stat-number {
    font-family: 'Cormorant Garamond', serif;
    font-size: 2rem; font-weight: 300; color: var(--gold); line-height: 1;
  }
  .stat-label {
    font-size: 0.68rem; letter-spacing: 0.15em; text-transform: uppercase; color: var(--muted);
    margin-top: 0.3rem;
  }

  /* ── SECTION BASE ── */
  section { padding: 6rem 4rem; }
  .section-header { margin-bottom: 3.5rem; }
  .section-eyebrow {
    font-size: 0.7rem; letter-spacing: 0.3em; text-transform: uppercase;
    color: var(--gold); margin-bottom: 0.8rem;
  }
  .section-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(2rem, 3vw, 3rem);
    font-weight: 300; color: var(--ink);
  }
  .section-title em { font-style: italic; color: var(--gold); }

  /* ── SKILLS ── */
  .skills-section { background: var(--stone); }
  .skills-grid {
    display: grid; grid-template-columns: repeat(3, 1fr); gap: 2rem;
  }
  .skill-card {
    background: var(--white); padding: 2rem;
    border: 1px solid rgba(184,150,74,0.15);
    transition: transform 0.3s, box-shadow 0.3s, border-color 0.3s;
    position: relative; overflow: hidden;
  }
  .skill-card::after {
    content: '';
    position: absolute; bottom: 0; left: 0;
    width: 0; height: 2px; background: var(--gold);
    transition: width 0.4s ease;
  }
  .skill-card:hover { transform: translateY(-4px); box-shadow: 0 12px 40px rgba(184,150,74,0.12); border-color: rgba(184,150,74,0.4); }
  .skill-card:hover::after { width: 100%; }
  .skill-icon { font-size: 1.8rem; margin-bottom: 1rem; }
  .skill-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.3rem; font-weight: 400; margin-bottom: 0.4rem;
  }
  .skill-desc { font-size: 0.82rem; color: var(--muted); line-height: 1.6; }
  .skill-tags { display: flex; flex-wrap: wrap; gap: 0.4rem; margin-top: 1rem; }
  .tag {
    font-size: 0.65rem; letter-spacing: 0.1em; text-transform: uppercase;
    padding: 0.25rem 0.6rem;
    border: 1px solid rgba(184,150,74,0.4); color: var(--gold);
  }

  /* ── EXPERIENCE ── */
  .experience-section { background: var(--white); }
  .timeline { position: relative; padding-left: 2.5rem; }
  .timeline::before {
    content: '';
    position: absolute; left: 0; top: 0; bottom: 0;
    width: 1px; background: linear-gradient(to bottom, var(--gold), transparent);
  }
  .timeline-item {
    position: relative; padding-bottom: 3rem;
    opacity: 0; transform: translateX(-20px);
    animation: slide-in 0.6s forwards;
  }
  .timeline-item:nth-child(1) { animation-delay: 0.1s; }
  .timeline-item:nth-child(2) { animation-delay: 0.25s; }
  .timeline-item:nth-child(3) { animation-delay: 0.4s; }
  @keyframes slide-in {
    to { opacity: 1; transform: translateX(0); }
  }
  .timeline-dot {
    position: absolute; left: -2.85rem; top: 0.3rem;
    width: 10px; height: 10px; border-radius: 50%;
    border: 2px solid var(--gold); background: var(--white);
  }
  .timeline-date {
    font-size: 0.72rem; letter-spacing: 0.15em; text-transform: uppercase;
    color: var(--gold); margin-bottom: 0.4rem;
  }
  .timeline-role {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.4rem; font-weight: 400; margin-bottom: 0.2rem;
  }
  .timeline-company { font-size: 0.85rem; color: var(--muted); margin-bottom: 0.8rem; }
  .timeline-desc { font-size: 0.9rem; color: var(--ink-soft); line-height: 1.7; max-width: 600px; }

  /* ── PORTFOLIO ── */
  .portfolio-section { background: var(--stone); }
  .portfolio-grid {
    display: grid; grid-template-columns: repeat(2, 1fr); gap: 1.5rem;
  }
  .portfolio-card {
    background: var(--white); overflow: hidden;
    border: 1px solid rgba(184,150,74,0.1);
    transition: transform 0.3s, box-shadow 0.3s;
    cursor: pointer;
  }
  .portfolio-card:hover { transform: translateY(-6px); box-shadow: 0 20px 50px rgba(184,150,74,0.15); }
  .portfolio-thumb {
    height: 200px;
    display: flex; align-items: center; justify-content: center;
    font-size: 3rem;
    position: relative; overflow: hidden;
  }
  .portfolio-thumb.gold-bg { background: linear-gradient(135deg, var(--gold-pale), #EAD9B0); }
  .portfolio-thumb.dark-bg { background: linear-gradient(135deg, var(--ink), var(--ink-soft)); }
  .portfolio-thumb.stone-bg { background: linear-gradient(135deg, var(--stone), #DDD3C3); }
  .portfolio-info { padding: 1.5rem; }
  .portfolio-cat {
    font-size: 0.65rem; letter-spacing: 0.2em; text-transform: uppercase;
    color: var(--gold); margin-bottom: 0.4rem;
  }
  .portfolio-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.25rem; margin-bottom: 0.5rem;
  }
  .portfolio-desc { font-size: 0.8rem; color: var(--muted); line-height: 1.6; }

  /* ── HIGHLIGHT BANNER ── */
  .highlight-banner {
    background: var(--ink); color: var(--white);
    padding: 5rem 4rem;
    display: grid; grid-template-columns: 1fr auto;
    align-items: center; gap: 3rem;
  }
  .highlight-label {
    font-size: 0.7rem; letter-spacing: 0.3em; text-transform: uppercase;
    color: var(--gold); margin-bottom: 1rem;
  }
  .highlight-text {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(1.8rem, 3vw, 2.8rem);
    font-weight: 300; line-height: 1.3;
  }
  .highlight-text em { font-style: italic; color: var(--gold-light); }
  .highlight-sub {
    font-size: 0.85rem; color: rgba(253,250,246,0.6);
    margin-top: 1rem; line-height: 1.7;
  }

  /* ── CONTACT ── */
  .contact-section { background: var(--white); }
  .contact-grid {
    display: grid; grid-template-columns: 1fr 1fr; gap: 5rem; align-items: start;
  }
  .contact-info p {
    font-size: 0.95rem; color: var(--ink-soft); line-height: 1.8;
    margin-bottom: 2rem;
  }
  .contact-links { display: flex; flex-direction: column; gap: 1rem; }
  .contact-link {
    display: flex; align-items: center; gap: 1rem;
    color: var(--ink); text-decoration: none;
    font-size: 0.9rem;
    padding: 1rem 1.2rem;
    border: 1px solid rgba(184,150,74,0.2);
    transition: all 0.3s;
  }
  .contact-link:hover { border-color: var(--gold); color: var(--gold); transform: translateX(6px); }
  .contact-link-icon { font-size: 1.2rem; }
  .contact-form { display: flex; flex-direction: column; gap: 1.2rem; }
  .form-group { display: flex; flex-direction: column; gap: 0.4rem; }
  .form-label { font-size: 0.7rem; letter-spacing: 0.15em; text-transform: uppercase; color: var(--muted); }
  .form-input, .form-textarea {
    padding: 0.9rem 1.1rem;
    border: 1px solid rgba(184,150,74,0.25);
    background: var(--stone); outline: none;
    font-family: 'DM Sans', sans-serif; font-size: 0.9rem;
    transition: border-color 0.3s;
  }
  .form-input:focus, .form-textarea:focus { border-color: var(--gold); }
  .form-textarea { resize: vertical; min-height: 120px; }

  /* ── FOOTER ── */
  footer {
    background: var(--ink); color: rgba(253,250,246,0.5);
    padding: 2rem 4rem;
    display: flex; justify-content: space-between; align-items: center;
    font-size: 0.75rem; letter-spacing: 0.08em;
  }
  footer a { color: var(--gold); text-decoration: none; }

  /* ── LANG TOGGLE ── */
  .lang-toggle {
    display: flex; align-items: center; gap: 0.5rem;
    cursor: pointer;
  }
  .lang-btn {
    padding: 0.3rem 0.7rem; font-size: 0.7rem; letter-spacing: 0.1em;
    text-transform: uppercase; cursor: pointer; border: 1px solid transparent;
    background: none; font-family: 'DM Sans', sans-serif;
    transition: all 0.2s;
  }
  .lang-btn.active { border-color: var(--gold); color: var(--gold); }
  .lang-btn:not(.active) { color: var(--muted); }

  /* ── SCROLL REVEAL ── */
  .reveal { opacity: 0; transform: translateY(30px); transition: opacity 0.7s ease, transform 0.7s ease; }
  .reveal.visible { opacity: 1; transform: translateY(0); }

  /* ── MOBILE ── */
  @media (max-width: 768px) {
    nav { padding: 1rem 1.5rem; }
    .nav-links { display: none; }
    .hero { grid-template-columns: 1fr; padding: 5rem 1.5rem 3rem; text-align: center; }
    .hero::before { display: none; }
    .hero-eyebrow { justify-content: center; }
    .hero-bio, .hero-bio-pt { max-width: 100%; }
    .hero-cta { justify-content: center; }
    .hero-visual { margin-top: 3rem; }
    section { padding: 4rem 1.5rem; }
    .skills-grid, .portfolio-grid { grid-template-columns: 1fr; }
    .contact-grid { grid-template-columns: 1fr; gap: 2.5rem; }
    .highlight-banner { grid-template-columns: 1fr; padding: 3rem 1.5rem; }
    footer { flex-direction: column; gap: 0.5rem; text-align: center; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">R<span>.</span>A. Sampaio</a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#portfolio">Portfolio</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <div class="lang-toggle">
    <button class="lang-btn active" onclick="setLang('en')">EN</button>
    <span style="color:var(--muted);font-size:0.7rem">|</span>
    <button class="lang-btn" onclick="setLang('pt')">PT</button>
  </div>
</nav>

<!-- HERO -->
<section class="hero" id="about">
  <div class="hero-text">
    <p class="hero-eyebrow" data-en="3D Jewelry Modeling · AI & Audiovisual · São Paulo, Brasil" data-pt="Modelagem 3D de Joias · IA & Audiovisual · São Paulo, Brasil">
      3D Jewelry Modeling · AI & Audiovisual · São Paulo, Brasil
    </p>
    <h1>Rafaela<br><em>Almeida Sampaio</em></h1>
    <p class="hero-title" data-en="3D Jewelry Designer & AI Specialist" data-pt="Designer de Modelagem de Joias em 3D & Especialista em IA">
      3D Jewelry Designer & AI Specialist
    </p>
    <p class="hero-bio" data-en="Versatile professional specializing in 3D jewelry modeling, 3D printing and graphic design. I transform ideas into real projects — managing every step from order intake to prototyping, while building the digital presence of brands through visual content and social media. Currently pioneering AI integration within the jewelry industry." data-pt="Profissional versátil especializada em modelagem 3D de joias, impressão 3D e design gráfico. Transformo ideias em projetos reais — gerenciando desde a entrada do pedido até a prototipagem, enquanto fortaleço a presença digital de marcas através de conteúdo visual e redes sociais. Pioneira na integração de IA na indústria joalheira.">
      Versatile professional specializing in 3D jewelry modeling, 3D printing and graphic design. I transform ideas into real projects — managing every step from order intake to prototyping, while building the digital presence of brands through visual content and social media.
    </p>
    <div class="hero-cta">
      <a href="#portfolio" class="btn-primary" data-en="View Portfolio" data-pt="Ver Portfólio">View Portfolio</a>
      <a href="#contact" class="btn-secondary" data-en="Get in Touch" data-pt="Entrar em Contato">Get in Touch</a>
    </div>
  </div>
  <div class="hero-visual">
    <div class="avatar-ring">
      <div class="avatar-inner">RAS</div>
    </div>
    <div class="hero-stats">
      <div class="stat">
        <div class="stat-number">5+</div>
        <div class="stat-label" data-en="Years Experience" data-pt="Anos de Exp.">Years Experience</div>
      </div>
      <div class="stat">
        <div class="stat-number">∞</div>
        <div class="stat-label" data-en="AI Curiosity" data-pt="Curiosidade com IA">AI Curiosity</div>
      </div>
      <div class="stat">
        <div class="stat-number">2</div>
        <div class="stat-label" data-en="Worlds United" data-pt="Mundos Unidos">Worlds United</div>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section class="skills-section" id="skills">
  <div class="section-header reveal">
    <p class="section-eyebrow" data-en="Expertise" data-pt="Especialidades">Expertise</p>
    <h2 class="section-title" data-en="Skills & <em>Capabilities</em>" data-pt="Habilidades & <em>Competências</em>">Skills & <em>Capabilities</em></h2>
  </div>
  <div class="skills-grid">
    <div class="skill-card reveal">
      <div class="skill-icon">💎</div>
      <div class="skill-name" data-en="3D Jewelry Modeling" data-pt="Modelagem 3D de Joias">3D Jewelry Modeling</div>
      <div class="skill-desc" data-en="Full-cycle jewelry modeling — from organic free forms to classic designs. Complete project management from order intake to prototyping and 3D printing." data-pt="Modelagem de joias de ponta a ponta — de formas orgânicas a designs clássicos. Gestão completa do projeto desde a entrada do pedido até a prototipagem e impressão 3D.">
        Full-cycle jewelry modeling — from organic free forms to classic designs. Complete project management from order intake to prototyping and 3D printing.
      </div>
      <div class="skill-tags">
        <span class="tag">3D Modeling</span>
        <span class="tag">3D Printing</span>
        <span class="tag">Prototyping</span>
      </div>
    </div>
    <div class="skill-card reveal">
      <div class="skill-icon">🤖</div>
      <div class="skill-name" data-en="AI for Jewelry" data-pt="IA para Joalheria">AI for Jewelry</div>
      <div class="skill-desc" data-en="Pioneer in applying AI tools to the jewelry industry — from generative design to workflow automation and visual production. Future instructor of AI for Jewelry course." data-pt="Pioneira na aplicação de ferramentas de IA na indústria joalheira — do design generativo à automação de processos. Futura instrutora do curso IA para Joalheria.">
        Pioneer in applying AI tools to the jewelry industry — from generative design to workflow automation and visual production.
      </div>
      <div class="skill-tags">
        <span class="tag">Generative AI</span>
        <span class="tag">AI Automation</span>
        <span class="tag">Innovation</span>
      </div>
    </div>
    <div class="skill-card reveal">
      <div class="skill-icon">🎬</div>
      <div class="skill-name" data-en="AI Audiovisual & Graphic Design" data-pt="Audiovisual com IA & Design Gráfico">AI Audiovisual & Graphic Design</div>
      <div class="skill-desc" data-en="Managing Instagram and creating visual content that strengthens brands' digital presence. Applying AI tools to elevate visual production in the jewelry industry." data-pt="Gerenciando Instagram e criando conteúdos visuais que fortalecem a presença digital de marcas. Aplicando ferramentas de IA para elevar a produção visual na joalheria.">
        Managing Instagram and creating visual content that strengthens brands' digital presence. Applying AI tools to elevate visual production.
      </div>
      <div class="skill-tags">
        <span class="tag">Graphic Design</span>
        <span class="tag">Social Media</span>
        <span class="tag">AI Video</span>
      </div>
    </div>
    <div class="skill-card reveal">
      <div class="skill-icon">📐</div>
      <div class="skill-name" data-en="Project Management" data-pt="Gestão de Projetos">Project Management</div>
      <div class="skill-desc" data-en="End-to-end client management — from briefing to delivery. Handling deadlines, challenges and stakeholder communication to deliver unique and meaningful pieces." data-pt="Gestão completa de clientes — do briefing à entrega. Administrando prazos, desafios e comunicação para entregar peças únicas e significativas.">
        End-to-end client management — from briefing to delivery. Handling deadlines, challenges and communication to deliver unique and meaningful pieces.
      </div>
      <div class="skill-tags">
        <span class="tag">Client Management</span>
        <span class="tag">Design Briefs</span>
      </div>
    </div>
    <div class="skill-card reveal">
      <div class="skill-icon">🧠</div>
      <div class="skill-name" data-en="AI Productivity Tools" data-pt="Ferramentas de IA para Produtividade">AI Productivity Tools</div>
      <div class="skill-desc" data-en="Deep exploration and practical application of AI tools for creative workflows, content creation and business efficiency. Constantly evolving to stay at the forefront of technology." data-pt="Exploração e aplicação prática de ferramentas de IA para fluxos criativos, criação de conteúdo e eficiência nos negócios. Em constante evolução para estar na vanguarda da tecnologia.">
        Deep exploration and practical application of AI tools for creative workflows, content creation and business efficiency.
      </div>
      <div class="skill-tags">
        <span class="tag">ChatGPT</span>
        <span class="tag">Claude</span>
        <span class="tag">Midjourney</span>
      </div>
    </div>
    <div class="skill-card reveal">
      <div class="skill-icon">🌍</div>
      <div class="skill-name" data-en="English — Advanced" data-pt="Inglês — Nível Avançado">English — Advanced</div>
      <div class="skill-desc" data-en="Advanced English proficiency, enabling collaboration with international teams, global clients and access to the latest global references in design and AI." data-pt="Inglês nível avançado, permitindo colaboração com equipes internacionais, clientes globais e acesso às mais recentes referências mundiais em design e IA.">
        Advanced English proficiency, enabling collaboration with international teams, global clients and access to the latest global references in design and AI.
      </div>
      <div class="skill-tags">
        <span class="tag">International</span>
        <span class="tag">Global Ready</span>
      </div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section class="experience-section" id="experience">
  <div class="section-header reveal">
    <p class="section-eyebrow" data-en="Career" data-pt="Carreira">Career</p>
    <h2 class="section-title" data-en="Professional <em>Journey</em>" data-pt="Trajetória <em>Profissional</em>">Professional <em>Journey</em></h2>
  </div>
  <div class="timeline">
    <div class="timeline-item">
      <div class="timeline-dot"></div>
      <p class="timeline-date" data-en="Current · Solução 3D Treinamentos e Serviços" data-pt="Atual · Solução 3D Treinamentos e Serviços">Current · Solução 3D Treinamentos e Serviços</p>
      <h3 class="timeline-role" data-en="3D Jewelry Designer & Graphic Design" data-pt="Designer de Modelagem de Joias em 3D & Design Gráfico">3D Jewelry Designer & Graphic Design</h3>
      <p class="timeline-company">Solução 3D Treinamentos e Serviços · São Paulo, Brasil</p>
      <p class="timeline-desc" data-en="Managing clients from order intake through to invoice and prototyping. Responsible for the company's graphic design, Instagram management and creation of visual content that strengthens the brand's digital presence. Developing the company's AI for Jewelry course — to be launched as an official training product." data-pt="Gerencio clientes de forma completa, desde a entrada do pedido até a finalização da nota e prototipagem. Responsável pelo design gráfico da empresa, gerenciamento do Instagram e criação de conteúdos visuais que fortalecem a presença digital da marca. Desenvolvendo o curso IA para Joalheria da empresa — a ser lançado como produto oficial de treinamento.">
        Managing clients from order intake through to invoice and prototyping. Responsible for the company's graphic design, Instagram management and creation of visual content that strengthens the brand's digital presence. Developing the company's AI for Jewelry course — to be launched as an official training product.
      </p>
    </div>
    <div class="timeline-item">
      <div class="timeline-dot"></div>
      <p class="timeline-date" data-en="Ongoing · Self-directed Research" data-pt="Contínuo · Pesquisa Independente">Ongoing · Self-directed Research</p>
      <h3 class="timeline-role" data-en="AI Tools for Jewelry & Audiovisual" data-pt="Ferramentas de IA para Joalheria & Audiovisual">AI Tools for Jewelry & Audiovisual</h3>
      <p class="timeline-company" data-en="Independent · Continuous Learning" data-pt="Independente · Aprendizado Contínuo">Independent · Continuous Learning</p>
      <p class="timeline-desc" data-en="Deep exploration of AI tools applied to the jewelry sector and audiovisual production. Studying with 'A Joia 3D Perfeita' course, instructed by Eliania Rosetti, to elevate technical skills. Passionate about technology and design as the future of jewelry." data-pt="Exploração profunda de ferramentas de IA aplicadas ao setor joalheiro e produção audiovisual. Aprimorando habilidades com o curso 'A Joia 3D Perfeita', ministrado por Eliania Rosetti. Apaixonada por tecnologia e design como o futuro da joalheria.">
        Deep exploration of AI tools applied to the jewelry sector and audiovisual production. Currently taking 'A Joia 3D Perfeita' course by Eliania Rosetti to elevate technical skills.
      </p>
    </div>
    <div class="timeline-item">
      <div class="timeline-dot"></div>
      <p class="timeline-date" data-en="Aug – Nov 2021 · Academic Project" data-pt="Ago – Nov 2021 · Projeto Acadêmico">Aug – Nov 2021 · Academic Project</p>
      <h3 class="timeline-role" data-en="Design Experimental — Retail of the Future Challenge" data-pt="Design Experimental — Desafio Varejo do Futuro">Design Experimental — Retail of the Future Challenge</h3>
      <p class="timeline-company">IMT – Mauá · Instituto Mauá de Tecnologia</p>
      <p class="timeline-desc" data-en="Team project mentored by Professor José Carlos. Collaborated with Laura Sirino and Marina Morillo on experimental design research for the future of retail. Developed skills in design briefs and creative teamwork." data-pt="Projeto em equipe mentorado pelo Professor José Carlos. Colaboração com Laura Sirino e Marina Morillo em pesquisa de design experimental para o futuro do varejo. Desenvolveu habilidades em design briefs e trabalho em equipe criativo.">
        Team project mentored by Professor José Carlos. Collaborated with Laura Sirino and Marina Morillo on experimental design research for the future of retail. Developed design briefs and creative teamwork skills.
      </p>
    </div>
    <div class="timeline-item">
      <div class="timeline-dot"></div>
      <p class="timeline-date" data-en="Academic Training · IMT Mauá" data-pt="Formação Acadêmica · IMT Mauá">Academic Training · IMT Mauá</p>
      <h3 class="timeline-role" data-en="Design — Instituto Mauá de Tecnologia" data-pt="Design — Instituto Mauá de Tecnologia">Design — Instituto Mauá de Tecnologia</h3>
      <p class="timeline-company">IMT – Mauá · Instituto Mauá de Tecnologia · São Paulo, Brasil</p>
      <p class="timeline-desc" data-en="Formal design education including Creativity for Engineers, Designers and Administrators (PM4002) and Experimental Design courses. Built a strong multidisciplinary foundation connecting technology and creative design." data-pt="Formação em design incluindo Criatividade para Engenheiros, Designers e Administradores (PM4002) e cursos de Design Experimental. Construiu uma base multidisciplinar conectando tecnologia e design criativo.">
        Formal design education including Creativity for Engineers, Designers and Administrators. Built a strong multidisciplinary foundation connecting technology and creative design.
      </p>
    </div>
  </div>
</section>

<!-- PORTFOLIO -->
<section class="portfolio-section" id="portfolio">
  <div class="section-header reveal">
    <p class="section-eyebrow" data-en="Work" data-pt="Trabalhos">Work</p>
    <h2 class="section-title" data-en="Selected <em>Projects</em>" data-pt="Projetos <em>Selecionados</em>">Selected <em>Projects</em></h2>
  </div>
  <div class="portfolio-grid">
    <div class="portfolio-card reveal">
      <div class="portfolio-thumb gold-bg">💍</div>
      <div class="portfolio-info">
        <p class="portfolio-cat" data-en="3D Jewelry Modeling" data-pt="Modelagem 3D de Joias">3D Jewelry Modeling</p>
        <h3 class="portfolio-name" data-en="Organic & Classic Jewelry Pieces" data-pt="Peças Orgânicas & Clássicas">Organic & Classic Jewelry Pieces</h3>
        <p class="portfolio-desc" data-en="Full cycle modeling of diverse jewelry pieces — from free-form organic shapes to timeless classic designs. From concept to 3D-ready files for prototyping and production at Solução 3D." data-pt="Modelagem de ciclo completo de diversas peças de joias — de formas orgânicas livres a designs clássicos atemporais. Do conceito a arquivos 3D prontos para prototipagem e produção na Solução 3D.">
          Full cycle modeling of diverse jewelry pieces — from free-form organic shapes to timeless classic designs, ready for 3D printing and production.
        </p>
      </div>
    </div>
    <div class="portfolio-card reveal">
      <div class="portfolio-thumb dark-bg">✨</div>
      <div class="portfolio-info">
        <p class="portfolio-cat" data-en="AI Audiovisual & Brand Content" data-pt="Audiovisual com IA & Conteúdo de Marca">AI Audiovisual & Brand Content</p>
        <h3 class="portfolio-name" data-en="Digital Presence — Solução 3D" data-pt="Presença Digital — Solução 3D">Digital Presence — Solução 3D</h3>
        <p class="portfolio-desc" data-en="Creation and management of visual content for Instagram and social media, strengthening Solução 3D's digital brand. Applying AI tools to elevate the quality of visual productions for the jewelry sector." data-pt="Criação e gestão de conteúdo visual para Instagram e redes sociais, fortalecendo a marca digital da Solução 3D. Aplicando ferramentas de IA para elevar a qualidade das produções visuais para o setor joalheiro.">
          Creation and management of visual content for Instagram and social media, strengthening Solução 3D's digital brand using AI tools.
        </p>
      </div>
    </div>
    <div class="portfolio-card reveal">
      <div class="portfolio-thumb stone-bg">🏆</div>
      <div class="portfolio-info">
        <p class="portfolio-cat" data-en="Academic Project · IMT Mauá" data-pt="Projeto Acadêmico · IMT Mauá">Academic Project · IMT Mauá</p>
        <h3 class="portfolio-name" data-en="Retail of the Future Challenge" data-pt="Desafio Varejo do Futuro">Retail of the Future Challenge</h3>
        <p class="portfolio-desc" data-en="Experimental design team project at IMT – Mauá (Aug–Nov 2021). Mentored by Professor José Carlos, in collaboration with Laura Sirino and Marina Morillo. Focused on the future of retail through the lens of experimental design." data-pt="Projeto de design experimental em equipe no IMT – Mauá (Ago–Nov 2021). Mentorado pelo Professor José Carlos, em colaboração com Laura Sirino e Marina Morillo. Focado no futuro do varejo através do design experimental.">
          Experimental design team project at IMT – Mauá. Exploring the future of retail through design thinking and creative research, mentored by Professor José Carlos.
        </p>
      </div>
    </div>
    <div class="portfolio-card reveal">
      <div class="portfolio-thumb gold-bg" style="background: linear-gradient(135deg,#1A1714,#3D3530);">🎓</div>
      <div class="portfolio-info">
        <p class="portfolio-cat" data-en="Course · Coming Soon" data-pt="Curso · Em Breve">Course · Coming Soon</p>
        <h3 class="portfolio-name" data-en="AI for Jewelry — Course" data-pt="IA para Joalheria — Curso">AI for Jewelry — Course</h3>
        <p class="portfolio-desc" data-en="A comprehensive course on applying Artificial Intelligence in the jewelry industry. Instructor: Rafaela Almeida Sampaio, in partnership with Solução 3D. Covering generative AI, audiovisual production and workflow automation for jewelry professionals." data-pt="Um curso abrangente sobre aplicação de Inteligência Artificial na indústria joalheira. Instrutora: Rafaela Almeida Sampaio, em parceria com a Solução 3D. Abordando IA generativa, produção audiovisual e automação de fluxo de trabalho para profissionais da joalheria.">
          A comprehensive course on applying AI in the jewelry industry. Instructor: Rafaela Almeida Sampaio, in partnership with Solução 3D.
        </p>
      </div>
    </div>
  </div>
</section>

<!-- BANNER -->
<div class="highlight-banner reveal">
  <div>
    <p class="highlight-label" data-en="What I bring to the table" data-pt="O que eu trago">What I bring to the table</p>
    <h2 class="highlight-text" data-en="Jewelry expertise meets <em>AI innovation</em> — a rare combination ready for global opportunities." data-pt="Expertise em joias encontra <em>inovação com IA</em> — uma combinação rara pronta para oportunidades globais.">
      Jewelry expertise meets <em>AI innovation</em> — a rare combination ready for global opportunities.
    </h2>
    <p class="highlight-sub" data-en="Open to international collaborations, consulting projects and leadership roles in innovative companies." data-pt="Aberta a colaborações internacionais, projetos de consultoria e posições de liderança em empresas inovadoras.">
      Open to international collaborations, consulting projects and leadership roles in innovative companies.
    </p>
  </div>
  <a href="#contact" class="btn-primary" style="white-space:nowrap" data-en="Let's Talk" data-pt="Vamos Conversar">Let's Talk</a>
</div>

<!-- CONTACT -->
<section class="contact-section" id="contact">
  <div class="section-header reveal">
    <p class="section-eyebrow" data-en="Contact" data-pt="Contato">Contact</p>
    <h2 class="section-title" data-en="Let's <em>Connect</em>" data-pt="Vamos <em>Conectar</em>">Let's <em>Connect</em></h2>
  </div>
  <div class="contact-grid">
    <div class="contact-info reveal">
      <p data-en="Whether you're looking for a 3D jewelry design specialist, an AI innovator for your team, or a creative collaborator for global projects — I'd love to hear from you. Versatile, driven and ready for international opportunities." data-pt="Se você busca uma especialista em modelagem 3D de joias, uma inovadora em IA para sua equipe, ou uma colaboradora criativa para projetos globais — adoraria conversar. Versátil, determinada e pronta para oportunidades internacionais.">
        Whether you're looking for a 3D jewelry design specialist, an AI innovator for your team, or a creative collaborator for global projects — I'd love to hear from you. Versatile, driven and ready for international opportunities.
      </p>
      <div class="contact-links">
        <a href="https://www.linkedin.com/in/rafaelasampaior/" target="_blank" class="contact-link">
          <span class="contact-link-icon">💼</span>
          <span>LinkedIn — rafaelasampaior</span>
        </a>
        <a href="mailto:contato@rafaelasampaio.com" class="contact-link">
          <span class="contact-link-icon">✉️</span>
          <span data-en="Send an email" data-pt="Enviar e-mail">Send an email</span>
        </a>
        <a href="#" class="contact-link">
          <span class="contact-link-icon">🌐</span>
          <span data-en="Available worldwide · Remote" data-pt="Disponível mundialmente · Remoto">Available worldwide · Remote</span>
        </a>
      </div>
    </div>
    <div class="reveal">
      <form class="contact-form" onsubmit="handleForm(event)">
        <div class="form-group">
          <label class="form-label" data-en="Your Name" data-pt="Seu Nome">Your Name</label>
          <input type="text" class="form-input" required placeholder="—">
        </div>
        <div class="form-group">
          <label class="form-label" data-en="Email" data-pt="E-mail">Email</label>
          <input type="email" class="form-input" required placeholder="—">
        </div>
        <div class="form-group">
          <label class="form-label" data-en="Message" data-pt="Mensagem">Message</label>
          <textarea class="form-textarea" required placeholder="—"></textarea>
        </div>
        <button type="submit" class="btn-primary" data-en="Send Message" data-pt="Enviar Mensagem">Send Message</button>
      </form>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <span>© 2025 Rafaela Almeida Sampaio — 3D Jewelry Designer & AI Specialist</span>
  <span data-en="Made with precision & vision" data-pt="Feito com precisão & visão">Made with precision & vision</span>
</footer>

<script>
  // LANG TOGGLE
  let currentLang = 'en';
  function setLang(lang) {
    currentLang = lang;
    document.querySelectorAll('.lang-btn').forEach(b => b.classList.remove('active'));
    document.querySelector(`.lang-btn:${lang === 'en' ? 'first' : 'last'}-child`).classList.add('active');
    document.querySelectorAll('[data-en]').forEach(el => {
      const text = el.getAttribute(`data-${lang}`);
      if (text) el.innerHTML = text;
    });
  }

  // SCROLL REVEAL
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
  }, { threshold: 0.12 });
  document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

  // FORM
  function handleForm(e) {
    e.preventDefault();
    const btn = e.target.querySelector('button');
    btn.textContent = currentLang === 'en' ? '✓ Sent!' : '✓ Enviado!';
    btn.style.background = '#2A6041';
    setTimeout(() => {
      btn.textContent = currentLang === 'en' ? 'Send Message' : 'Enviar Mensagem';
      btn.style.background = '';
      e.target.reset();
    }, 3000);
  }
</script>
</body>
</html>
