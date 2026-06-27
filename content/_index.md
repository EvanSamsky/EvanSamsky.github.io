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

  .home-masthead p.home-masthead-top,
  .home-masthead p.home-masthead-sub {
    font-family: 'Source Serif 4', serif;
    font-weight: 700;
    font-size: 0.82rem;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: #fff2d6;
    background: linear-gradient(180deg, rgba(123, 70, 58, 0.34), rgba(123, 70, 58, 0.22));
    border: 1px solid rgba(245, 239, 230, 0.14);
    border-radius: 999px;
    display: inline-block;
    padding: 0.16rem 0.72rem;
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

  .home-map-grid {
    display: grid;
    grid-template-columns: minmax(0, 1.15fr) minmax(280px, 0.85fr);
    gap: 1.35rem;
    align-items: stretch;
    margin-top: 1.5rem;
  }

  .home-map-frame,
  .home-map-detail {
    background: #f6f0e6;
    border: 1px solid var(--home-border);
  }

  .home-map-frame {
    padding: 1rem;
    position: relative;
    overflow: hidden;
  }

  .home-map-frame::before {
    content: '';
    position: absolute;
    inset: 0;
    background:
      radial-gradient(circle at 18% 82%, rgba(123, 70, 58, 0.08), transparent 28%),
      radial-gradient(circle at 84% 18%, rgba(95, 127, 105, 0.1), transparent 30%);
  }

  .home-map {
    position: relative;
    z-index: 1;
    display: block;
    width: 100%;
    height: auto;
  }

  .home-map-water {
    fill: #efe7dc;
  }

  .home-map-land {
    fill: #fbf7f0;
    stroke: #d5c8b4;
    stroke-width: 1.5;
  }

  .home-map-route {
    fill: none;
    stroke: rgba(123, 70, 58, 0.28);
    stroke-width: 2.2;
    stroke-dasharray: 8 6;
  }

  .home-country {
    cursor: pointer;
    stroke: rgba(250, 247, 240, 0.95);
    stroke-width: 2;
    transition: transform 0.18s ease, opacity 0.18s ease, filter 0.18s ease, stroke-width 0.18s ease;
    transform-box: fill-box;
    transform-origin: center;
  }

  .home-country:hover,
  .home-country:focus,
  .home-country.is-active {
    filter: drop-shadow(0 7px 16px rgba(36, 64, 65, 0.22));
    opacity: 1;
    stroke-width: 3;
    transform: translateY(-1px);
    outline: none;
  }

  .home-country--morocco {
    fill: #b76a66;
  }

  .home-country--estonia {
    fill: #7e9b88;
  }

  .home-country--czechia {
    fill: #c8866f;
  }

  .home-country--bulgaria {
    fill: #d2a75f;
  }

  .home-country--ukraine {
    fill: #8a6d9a;
  }

  .home-map-label-text {
    font-family: 'Source Serif 4', Georgia, serif;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.08em;
    fill: var(--home-ink);
  }

  .home-map-detail {
    border-top: 3px solid var(--home-rust);
    padding: 1.15rem 1.2rem;
  }

  .home-map-detail h3 {
    margin-top: 0.3rem;
    margin-bottom: 0.5rem;
  }

  .home-map-detail p:last-of-type {
    margin-bottom: 0;
  }

  .home-map-meta {
    margin-top: 0.95rem;
    padding-top: 0.95rem;
    border-top: 1px solid var(--home-border);
    color: var(--home-muted);
    font-size: 0.92rem;
  }

  .home-country-controls {
    display: flex;
    flex-wrap: wrap;
    gap: 0.55rem;
    margin-top: 1rem;
  }

  .home-country-chip {
    border: 1px solid var(--home-border);
    background: #fbf7f0;
    color: var(--home-rust);
    font-family: 'Source Serif 4', Georgia, serif;
    font-size: 0.78rem;
    font-weight: 700;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    padding: 0.45rem 0.7rem;
    cursor: pointer;
  }

  .home-country-chip:hover,
  .home-country-chip:focus,
  .home-country-chip.is-active {
    background: rgba(123, 70, 58, 0.12);
    border-color: rgba(123, 70, 58, 0.35);
    outline: none;
  }

  .home-map-note {
    margin-top: 1rem;
    font-size: 0.9rem;
    color: var(--home-muted);
  }

  .home-country-card {
    display: none;
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

    .home-map-grid {
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
    <a href="#geography">Geography</a>
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

    <section id="geography">
      <span class="home-label">Geographic experience</span>
      <h2>Selected places in study, research, and field-based work</h2>
      <p>This map highlights places that already structure the current research agenda. Move across the highlighted countries, or select one on mobile, to view the related experience.</p>
      <div class="home-map-grid">
        <div class="home-map-frame">
          <svg class="home-map" viewBox="0 0 620 420" role="img" aria-labelledby="home-map-title home-map-desc">
            <title id="home-map-title">Selected research and study locations</title>
            <desc id="home-map-desc">Highlighted countries show selected places connected to academic research, language study, and professional experience.</desc>
            <rect class="home-map-water" x="0" y="0" width="620" height="420"></rect>
            <path class="home-map-land" d="M108 302 C134 248, 182 196, 233 159 C286 121, 347 97, 404 103 C461 108, 505 134, 536 174 C560 206, 572 233, 566 260 C557 287, 531 307, 497 315 C449 327, 397 319, 345 302 C287 283, 235 284, 196 296 C165 305, 137 314, 108 302 Z"></path>
            <path class="home-map-land" d="M66 315 C81 295, 108 286, 137 289 C161 291, 178 301, 183 318 C188 336, 176 351, 149 358 C118 365, 91 359, 73 344 C61 333, 58 323, 66 315 Z"></path>
            <path class="home-map-route" d="M97 321 C159 289, 221 235, 301 180 C365 136, 439 145, 485 186"></path>
            <path class="home-map-route" d="M307 178 C319 144, 332 121, 321 96"></path>
            <path class="home-map-route" d="M359 241 C373 226, 389 212, 413 200"></path>

            <path tabindex="0" aria-label="Morocco" class="home-country home-country--morocco" data-country="morocco" d="M78 312 L100 303 L122 311 L118 329 L93 334 L75 324 Z"></path>
            <text class="home-map-label-text" x="56" y="348">MOROCCO</text>

            <path tabindex="0" aria-label="Estonia" class="home-country home-country--estonia" data-country="estonia" d="M312 87 L329 83 L341 91 L334 104 L316 105 L307 95 Z"></path>
            <text class="home-map-label-text" x="286" y="75">ESTONIA</text>

            <path tabindex="0" aria-label="Czechia" class="home-country home-country--czechia" data-country="czechia" d="M284 169 L304 162 L323 168 L320 181 L299 186 L282 178 Z"></path>
            <text class="home-map-label-text" x="255" y="202">CZECHIA</text>

            <path tabindex="0" aria-label="Bulgaria" class="home-country home-country--bulgaria" data-country="bulgaria" d="M339 235 L367 231 L385 238 L378 249 L350 252 L337 244 Z"></path>
            <text class="home-map-label-text" x="318" y="272">BULGARIA</text>

            <path tabindex="0" aria-label="Ukraine" class="home-country home-country--ukraine is-active" data-country="ukraine" d="M391 170 L432 158 L481 170 L509 186 L499 214 L463 227 L423 220 L392 203 L383 185 Z"></path>
            <text class="home-map-label-text" x="443" y="247">UKRAINE</text>
          </svg>
          <div class="home-country-controls" aria-label="Country selector">
            <button class="home-country-chip" type="button" data-country-target="morocco">Morocco</button>
            <button class="home-country-chip" type="button" data-country-target="estonia">Estonia</button>
            <button class="home-country-chip" type="button" data-country-target="czechia">Czechia</button>
            <button class="home-country-chip" type="button" data-country-target="bulgaria">Bulgaria</button>
            <button class="home-country-chip is-active" type="button" data-country-target="ukraine">Ukraine</button>
          </div>
        </div>

        <div class="home-map-detail" aria-live="polite">
          <span class="home-label">Selected country</span>
          <h3 data-map-title>Ukraine</h3>
          <p data-map-body>I conducted policy research on climate adaptation in Ukrainian agriculture and produced briefing materials on food security, agricultural recovery, and environmental sustainability.</p>
          <p class="home-map-meta" data-map-meta>The CV also lists Ukrainian language study, systems mapping on adaptation policy, and multiple Ukraine-focused reports and publications.</p>
        </div>
      </div>

      <div class="home-country-card" data-country="morocco" data-title="Morocco" data-body="I worked as an agricultural volunteer in Meknes and presented in Arabic at the Arabic Language Flagship Capstone Student Panel in Fes." data-meta="The experience connects field agriculture, language study, and public presentation."></div>
      <div class="home-country-card" data-country="estonia" data-title="Estonia" data-body="I served as resident director for American Councils programs in Narva during the summers of 2022 and 2023." data-meta="The site profile also identifies Estonia as part of the comparative regional experience behind the current research agenda."></div>
      <div class="home-country-card" data-country="czechia" data-title="Czechia" data-body="I am a visiting researcher at the Czech University of Life Sciences, where I am conducting thesis research on farmer networks and environmental solutions in EU agricultural governance." data-meta="Related entries include Czech language training at Indiana University and scholarship support for on-site thesis research."></div>
      <div class="home-country-card" data-country="bulgaria" data-title="Bulgaria" data-body="I conducted archival research with Bulgarian National Statistical Institute materials and analyzed agricultural data from 1944 through 1989." data-meta="The CV also lists coauthored work on agricultural transformation and environmental politics in Bulgaria."></div>
      <div class="home-country-card" data-country="ukraine" data-title="Ukraine" data-body="I conducted policy research on climate adaptation in Ukrainian agriculture and produced briefing materials on food security, agricultural recovery, and environmental sustainability." data-meta="The CV also lists Ukrainian language study, systems mapping on adaptation policy, and multiple Ukraine-focused reports and publications."></div>
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

<script>
  (function () {
    var detailTitle = document.querySelector('[data-map-title]');
    var detailBody = document.querySelector('[data-map-body]');
    var detailMeta = document.querySelector('[data-map-meta]');
    var cards = Array.prototype.slice.call(document.querySelectorAll('.home-country-card'));
    var regions = Array.prototype.slice.call(document.querySelectorAll('.home-country'));
    var chips = Array.prototype.slice.call(document.querySelectorAll('.home-country-chip'));

    if (!detailTitle || !detailBody || !detailMeta || !cards.length) {
      return;
    }

    function activate(country) {
      var match = cards.find(function (card) {
        return card.getAttribute('data-country') === country;
      });

      if (!match) {
        return;
      }

      detailTitle.textContent = match.getAttribute('data-title');
      detailBody.textContent = match.getAttribute('data-body');
      detailMeta.textContent = match.getAttribute('data-meta');

      regions.forEach(function (region) {
        var isActive = region.getAttribute('data-country') === country;
        region.classList.toggle('is-active', isActive);
      });

      chips.forEach(function (chip) {
        var isActive = chip.getAttribute('data-country-target') === country;
        chip.classList.toggle('is-active', isActive);
      });
    }

    regions.forEach(function (region) {
      ['mouseenter', 'focus', 'click'].forEach(function (eventName) {
        region.addEventListener(eventName, function () {
          activate(region.getAttribute('data-country'));
        });
      });
    });

    chips.forEach(function (chip) {
      chip.addEventListener('click', function () {
        activate(chip.getAttribute('data-country-target'));
      });
    });
  })();
</script>
