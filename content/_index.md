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

  .home-map-context {
    fill: #fbf7f0;
    stroke: #d5c8b4;
    stroke-width: 1.3;
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
    pointer-events: none;
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
            <path class="home-map-context" data-name="Portugal" d="M 88.1 242.1 L 91.8 239.5 L 95.9 238.1 L 98.4 243.0 L 104.4 243.0 L 106.1 241.7 L 112.0 242.1 L 114.8 247.1 L 110.1 249.8 L 110.0 257.7 L 108.4 259.2 L 108.0 263.9 L 103.6 264.8 L 107.6 270.8 L 104.9 277.4 L 108.3 280.4 L 106.9 283.1 L 103.2 286.9 L 104.1 290.3 L 100.0 292.9 L 94.7 291.5 L 89.5 292.6 L 91.0 284.7 L 90.1 278.5 L 85.6 277.6 L 83.2 273.7 L 84.0 267.2 L 88.0 263.5 L 90.8 253.4 L 90.6 249.1 L 88.6 245.5 L 88.1 242.1 Z"></path>
            <path class="home-map-context" data-name="Spain" d="M 104.1 290.3 L 103.2 286.9 L 106.9 283.1 L 108.3 280.4 L 104.9 277.4 L 107.6 270.8 L 103.6 264.8 L 108.0 263.9 L 108.4 259.2 L 110.0 257.7 L 110.1 249.8 L 114.8 247.1 L 112.0 242.1 L 106.1 241.7 L 104.4 243.0 L 98.4 243.0 L 95.9 238.1 L 91.8 239.5 L 88.1 242.1 L 88.6 234.9 L 84.5 230.6 L 98.8 223.3 L 111.1 225.1 L 124.6 225.0 L 135.3 226.8 L 143.7 226.2 L 160.0 226.6 L 164.0 230.5 L 182.5 235.1 L 186.2 232.9 L 197.5 237.4 L 209.2 236.1 L 209.7 242.0 L 200.2 248.7 L 187.3 250.8 L 186.4 254.2 L 180.2 259.8 L 176.3 268.0 L 180.2 273.7 L 174.4 278.2 L 172.2 284.8 L 164.6 286.8 L 157.5 294.5 L 135.1 294.5 L 128.8 298.0 L 125.0 301.8 L 120.0 301.0 L 116.3 297.6 L 113.5 291.8 L 104.1 290.3 Z"></path>
            <path class="home-map-context" data-name="France" d="M 241.4 165.7 L 246.1 168.4 L 260.7 170.2 L 255.6 177.1 L 254.3 184.3 L 251.5 186.0 L 246.9 185.1 L 247.3 187.7 L 239.9 193.3 L 239.7 197.9 L 244.6 196.3 L 248.0 200.7 L 247.6 203.6 L 250.6 207.3 L 247.1 210.4 L 249.7 218.2 L 255.1 219.5 L 254.0 223.8 L 244.8 229.5 L 225.0 226.8 L 210.3 230.1 L 209.2 236.1 L 197.5 237.4 L 186.2 232.9 L 182.5 235.1 L 164.0 230.5 L 160.0 226.6 L 165.2 220.5 L 167.1 200.5 L 156.7 189.9 L 149.3 184.8 L 133.9 180.9 L 132.9 173.6 L 145.9 171.4 L 162.8 174.0 L 159.6 162.6 L 169.1 166.9 L 192.6 159.1 L 195.6 150.8 L 204.4 148.8 L 205.9 152.3 L 210.6 152.5 L 222.3 161.3 L 227.4 160.5 L 238.5 166.0 L 241.4 165.7 Z M 267.2 234.6 L 273.7 230.7 L 275.4 239.4 L 272.0 247.1 L 267.5 245.1 L 265.1 238.3 L 267.2 234.6 Z"></path>
            <path class="home-map-context" data-name="Ireland" d="M 116.7 121.4 L 118.4 128.6 L 110.7 137.6 L 92.9 143.5 L 78.6 142.0 L 86.8 131.5 L 81.6 121.3 L 102.9 108.7 L 104.9 114.1 L 102.9 119.5 L 109.1 119.3 L 116.7 121.4 Z"></path>
            <path class="home-map-context" data-name="United Kingdom" d="M 116.7 121.4 L 109.1 119.3 L 102.9 119.5 L 104.9 114.1 L 102.9 108.7 L 111.3 108.3 L 122.1 114.5 L 116.7 121.4 Z M 148.0 126.1 L 149.5 120.2 L 142.6 113.9 L 130.3 112.1 L 127.9 109.4 L 131.6 104.9 L 128.3 102.1 L 122.9 106.9 L 122.3 97.2 L 117.2 92.0 L 120.8 81.6 L 128.7 73.4 L 136.7 74.2 L 148.8 73.4 L 138.1 84.3 L 148.3 82.9 L 159.4 83.0 L 156.8 91.2 L 147.7 100.2 L 158.1 100.8 L 167.9 113.8 L 174.8 115.4 L 181.0 126.9 L 183.8 130.8 L 196.0 132.8 L 194.8 139.2 L 189.7 142.2 L 193.7 147.4 L 184.6 152.6 L 171.2 152.5 L 154.0 155.3 L 149.3 153.3 L 142.7 158.0 L 133.4 156.9 L 126.3 160.7 L 120.9 158.7 L 135.7 148.2 L 144.7 146.0 L 128.9 144.3 L 126.1 140.3 L 136.6 137.2 L 131.1 131.7 L 133.0 125.2 L 148.0 126.1 Z"></path>
            <path class="home-map-context" data-name="Belgium" d="M 241.1 152.3 L 240.0 159.1 L 237.3 159.4 L 236.2 165.1 L 227.4 160.5 L 222.3 161.3 L 210.6 152.5 L 205.9 152.3 L 204.4 148.8 L 212.5 146.8 L 219.9 147.6 L 229.2 145.5 L 235.6 149.9 L 241.1 152.3 Z"></path>
            <path class="home-map-context" data-name="Netherlands" d="M 248.6 125.3 L 250.5 128.7 L 248.0 137.9 L 245.5 141.7 L 239.4 141.7 L 241.1 152.3 L 235.6 149.9 L 229.2 145.5 L 219.9 147.6 L 212.5 146.8 L 217.7 144.0 L 226.5 129.2 L 240.3 125.0 L 248.6 125.3 Z"></path>
            <path class="home-map-context" data-name="Luxembourg" d="M 240.0 159.1 L 242.0 161.3 L 241.4 165.7 L 238.5 166.0 L 236.2 165.1 L 237.3 159.4 L 240.0 159.1 Z"></path>
            <path class="home-map-context" data-name="Germany" d="M 321.3 122.5 L 323.6 127.6 L 320.8 130.3 L 324.5 133.9 L 327.0 139.3 L 326.2 142.8 L 330.3 149.2 L 325.8 150.3 L 323.2 149.1 L 320.6 151.0 L 313.4 153.0 L 309.7 155.5 L 302.3 157.7 L 304.1 160.7 L 305.2 164.9 L 310.3 167.3 L 316.0 171.7 L 312.5 176.3 L 308.8 177.6 L 310.3 184.1 L 309.3 185.8 L 306.2 183.8 L 301.4 183.5 L 294.2 185.3 L 285.3 184.8 L 283.8 187.5 L 278.7 184.7 L 275.7 185.3 L 264.9 182.2 L 262.9 184.4 L 254.3 184.3 L 255.6 177.1 L 260.7 170.2 L 246.1 168.4 L 241.4 165.7 L 242.0 161.3 L 240.0 159.1 L 241.1 152.3 L 239.4 141.7 L 245.5 141.7 L 248.0 137.9 L 250.5 128.7 L 248.6 125.3 L 250.6 123.2 L 259.0 122.6 L 260.9 124.8 L 267.7 119.9 L 265.4 116.1 L 265.0 110.4 L 272.6 111.7 L 279.0 110.2 L 279.2 114.1 L 289.4 116.4 L 289.3 120.0 L 299.5 118.1 L 305.2 115.3 L 316.5 119.3 L 321.3 122.5 Z"></path>
            <path class="home-map-context" data-name="Switzerland" d="M 275.7 185.3 L 276.1 187.1 L 274.6 189.5 L 279.1 191.3 L 284.3 191.6 L 283.5 195.8 L 279.0 197.4 L 271.6 196.2 L 269.4 200.2 L 264.6 200.6 L 262.8 199.0 L 257.2 202.4 L 252.3 202.9 L 248.0 200.7 L 244.6 196.3 L 239.7 197.9 L 239.9 193.3 L 247.3 187.7 L 246.9 185.1 L 251.5 186.0 L 254.3 184.3 L 262.9 184.4 L 264.9 182.2 L 275.7 185.3 Z"></path>
            <path class="home-map-context" data-name="Italy" d="M 284.3 191.6 L 290.4 193.1 L 291.5 191.1 L 301.5 189.4 L 303.7 192.9 L 318.1 195.5 L 317.0 200.5 L 319.4 204.7 L 311.4 203.3 L 303.2 206.8 L 303.8 211.8 L 302.6 214.7 L 305.9 219.8 L 315.3 224.9 L 320.4 233.2 L 331.6 241.3 L 339.5 241.3 L 341.9 243.5 L 339.1 245.5 L 355.5 252.2 L 364.1 257.5 L 365.2 259.3 L 363.3 262.9 L 357.7 258.2 L 349.0 256.6 L 344.7 263.1 L 352.0 266.8 L 350.8 272.1 L 346.6 272.7 L 341.2 281.3 L 337.0 282.1 L 337.1 279.0 L 339.1 273.6 L 341.3 271.5 L 334.3 260.5 L 330.1 259.3 L 327.2 254.9 L 320.7 253.1 L 316.3 249.1 L 301.0 243.9 L 291.8 237.3 L 284.9 231.5 L 281.8 221.6 L 276.8 220.4 L 268.6 217.1 L 264.0 218.4 L 258.2 223.1 L 254.0 223.8 L 255.1 219.5 L 249.7 218.2 L 247.1 210.4 L 250.6 207.3 L 247.6 203.6 L 248.0 200.7 L 252.3 202.9 L 257.2 202.4 L 262.8 199.0 L 264.6 200.6 L 269.4 200.2 L 271.6 196.2 L 279.0 197.4 L 283.5 195.8 L 284.3 191.6 Z M 327.7 279.7 L 335.4 278.8 L 331.8 286.8 L 333.3 289.9 L 331.1 295.1 L 323.4 291.3 L 318.3 290.2 L 304.3 285.1 L 305.7 279.9 L 317.5 280.8 L 327.7 279.7 Z M 266.8 252.0 L 271.8 248.9 L 277.9 256.0 L 276.5 269.3 L 271.9 268.7 L 267.8 272.0 L 264.0 269.4 L 263.6 257.2 L 261.3 251.5 L 266.8 252.0 Z"></path>
            <path class="home-map-context" data-name="Austria" d="M 350.1 179.2 L 349.3 183.4 L 343.6 183.4 L 345.6 185.6 L 342.2 192.0 L 340.3 193.7 L 331.5 194.0 L 318.1 195.5 L 303.7 192.9 L 301.5 189.4 L 291.5 191.1 L 290.4 193.1 L 284.3 191.6 L 279.1 191.3 L 274.6 189.5 L 276.1 187.1 L 275.7 185.3 L 278.7 184.7 L 283.8 187.5 L 285.3 184.8 L 294.2 185.3 L 301.4 183.5 L 306.2 183.8 L 309.3 185.8 L 310.3 184.1 L 308.8 177.6 L 312.5 176.3 L 316.0 171.7 L 323.5 174.9 L 329.1 170.8 L 332.7 170.0 L 340.5 173.1 L 345.2 172.6 L 349.9 174.5 L 349.1 175.8 L 350.1 179.2 Z"></path>
            <path class="home-map-context" data-name="Denmark" d="M 279.0 110.2 L 272.6 111.7 L 265.0 110.4 L 260.9 104.8 L 260.6 94.5 L 265.1 88.8 L 274.0 88.1 L 277.5 85.4 L 285.6 82.5 L 285.3 87.7 L 282.3 91.0 L 283.5 93.8 L 289.0 95.3 L 286.5 99.1 L 283.5 98.0 L 276.3 105.3 L 279.0 110.2 Z M 303.7 98.8 L 306.9 103.9 L 300.8 112.0 L 290.3 106.3 L 288.9 102.1 L 303.7 98.8 Z"></path>
            <path class="home-map-context" data-name="Sweden" d="M 290.1 71.2 L 294.6 65.4 L 303.0 58.5 L 306.3 46.6 L 299.9 41.5 L 299.2 28.2 L 305.8 18.7 L 315.8 18.9 L 319.3 14.9 L 315.6 11.5 L 331.2 -2.7 L 347.9 -21.0 L 357.6 -21.0 L 360.3 -26.6 L 416.1 -20.3 L 416.4 -4.7 L 419.8 -0.8 L 402.5 2.0 L 392.7 9.0 L 394.3 15.2 L 378.3 23.3 L 358.8 32.0 L 351.5 46.2 L 358.6 53.2 L 368.3 58.8 L 359.0 70.2 L 348.6 72.5 L 344.7 89.4 L 339.0 98.9 L 326.8 97.9 L 321.1 105.9 L 309.4 106.4 L 306.2 96.8 L 297.8 85.4 L 290.1 71.2 Z"></path>
            <path class="home-map-context" data-name="Latvia" d="M 453.9 85.1 L 458.7 87.4 L 459.6 92.3 L 462.8 98.2 L 445.9 103.8 L 436.2 98.9 L 430.8 98.3 L 429.4 96.2 L 419.5 97.2 L 402.6 96.5 L 391.1 99.6 L 391.5 92.0 L 396.4 85.7 L 405.9 82.3 L 413.9 89.8 L 422.0 89.6 L 423.9 81.9 L 432.5 80.1 L 445.6 85.1 L 453.9 85.1 Z"></path>
            <path class="home-map-context" data-name="Lithuania" d="M 445.9 103.8 L 446.8 108.3 L 438.6 111.5 L 436.2 117.2 L 425.3 121.0 L 415.6 121.0 L 413.1 117.8 L 408.0 116.8 L 407.2 114.2 L 408.3 111.4 L 403.8 109.8 L 393.3 108.1 L 391.1 99.6 L 402.6 96.5 L 419.5 97.2 L 429.4 96.2 L 430.8 98.3 L 436.2 98.9 L 445.9 103.8 Z"></path>
            <path class="home-map-context" data-name="Belarus" d="M 462.8 98.2 L 473.4 100.8 L 474.8 103.3 L 480.1 102.1 L 490.0 104.5 L 491.0 109.2 L 488.8 111.9 L 495.1 118.5 L 499.2 120.3 L 498.6 122.1 L 505.4 123.9 L 508.3 126.6 L 504.4 128.8 L 496.3 128.5 L 494.3 129.4 L 496.7 132.7 L 499.2 139.2 L 490.5 139.8 L 487.4 142.0 L 486.8 147.1 L 482.8 146.1 L 473.7 146.6 L 471.0 144.2 L 467.3 146.0 L 463.5 144.5 L 455.5 144.3 L 444.3 141.9 L 434.1 141.1 L 426.3 141.3 L 420.8 144.1 L 416.0 144.5 L 415.8 140.0 L 412.7 135.3 L 418.7 133.2 L 418.8 129.2 L 416.0 125.4 L 415.6 121.0 L 425.3 121.0 L 436.2 117.2 L 438.6 111.5 L 446.8 108.3 L 445.9 103.8 L 452.0 102.1 L 462.8 98.2 Z"></path>
            <path class="home-map-context" data-name="Poland" d="M 415.6 121.0 L 416.0 125.4 L 418.8 129.2 L 418.7 133.2 L 412.7 135.3 L 415.8 140.0 L 416.0 144.5 L 421.1 153.2 L 420.0 156.1 L 415.0 157.2 L 405.8 165.6 L 408.4 170.1 L 396.7 165.7 L 389.4 167.1 L 384.7 166.1 L 378.7 168.2 L 373.6 164.7 L 369.5 166.0 L 364.3 160.5 L 356.8 159.9 L 355.9 156.7 L 349.0 155.6 L 347.5 158.2 L 342.0 156.1 L 342.6 153.3 L 335.1 152.4 L 330.3 149.2 L 326.2 142.8 L 327.0 139.3 L 324.5 133.9 L 320.8 130.3 L 323.6 127.6 L 321.3 122.5 L 328.2 119.6 L 356.5 111.5 L 366.6 113.2 L 367.4 115.7 L 389.5 116.9 L 408.0 116.8 L 413.1 117.8 L 415.6 121.0 Z"></path>
            <path class="home-map-context" data-name="Slovakia" d="M 406.2 169.6 L 403.4 172.2 L 401.5 176.2 L 399.3 177.3 L 388.6 174.2 L 385.3 174.8 L 377.1 177.8 L 372.2 179.4 L 368.2 179.7 L 367.4 181.7 L 358.9 182.9 L 355.2 181.8 L 350.1 179.2 L 349.1 175.8 L 351.3 172.3 L 355.8 172.4 L 359.2 171.4 L 359.5 170.4 L 361.4 170.0 L 362.1 167.7 L 364.4 167.2 L 365.9 165.4 L 368.9 165.4 L 369.5 166.0 L 373.6 164.7 L 378.7 168.2 L 384.7 166.1 L 389.4 167.1 L 396.7 165.7 L 406.2 169.6 Z"></path>
            <path class="home-map-context" data-name="Hungary" d="M 401.5 176.2 L 407.1 179.0 L 407.8 181.7 L 401.6 183.8 L 396.9 190.6 L 390.8 197.4 L 382.7 199.3 L 376.4 198.9 L 364.9 203.0 L 356.6 201.1 L 345.9 195.5 L 343.9 192.1 L 342.2 192.0 L 345.6 185.6 L 343.6 183.4 L 349.3 183.4 L 350.1 179.2 L 358.9 182.9 L 367.4 181.7 L 368.2 179.7 L 372.2 179.4 L 377.1 177.8 L 382.9 177.2 L 385.3 174.8 L 388.6 174.2 L 399.3 177.3 L 401.5 176.2 Z"></path>
            <path class="home-map-context" data-name="Slovenia" d="M 318.1 195.5 L 326.4 196.3 L 331.5 194.0 L 340.3 193.7 L 342.2 192.0 L 343.9 192.1 L 345.9 195.5 L 337.9 198.2 L 336.9 202.3 L 333.4 203.3 L 333.4 206.1 L 329.5 205.9 L 326.1 204.3 L 324.2 206.0 L 317.2 205.7 L 319.4 204.7 L 317.0 200.5 L 318.1 195.5 Z"></path>
            <path class="home-map-context" data-name="Croatia" d="M 345.9 195.5 L 356.6 201.1 L 364.9 203.0 L 368.7 201.5 L 371.1 205.4 L 374.3 208.3 L 370.5 212.1 L 365.9 209.9 L 359.0 210.0 L 350.3 208.3 L 345.6 208.6 L 343.4 210.6 L 339.8 208.3 L 337.7 212.5 L 342.6 217.2 L 353.3 226.3 L 357.1 230.5 L 366.0 234.4 L 364.9 236.1 L 355.4 232.3 L 349.6 228.7 L 340.4 225.7 L 331.9 218.3 L 333.9 217.6 L 329.3 213.3 L 329.1 209.9 L 322.7 208.3 L 319.6 212.7 L 316.6 209.3 L 317.2 205.7 L 324.2 206.0 L 326.1 204.3 L 329.5 205.9 L 333.4 206.1 L 333.4 203.3 L 336.9 202.3 L 337.9 198.2 L 345.9 195.5 Z"></path>
            <path class="home-map-context" data-name="Bosnia and Herz." d="M 366.0 234.4 L 357.1 230.5 L 353.3 226.3 L 342.6 217.2 L 337.7 212.5 L 339.8 208.3 L 343.4 210.6 L 345.6 208.6 L 350.3 208.3 L 359.0 210.0 L 365.9 209.9 L 370.5 212.1 L 374.1 212.1 L 371.6 216.5 L 376.5 220.4 L 375.0 225.1 L 370.7 226.5 L 367.5 228.8 L 366.0 234.4 Z"></path>
            <path class="home-map-context" data-name="Serbia" d="M 368.7 201.5 L 376.4 198.9 L 382.7 199.3 L 388.2 203.3 L 389.3 206.5 L 395.4 208.9 L 396.2 213.0 L 402.1 215.9 L 405.2 213.7 L 407.7 214.9 L 405.4 216.6 L 407.2 218.4 L 404.8 220.7 L 405.7 224.4 L 410.5 228.7 L 406.7 231.8 L 405.0 235.1 L 406.1 236.3 L 404.5 237.7 L 396.4 238.4 L 396.0 237.7 L 398.4 234.0 L 396.9 234.1 L 388.7 228.1 L 386.9 228.6 L 385.5 232.0 L 383.1 232.7 L 383.9 231.8 L 376.8 228.7 L 372.6 225.6 L 375.0 225.1 L 376.5 220.4 L 371.6 216.5 L 374.1 212.1 L 370.5 212.1 L 374.3 208.3 L 371.1 205.4 L 368.7 201.5 Z"></path>
            <path class="home-map-context" data-name="Montenegro" d="M 381.2 235.0 L 378.5 235.9 L 377.8 234.0 L 373.5 238.9 L 374.2 242.1 L 372.0 241.3 L 369.2 238.1 L 364.9 236.1 L 366.0 234.4 L 367.5 228.8 L 372.6 225.6 L 376.8 228.7 L 383.9 231.8 L 383.1 232.7 L 381.2 235.0 Z"></path>
            <path class="home-map-context" data-name="Kosovo" d="M 386.4 242.4 L 385.7 238.7 L 383.3 237.7 L 381.2 235.0 L 383.1 232.7 L 385.5 232.0 L 386.9 228.6 L 388.7 228.1 L 396.9 234.1 L 398.4 234.0 L 396.0 237.7 L 396.4 238.4 L 388.2 240.4 L 387.7 242.4 L 386.4 242.4 Z"></path>
            <path class="home-map-context" data-name="Albania" d="M 390.8 252.5 L 390.6 255.2 L 387.3 256.7 L 386.7 259.9 L 382.0 264.8 L 380.3 264.1 L 380.1 261.9 L 374.5 258.5 L 373.6 253.7 L 374.5 246.8 L 375.9 243.7 L 374.2 242.1 L 373.5 238.9 L 377.8 234.0 L 378.5 235.9 L 381.2 235.0 L 383.3 237.7 L 385.7 238.7 L 386.4 242.4 L 385.1 245.8 L 386.6 250.1 L 390.8 252.5 Z"></path>
            <path class="home-map-context" data-name="North Macedonia" d="M 404.5 237.7 L 409.5 240.9 L 410.2 247.6 L 408.3 247.9 L 406.6 249.7 L 401.2 249.5 L 397.3 251.7 L 390.8 252.5 L 386.6 250.1 L 385.1 245.8 L 386.4 242.4 L 387.7 242.4 L 388.2 240.4 L 399.8 237.8 L 404.5 237.7 Z"></path>
            <path class="home-map-context" data-name="Greece" d="M 443.8 308.4 L 442.6 311.3 L 428.1 312.2 L 428.2 310.5 L 415.9 308.6 L 417.7 304.3 L 423.2 307.7 L 431.1 307.1 L 438.6 307.8 L 438.3 309.6 L 443.8 308.4 Z M 410.2 247.6 L 417.7 247.9 L 425.7 245.1 L 432.8 248.6 L 442.0 247.7 L 442.1 242.6 L 447.0 245.3 L 443.9 251.6 L 441.5 252.7 L 430.1 251.5 L 417.9 254.1 L 424.9 259.8 L 419.8 261.4 L 414.1 261.4 L 408.8 256.2 L 406.9 258.5 L 409.2 264.5 L 414.2 269.2 L 410.4 271.4 L 416.0 276.0 L 421.0 279.0 L 421.2 284.6 L 411.8 282.0 L 414.8 287.1 L 408.4 288.2 L 412.2 297.1 L 405.6 297.2 L 397.3 292.8 L 393.5 284.7 L 391.8 278.0 L 382.7 267.7 L 382.0 264.8 L 386.7 259.9 L 387.3 256.7 L 390.6 255.2 L 390.8 252.5 L 397.3 251.7 L 401.2 249.5 L 406.6 249.7 L 408.3 247.9 L 410.2 247.6 Z"></path>
            <path class="home-map-context" data-name="Romania" d="M 463.4 205.8 L 467.9 207.6 L 472.6 206.0 L 477.2 207.7 L 477.4 210.3 L 472.5 212.5 L 469.5 211.6 L 466.7 223.7 L 460.7 222.6 L 453.4 219.0 L 441.6 221.3 L 436.6 223.9 L 421.8 223.4 L 414.0 221.8 L 410.1 222.5 L 405.4 216.6 L 407.7 214.9 L 405.2 213.7 L 402.1 215.9 L 396.2 213.0 L 395.4 208.9 L 389.3 206.5 L 388.2 203.3 L 382.7 199.3 L 390.8 197.4 L 396.9 190.6 L 401.6 183.8 L 412.1 179.5 L 418.4 180.6 L 424.8 180.7 L 429.5 183.1 L 432.9 181.6 L 440.4 180.6 L 442.9 178.3 L 447.1 178.3 L 450.2 179.2 L 462.3 192.5 L 462.6 196.9 L 461.6 201.2 L 463.4 205.8 Z"></path>
            <path class="home-map-context" data-name="Moldova" d="M 447.1 178.3 L 449.5 176.8 L 456.2 175.8 L 463.6 178.9 L 467.8 179.3 L 472.3 182.0 L 471.6 185.4 L 475.3 187.1 L 476.7 191.3 L 480.3 193.8 L 479.5 195.3 L 481.4 196.4 L 478.8 197.1 L 472.8 196.8 L 471.8 195.4 L 469.7 196.2 L 470.4 198.0 L 467.7 201.2 L 465.9 204.7 L 463.4 205.8 L 461.6 201.2 L 462.6 196.9 L 462.3 192.5 L 450.2 179.2 L 447.1 178.3 Z"></path>
            <path class="home-map-context" data-name="Turkey" d="M 629.9 289.5 L 625.1 291.2 L 621.6 288.7 L 609.8 287.4 L 605.5 288.9 L 594.1 290.5 L 588.6 290.3 L 577.1 294.1 L 568.8 294.1 L 563.4 292.2 L 552.3 295.0 L 549.0 293.1 L 548.5 298.7 L 543.1 303.1 L 539.4 298.5 L 543.2 294.8 L 537.1 295.6 L 528.6 293.3 L 521.7 299.1 L 506.4 300.2 L 498.3 294.8 L 487.4 294.5 L 485.1 298.7 L 478.2 299.9 L 468.4 294.5 L 457.4 294.7 L 451.5 284.7 L 444.1 279.1 L 449.0 271.2 L 442.6 266.4 L 453.8 256.8 L 469.3 256.4 L 473.5 248.8 L 492.7 250.1 L 504.8 243.6 L 516.5 240.7 L 533.2 240.5 L 550.8 247.6 L 565.2 251.5 L 577.0 249.9 L 585.6 250.8 L 597.5 245.6 L 608.2 245.1 L 617.9 250.0 L 619.6 253.6 L 618.7 258.5 L 626.2 261.0 L 630.1 263.9 L 623.2 266.8 L 626.4 278.3 L 624.4 281.5 L 629.9 289.5 Z M 442.1 242.6 L 452.3 239.5 L 461.0 240.8 L 462.2 244.7 L 471.0 247.9 L 469.2 250.4 L 457.2 251.0 L 444.5 259.5 L 441.3 254.8 L 441.5 252.7 L 443.9 251.6 L 447.0 245.3 L 442.1 242.6 Z"></path>
            <path class="home-map-context" data-name="Cyprus" d="M 508.7 310.0 L 510.6 310.5 L 515.2 309.7 L 516.2 311.4 L 520.1 310.4 L 521.2 310.8 L 521.5 311.6 L 511.2 315.7 L 506.2 314.4 L 503.9 310.3 L 508.7 310.0 Z"></path>
            <path class="home-map-context" data-name="W. Sahara" d="M 91.8 385.3 L 91.6 403.2 L 58.6 402.7 L 58.9 428.4 L 49.5 429.3 L 47.0 434.5 L 48.9 449.1 L 9.5 449.0 L 7.3 452.3 L 7.7 448.1 L 30.6 447.3 L 31.8 443.7 L 35.9 439.2 L 39.2 425.2 L 53.2 414.4 L 58.0 401.7 L 61.1 401.0 L 64.4 393.1 L 72.9 392.0 L 76.5 393.3 L 81.1 393.3 L 84.3 391.0 L 90.5 390.7 L 90.3 385.3 L 91.8 385.3 Z"></path>
            <path class="home-map-context" data-name="Mauritania" d="M 7.3 452.3 L 9.5 449.0 L 48.9 449.1 L 47.0 434.5 L 49.5 429.3 L 58.9 428.4 L 58.6 402.7 L 91.6 403.2 L 91.7 387.9 L 129.5 412.3 L 114.1 412.5 L 123.8 499.4 L 125.6 500.7 L 123.3 507.7 L 82.9 507.9 L 81.4 510.1 L 77.5 509.4 L 71.9 511.4 L 64.8 508.6 L 61.6 508.8 L 59.9 514.8 L 56.6 516.6 L 43.8 502.3 L 37.1 499.6 L 32.3 496.7 L 26.7 496.8 L 21.8 499.0 L 16.8 498.1 L 13.3 501.3 L 12.5 495.9 L 15.3 490.9 L 16.5 481.5 L 14.2 466.5 L 15.2 461.5 L 12.6 456.7 L 7.3 452.3 Z"></path>
            <path class="home-map-context" data-name="Algeria" d="M 91.7 387.9 L 91.8 373.4 L 108.0 366.0 L 118.1 364.4 L 126.3 361.7 L 130.2 356.7 L 141.9 352.7 L 142.4 345.2 L 148.2 344.4 L 152.8 340.6 L 165.9 338.9 L 167.8 335.0 L 165.1 332.9 L 161.6 322.3 L 161.0 316.1 L 157.3 309.7 L 166.9 304.2 L 177.8 302.4 L 184.2 298.3 L 193.9 295.2 L 210.9 293.4 L 227.6 292.6 L 232.7 294.1 L 242.2 290.1 L 252.9 290.0 L 257.0 292.4 L 263.9 291.8 L 261.8 296.9 L 263.4 306.5 L 261.1 314.9 L 254.9 320.5 L 255.8 328.1 L 264.0 334.1 L 264.1 336.5 L 270.3 340.6 L 274.6 358.6 L 277.8 367.5 L 278.4 372.2 L 276.6 380.4 L 277.3 385.0 L 276.1 390.5 L 276.9 396.8 L 272.9 401.1 L 278.9 408.4 L 279.3 412.7 L 282.9 418.3 L 287.6 416.5 L 295.5 421.2 L 299.9 427.5 L 265.4 446.6 L 236.3 466.4 L 222.1 470.9 L 210.9 471.9 L 210.8 465.5 L 199.9 461.0 L 197.5 456.3 L 129.5 412.3 L 91.7 387.9 Z"></path>
            <path class="home-map-context" data-name="Tunisia" d="M 274.6 358.6 L 270.3 340.6 L 264.1 336.5 L 264.0 334.1 L 255.8 328.1 L 254.9 320.5 L 261.1 314.9 L 263.4 306.5 L 261.8 296.9 L 263.9 291.8 L 274.9 287.7 L 281.9 288.9 L 281.6 294.0 L 290.2 290.3 L 290.9 292.2 L 285.8 297.2 L 285.8 301.8 L 289.3 304.3 L 287.9 313.1 L 281.3 318.1 L 283.2 323.6 L 288.4 323.8 L 291.0 328.6 L 294.8 330.1 L 294.2 337.9 L 289.3 340.8 L 286.2 344.0 L 279.3 347.9 L 280.4 352.0 L 279.5 356.3 L 274.6 358.6 Z"></path>
            <path class="home-map-context" data-name="Libya" d="M 430.8 442.3 L 430.8 462.4 L 419.2 462.4 L 419.1 466.6 L 338.8 428.1 L 321.5 437.3 L 315.9 431.8 L 299.9 427.5 L 295.5 421.2 L 287.6 416.5 L 282.9 418.3 L 279.3 412.7 L 278.9 408.4 L 272.9 401.1 L 276.9 396.8 L 276.1 390.5 L 277.3 385.0 L 276.6 380.4 L 278.4 372.2 L 277.8 367.5 L 274.6 358.6 L 279.5 356.3 L 280.4 352.0 L 279.3 347.9 L 286.2 344.0 L 289.3 340.8 L 294.2 337.9 L 294.8 330.1 L 306.6 333.6 L 310.8 332.7 L 319.3 334.4 L 332.6 338.9 L 337.3 347.9 L 360.6 354.0 L 371.3 359.0 L 376.2 356.4 L 381.0 351.8 L 378.7 344.1 L 381.8 339.2 L 389.1 334.5 L 396.0 333.1 L 409.6 335.2 L 413.1 339.7 L 416.8 339.7 L 420.0 341.4 L 430.0 342.6 L 432.5 345.9 L 428.8 350.8 L 430.4 355.1 L 427.8 361.3 L 430.8 369.4 L 430.8 405.2 L 430.8 442.3 Z"></path>
            <path class="home-map-context" data-name="Egypt" d="M 550.3 442.3 L 430.8 442.3 L 430.8 369.4 L 427.8 361.3 L 430.4 355.1 L 428.8 350.8 L 432.5 345.9 L 445.9 345.8 L 470.2 353.0 L 478.0 349.8 L 482.1 346.9 L 491.0 346.1 L 498.2 347.3 L 500.9 352.3 L 503.2 349.0 L 511.3 351.4 L 519.2 352.0 L 524.1 349.4 L 530.7 366.7 L 527.9 370.8 L 525.7 378.4 L 523.0 383.6 L 520.7 385.4 L 512.8 377.7 L 505.6 363.2 L 504.5 364.1 L 508.7 374.8 L 514.9 384.9 L 522.5 400.6 L 529.5 411.7 L 538.5 422.9 L 536.5 424.6 L 536.8 431.2 L 548.5 440.2 L 550.3 442.3 Z"></path>
            <path tabindex="0" aria-label="Morocco" class="home-country home-country--morocco" data-country="morocco" d="M 157.3 309.7 L 161.0 316.1 L 161.6 322.3 L 165.1 332.9 L 167.8 335.0 L 165.9 338.9 L 152.8 340.6 L 148.2 344.4 L 142.4 345.2 L 141.9 352.7 L 130.2 356.7 L 126.3 361.7 L 118.1 364.4 L 108.0 366.0 L 91.8 373.4 L 91.8 385.3 L 90.3 385.3 L 90.5 390.7 L 84.3 391.0 L 81.1 393.3 L 76.5 393.3 L 72.9 392.0 L 64.4 393.1 L 61.1 401.0 L 58.0 401.7 L 53.2 414.4 L 39.2 425.2 L 35.9 439.2 L 31.8 443.7 L 30.6 447.3 L 7.9 448.1 L 8.2 443.4 L 12.1 440.7 L 15.4 435.4 L 14.7 432.0 L 18.2 424.9 L 23.8 418.5 L 27.2 416.9 L 29.8 411.0 L 30.1 405.7 L 33.7 399.4 L 40.4 395.8 L 46.8 385.5 L 52.0 381.5 L 61.4 380.4 L 69.3 373.5 L 74.4 370.8 L 82.8 362.4 L 80.3 349.9 L 84.1 341.2 L 85.5 335.9 L 91.9 329.1 L 102.0 324.5 L 109.5 320.3 L 116.2 309.9 L 119.4 303.7 L 126.8 303.8 L 132.9 308.0 L 142.5 307.4 L 152.9 309.6 L 157.3 309.7 Z"></path>
            <text class="home-map-label-text" x="106.7" y="345.1">MOROCCO</text>
            <path tabindex="0" aria-label="Estonia" class="home-country home-country--estonia" data-country="estonia" d="M 460.8 64.9 L 462.4 66.7 L 455.2 72.5 L 458.2 81.9 L 453.9 85.1 L 445.6 85.1 L 436.9 81.3 L 432.5 80.1 L 423.9 81.9 L 425.1 75.9 L 421.4 77.2 L 415.0 73.6 L 414.1 67.8 L 426.8 65.0 L 439.5 63.6 L 450.5 65.2 L 460.8 64.9 Z"></path>
            <text class="home-map-label-text" x="439.6" y="72.5">ESTONIA</text>
            <path tabindex="0" aria-label="Czechia" class="home-country home-country--czechia" data-country="czechia" d="M 330.3 149.2 L 335.1 152.4 L 342.6 153.3 L 342.0 156.1 L 347.5 158.2 L 349.0 155.6 L 355.9 156.7 L 356.8 159.9 L 364.3 160.5 L 368.9 165.4 L 365.9 165.4 L 364.4 167.2 L 362.1 167.7 L 361.4 170.0 L 359.5 170.4 L 359.2 171.4 L 355.8 172.4 L 351.3 172.3 L 349.9 174.5 L 345.2 172.6 L 340.5 173.1 L 332.7 170.0 L 329.1 170.8 L 323.5 174.9 L 316.0 171.7 L 310.3 167.3 L 305.2 164.9 L 304.1 160.7 L 302.3 157.7 L 309.7 155.5 L 313.4 153.0 L 320.6 151.0 L 323.2 149.1 L 325.8 150.3 L 330.3 149.2 Z"></path>
            <text class="home-map-label-text" x="333.9" y="161.5">CZECHIA</text>
            <path tabindex="0" aria-label="Bulgaria" class="home-country home-country--bulgaria" data-country="bulgaria" d="M 407.2 218.4 L 410.1 222.5 L 414.0 221.8 L 421.8 223.4 L 436.6 223.9 L 441.6 221.3 L 453.4 219.0 L 460.7 222.6 L 466.7 223.7 L 461.4 227.9 L 457.8 235.1 L 461.0 240.8 L 452.3 239.5 L 442.1 242.6 L 442.0 247.7 L 432.8 248.6 L 425.7 245.1 L 417.7 247.9 L 410.2 247.6 L 409.5 240.9 L 404.5 237.7 L 406.1 236.3 L 405.0 235.1 L 406.7 231.8 L 410.5 228.7 L 405.7 224.4 L 404.8 220.7 L 407.2 218.4 Z"></path>
            <text class="home-map-label-text" x="432.4" y="235.8">BULGARIA</text>
            <path tabindex="0" aria-label="Ukraine" class="home-country home-country--ukraine is-active" data-country="ukraine" d="M 499.2 139.2 L 502.9 139.6 L 505.5 137.3 L 508.5 137.8 L 519.0 136.8 L 525.4 142.5 L 522.9 144.6 L 523.7 147.7 L 531.7 148.2 L 535.3 152.6 L 535.1 154.5 L 547.9 158.1 L 555.6 156.5 L 561.8 161.2 L 567.7 161.1 L 582.6 164.4 L 582.7 167.3 L 578.6 172.6 L 580.8 178.1 L 579.2 181.5 L 569.5 182.2 L 564.3 185.1 L 564.0 189.5 L 555.9 190.3 L 549.2 193.6 L 539.8 194.1 L 531.1 197.9 L 531.6 203.3 L 530.1 203.0 L 528.8 201.0 L 525.6 200.6 L 518.4 198.4 L 515.8 200.9 L 514.4 199.8 L 498.7 197.3 L 498.0 193.5 L 488.7 194.7 L 485.0 200.3 L 477.2 207.7 L 472.6 206.0 L 467.9 207.6 L 463.4 205.8 L 465.9 204.7 L 467.7 201.2 L 470.4 198.0 L 469.7 196.2 L 471.8 195.4 L 472.8 196.8 L 478.8 197.1 L 481.4 196.4 L 479.5 195.3 L 480.3 193.8 L 476.7 191.3 L 475.3 187.1 L 471.6 185.4 L 472.3 182.0 L 467.8 179.3 L 463.6 178.9 L 456.2 175.8 L 449.5 176.8 L 447.1 178.3 L 442.9 178.3 L 440.4 180.6 L 432.9 181.6 L 429.5 183.1 L 424.8 180.7 L 418.4 180.6 L 412.1 179.5 L 407.8 181.7 L 407.1 179.0 L 401.5 176.2 L 403.4 172.2 L 406.2 169.6 L 408.4 170.1 L 405.8 165.6 L 415.0 157.2 L 420.0 156.1 L 421.1 153.2 L 416.0 144.5 L 420.8 144.1 L 426.3 141.3 L 434.1 141.1 L 444.3 141.9 L 455.5 144.3 L 463.5 144.5 L 467.3 146.0 L 471.0 144.2 L 473.7 146.6 L 482.8 146.1 L 486.8 147.1 L 487.4 142.0 L 490.5 139.8 L 499.2 139.2 Z"></path>
            <text class="home-map-label-text" x="502.7" y="163.1">UKRAINE</text>
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
