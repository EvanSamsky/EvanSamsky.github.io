---
title: "Home"
markup: "html"
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,600;0,700;1,400&family=Source+Serif+4:wght@300;400;600;700&display=swap');

  :root {
    --home-ink: #244041;
    --home-paper: #f5efe6;
    --home-aged: #d9d8c7;
    --home-rust: #7b463a;
    --home-gold: #d2a75f;
    --home-sage: #5f7f69;
    --home-muted: #6f7d74;
    --home-border: #c8bda9;
    --home-panel: #1f3439;
    --home-blush: #ead6c7;
  }

  .home-report {
    font-family: 'Source Serif 4', Georgia, serif;
    color: var(--home-ink);
    font-size: 17px;
    line-height: 1.75;
    margin: -2rem -1rem 0;
  }

  .home-report p {
    color: var(--home-ink);
    margin-bottom: 1rem;
  }

  .home-report section {
    margin-bottom: 4rem;
  }

  .home-report h2 {
    font-family: 'Playfair Display', Georgia, serif;
    font-size: 1.85rem;
    font-weight: 700;
    color: var(--home-ink);
    margin-bottom: 0.45rem;
    padding-bottom: 0.55rem;
    border-bottom: 2px solid var(--home-gold);
  }

  .home-report h3 {
    font-family: 'Playfair Display', Georgia, serif;
    font-size: 1.18rem;
    font-weight: 400;
    font-style: italic;
    color: var(--home-rust);
    margin: 1.4rem 0 0.7rem;
  }

  .home-masthead {
    background:
      linear-gradient(135deg, rgba(31, 52, 57, 0.96), rgba(46, 73, 66, 0.94) 60%, rgba(123, 70, 58, 0.9)),
      var(--home-panel);
    color: var(--home-paper);
    padding: 3.2rem 2rem 2.6rem;
    position: relative;
    overflow: hidden;
    margin: 0 -2rem;
  }

  .home-masthead::before {
    content: '';
    position: absolute;
    inset: 0;
    background: repeating-linear-gradient(
      45deg,
      transparent,
      transparent 42px,
      rgba(210, 167, 95, 0.06) 42px,
      rgba(210, 167, 95, 0.06) 43px
    );
  }

  .home-masthead::after {
    content: '';
    position: absolute;
    left: 2rem;
    right: 2rem;
    top: 1.2rem;
    height: 8px;
    border-radius: 999px;
    background: linear-gradient(90deg, #244041 0%, #5f7f69 30%, #d2a75f 64%, #7b463a 100%);
    box-shadow: 0 2px 12px rgba(0, 0, 0, 0.18);
  }

  .home-masthead-inner {
    position: relative;
    max-width: 860px;
    margin: 0 auto;
    text-align: center;
  }

  .home-masthead-top,
  .home-masthead-sub {
    font-family: 'Source Serif 4', serif;
    font-weight: 700;
    font-size: 0.82rem;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: #fff2d6;
    text-shadow: 0 1px 2px rgba(11, 18, 22, 0.28);
  }

  .home-masthead-rule {
    width: 72px;
    height: 2px;
    background: var(--home-gold);
    margin: 1rem auto 1.1rem;
  }

  .home-masthead h1 {
    font-family: 'Playfair Display', Georgia, serif;
    font-size: clamp(2rem, 4.8vw, 3.25rem);
    font-weight: 700;
    line-height: 1.12;
    letter-spacing: -0.02em;
    margin: 0 auto 0.85rem;
    max-width: 860px;
    color: var(--home-paper);
  }

  .home-amp {
    display: inline-block;
    margin: 0 0.08em;
    color: var(--home-gold);
    font-style: italic;
    font-size: 1.2em;
    line-height: 0.8;
    text-shadow: 0 2px 0 rgba(36, 64, 65, 0.35);
  }

  .home-masthead .subtitle {
    max-width: 720px;
    margin: 0.9rem auto 0;
    font-size: 1rem;
    color: rgba(245, 239, 230, 0.94);
  }

  .home-jump {
    background: var(--home-aged);
    border-bottom: 1px solid var(--home-border);
    padding: 0.75rem 1.5rem;
    display: flex;
    gap: 0.6rem 1.5rem;
    flex-wrap: wrap;
    justify-content: center;
    margin: 0 -2rem;
  }

  .home-jump a {
    font-size: 0.78rem;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--home-rust);
    text-decoration: none;
    font-family: 'Source Serif 4', serif;
    font-weight: 700;
  }

  .home-jump a:hover {
    color: var(--home-ink);
  }

  .home-container {
    max-width: 860px;
    margin: 0 auto;
    padding: 3rem 0 1rem;
  }

  .home-label {
    display: block;
    margin-bottom: 0.55rem;
    font-size: 0.72rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--home-muted);
    font-family: 'Source Serif 4', serif;
    font-weight: 700;
  }

  .home-callout {
    border-left: 3px solid var(--home-rust);
    background: rgba(234, 214, 199, 0.45);
    padding: 1rem 1.2rem;
    margin: 1.5rem 0;
    font-size: 0.95rem;
    color: var(--home-ink);
  }

  .home-callout strong {
    color: var(--home-rust);
  }

  .home-stat-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 1rem;
    margin: 1.6rem 0;
  }

  .home-stat-card {
    background: var(--home-aged);
    border: 1px solid var(--home-border);
    border-top: 3px solid var(--home-gold);
    padding: 1rem 1.15rem;
  }

  .home-stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 2rem;
    color: var(--home-rust);
    line-height: 1;
    margin-bottom: 0.35rem;
  }

  .home-stat-label {
    font-size: 0.8rem;
    font-weight: 700;
    letter-spacing: 0.05em;
    text-transform: uppercase;
    color: var(--home-ink);
  }

  .home-stat-desc {
    font-size: 0.82rem;
    color: var(--home-muted);
    margin-top: 0.4rem;
  }

  .home-two-col {
    display: grid;
    grid-template-columns: minmax(0, 1.4fr) minmax(250px, 0.9fr);
    gap: 1.5rem;
    align-items: start;
  }

  .home-note {
    background: #f3eee4;
    border: 1px solid var(--home-border);
    padding: 1.1rem 1.2rem;
    margin-bottom: 1rem;
  }

  .home-note h3 {
    margin-top: 0;
  }

  .home-note ul {
    margin: 0.5rem 0 0 1.1rem;
    padding: 0;
  }

  .home-note li {
    margin-bottom: 0.45rem;
  }

  .home-theme-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 1rem;
    margin-top: 1.5rem;
  }

  .home-theme-card {
    background: #f6f0e6;
    border: 1px solid var(--home-border);
    padding: 1.15rem 1.2rem;
    border-top: 3px solid var(--home-sage);
  }

  .home-theme-card .theme-num {
    font-family: 'Playfair Display', serif;
    font-size: 1.5rem;
    color: var(--home-rust);
  }

  .home-theme-card h3 {
    margin-top: 0.55rem;
  }

  .home-theme-card p:last-child {
    margin-bottom: 0;
  }

  .home-timeline {
    list-style: none;
    padding: 0;
    margin: 1.2rem 0 0;
  }

  .home-timeline li {
    display: grid;
    grid-template-columns: 110px minmax(0, 1fr);
    gap: 1rem;
    padding: 1rem 0;
    border-bottom: 1px solid var(--home-border);
  }

  .home-timeline li:last-child {
    border-bottom: none;
  }

  .home-timeline-year {
    font-size: 0.82rem;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--home-muted);
    font-family: 'Source Serif 4', serif;
    font-weight: 700;
  }

  .home-timeline-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    color: var(--home-ink);
    margin-bottom: 0.25rem;
  }

  .home-footer-panel {
    background: var(--home-panel);
    color: rgba(245, 239, 230, 0.86);
    padding: 2rem;
    margin-top: 2.75rem;
  }

  .home-footer-panel h2 {
    color: var(--home-paper);
    border-bottom-color: var(--home-gold);
  }

  .home-footer-panel p,
  .home-footer-panel a {
    color: rgba(245, 239, 230, 0.86);
  }

  .home-links {
    display: flex;
    flex-wrap: wrap;
    gap: 0.8rem;
    margin-top: 1.2rem;
  }

  .home-links a {
    display: inline-block;
    padding: 0.55rem 0.95rem;
    border: 1px solid rgba(245, 239, 230, 0.18);
    text-decoration: none;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    font-size: 0.75rem;
    font-weight: 700;
  }

  .home-links a:hover {
    background: rgba(245, 239, 230, 0.08);
  }

  @media (max-width: 760px) {
    .home-report {
      margin: -1.5rem 0 0;
    }

    .home-masthead,
    .home-jump {
      margin-left: -1rem;
      margin-right: -1rem;
    }

    .home-two-col {
      grid-template-columns: 1fr;
    }

    .home-timeline li {
      grid-template-columns: 1fr;
      gap: 0.35rem;
    }
  }
</style>

<div class="home-report">
  <header class="home-masthead">
    <div class="home-masthead-inner">
      <p class="home-masthead-top">Research portfolio · Evan Samsky</p>
      <div class="home-masthead-rule"></div>
      <h1>Food systems <span class="home-amp">&amp;</span> institutional capacity in Eastern Europe</h1>
      <div class="home-masthead-rule"></div>
      <p class="home-masthead-sub">Agricultural policy · Political economy · Ukraine, Czechia, and the post-Soviet region</p>
      <p class="subtitle">Graduate research on resilience, state capacity, and the institutions that shape food security under pressure.</p>
    </div>
  </header>

  <nav class="home-jump">
    <a href="#overview">Overview</a>
    <a href="#research">Research</a>
    <a href="#themes">Themes</a>
    <a href="#trajectory">Trajectory</a>
    <a href="#contact">Contact</a>
  </nav>

  <div class="home-container">
    <section id="overview">
      <span class="home-label">Overview</span>
      <h2>Research anchored in agriculture, welfare, and political transition</h2>
      <p>I am a dual MA candidate in Global Policy Studies and Russian, East European, and Eurasian Studies at The University of Texas at Austin. My work focuses on how agricultural systems, state institutions, and social welfare structures shape resilience across Eastern Europe and the post-Soviet space.</p>
      <p>Across my projects, I study how climate stress, conflict, and political transition affect the governance of food systems. I am especially interested in the institutional side of adaptation: the administrative capacity, policy incentives, and historical legacies that determine whether reform can take hold.</p>

      <div class="home-callout">
        <strong>Current direction:</strong> building a research agenda around food security, agricultural governance, and institutional capacity in Ukraine and neighboring contexts, with thesis fieldwork preparation focused on Czechia.
      </div>

      <div class="home-stat-grid">
        <div class="home-stat-card">
          <div class="home-stat-num">5</div>
          <div class="home-stat-label">Fieldwork settings</div>
          <div class="home-stat-desc">Ukraine, Morocco, Estonia, Moldova, and Kyrgyzstan inform the comparative lens behind the research.</div>
        </div>
        <div class="home-stat-card">
          <div class="home-stat-num">4+</div>
          <div class="home-stat-label">Working languages</div>
          <div class="home-stat-desc">Russian and Arabic at advanced level, Ukrainian at intermediate level, and Czech in active study.</div>
        </div>
        <div class="home-stat-card">
          <div class="home-stat-num">2025</div>
          <div class="home-stat-label">Current fellowship cycle</div>
          <div class="home-stat-desc">Summer Excellence Fellowship and FLAS-supported language training tied directly to research development.</div>
        </div>
      </div>
    </section>

    <section id="research">
      <span class="home-label">Research profile</span>
      <h2>Studying how institutions condition resilience in everyday systems</h2>
      <div class="home-two-col">
        <div>
          <p>My graduate research examines food security and agricultural resilience in Eastern Europe, with particular attention to Ukraine and the wider post-Soviet region. I am interested in what happens when essential sectors like agriculture must adapt under simultaneous environmental, economic, and political strain.</p>
          <p>Before graduate school, I completed dual bachelor's degrees in Biology and Middle Eastern Language and Culture at UT Austin. My undergraduate thesis traced the Soviet <em>stolovaya</em> cafeteria system as a form of public food aid, which set the foundation for my ongoing interest in the institutional life of food.</p>
          <p>Together, that background has pushed my work toward questions that are both historical and policy-oriented: how states provision, how infrastructures persist, and how institutions are reworked under stress.</p>
        </div>
        <div>
          <div class="home-note">
            <span class="home-label">Current emphasis</span>
            <h3>Institutional capacity under pressure</h3>
            <p>Current projects ask how agricultural governance systems respond to conflict, climate risk, and uneven development, and what those responses reveal about state capacity.</p>
          </div>
          <div class="home-note">
            <span class="home-label">Languages and fieldwork</span>
            <ul>
              <li>Russian and Arabic: advanced</li>
              <li>Ukrainian: intermediate</li>
              <li>Czech: active study</li>
              <li>Fieldwork and lived experience across five countries</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section id="themes">
      <span class="home-label">Research themes</span>
      <h2>Three threads organize the work</h2>
      <div class="home-theme-grid">
        <div class="home-theme-card">
          <div class="theme-num">01</div>
          <h3>Food systems and agricultural policy</h3>
          <p>Examining how land use, production systems, and policy incentives shape food access, export dependence, and rural resilience.</p>
        </div>
        <div class="home-theme-card">
          <div class="theme-num">02</div>
          <h3>Post-Soviet transitions and welfare institutions</h3>
          <p>Tracing what continuity, reform, and institutional drift look like after socialism, especially in sectors tied to everyday material life.</p>
        </div>
        <div class="home-theme-card">
          <div class="theme-num">03</div>
          <h3>Climate adaptation and political economy</h3>
          <p>Studying how environmental stress interacts with governance capacity, reconstruction, and competing development models.</p>
        </div>
      </div>
    </section>

    <section id="trajectory">
      <span class="home-label">Trajectory</span>
      <h2>Recent training, fellowship support, and momentum</h2>
      <ul class="home-timeline">
        <li>
          <div class="home-timeline-year">2025</div>
          <div>
            <div class="home-timeline-title">UT Austin Graduate School Summer Excellence Fellowship</div>
            <p>Support for focused summer research and project development.</p>
          </div>
        </li>
        <li>
          <div class="home-timeline-year">2025</div>
          <div>
            <div class="home-timeline-title">FLAS Fellow, Czech Language, Indiana University</div>
            <p>Intensive language study tied to planned thesis fieldwork in Czechia.</p>
          </div>
        </li>
        <li>
          <div class="home-timeline-year">2024–25</div>
          <div>
            <div class="home-timeline-title">FLAS Fellow, Ukrainian Language, UT Austin</div>
            <p>Advanced regional language training supporting research on Ukraine and agricultural governance.</p>
          </div>
        </li>
      </ul>
    </section>

    <section id="contact" class="home-footer-panel">
      <span class="home-label">Contact</span>
      <h2>Open to collaboration, conversation, and research exchange</h2>
      <p>I am always glad to connect with researchers, practitioners, and institutions working on food systems, Eastern Europe, agriculture, or climate adaptation.</p>
      <div class="home-links">
        <a href="/research/">Research</a>
        <a href="/cv/">CV</a>
        <a href="/contact/">Contact Page</a>
        <a href="https://linkedin.com/in/evan-samsky">LinkedIn</a>
      </div>
    </section>
  </div>
</div>
