---
date: "2025-08-04"
title: "Contact"
markup: "html"
layout: "profile"
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,600;0,700;1,400&family=Source+Serif+4:wght@300;400;600;700&display=swap');

  :root {
    --contact-ink: #244041;
    --contact-paper: #f5efe6;
    --contact-aged: #d9d8c7;
    --contact-rust: #7b463a;
    --contact-gold: #d2a75f;
    --contact-sage: #5f7f69;
    --contact-muted: #6f7d74;
    --contact-border: #c8bda9;
    --contact-panel: #1f3439;
  }

  .contact-report {
    font-family: 'Source Serif 4', Georgia, serif;
    color: var(--contact-ink);
    font-size: 17px;
    line-height: 1.72;
    margin: -2rem -1rem 0;
  }

  .contact-report p {
    color: var(--contact-ink);
    margin-bottom: 1rem;
  }

  .contact-report section {
    margin-bottom: 3.5rem;
  }

  .contact-report h2 {
    font-family: 'Playfair Display', Georgia, serif;
    font-size: 1.8rem;
    font-weight: 700;
    color: var(--contact-ink);
    margin-bottom: 0.45rem;
    padding-bottom: 0.55rem;
    border-bottom: 2px solid var(--contact-gold);
  }

  .contact-report h3 {
    font-family: 'Playfair Display', Georgia, serif;
    font-size: 1.1rem;
    font-weight: 400;
    font-style: italic;
    color: var(--contact-rust);
    margin: 0 0 0.45rem;
  }

  .contact-report ul {
    margin: 0.7rem 0 0 1.2rem;
    padding: 0;
  }

  .contact-report li {
    margin-bottom: 0.55rem;
  }

  .contact-masthead {
    background:
      linear-gradient(135deg, rgba(31, 52, 57, 0.96), rgba(46, 73, 66, 0.94) 60%, rgba(123, 70, 58, 0.9)),
      var(--contact-panel);
    color: var(--contact-paper);
    padding: 3.1rem 2rem 2.5rem;
    position: relative;
    overflow: hidden;
    margin: 0 -2rem;
  }

  .contact-masthead::before {
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

  .contact-masthead::after {
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

  .contact-masthead-inner {
    position: relative;
    max-width: 860px;
    margin: 0 auto;
    text-align: center;
  }

  .contact-masthead p.contact-masthead-top,
  .contact-masthead p.contact-masthead-sub {
    font-family: 'Source Serif 4', serif;
    font-weight: 700;
    font-size: 0.82rem;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: #fff2d6;
    text-shadow: 0 1px 2px rgba(11, 18, 22, 0.28);
  }

  .contact-masthead-rule {
    width: 72px;
    height: 2px;
    background: var(--contact-gold);
    margin: 1rem auto 1.1rem;
  }

  .contact-masthead h1 {
    font-family: 'Playfair Display', Georgia, serif;
    font-size: clamp(2rem, 4.8vw, 3rem);
    font-weight: 700;
    line-height: 1.12;
    letter-spacing: -0.02em;
    margin: 0 auto 0.85rem;
    max-width: 820px;
    color: var(--contact-paper);
  }

  .contact-masthead .subtitle {
    max-width: 700px;
    margin: 0.9rem auto 0;
    font-size: 1rem;
    color: rgba(245, 239, 230, 0.94);
  }

  .contact-container {
    max-width: 900px;
    margin: 0 auto;
    padding: 3rem 0 1rem;
  }

  .contact-label {
    display: block;
    margin-bottom: 0.55rem;
    font-size: 0.72rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--contact-muted);
    font-family: 'Source Serif 4', serif;
    font-weight: 700;
  }

  .contact-callout {
    border-left: 3px solid var(--contact-rust);
    background: rgba(234, 214, 199, 0.45);
    padding: 1rem 1.2rem;
    margin: 1.5rem 0;
    font-size: 0.95rem;
    color: var(--contact-ink);
  }

  .contact-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 1rem;
    margin-top: 1.5rem;
  }

  .contact-card {
    background: #f6f0e6;
    border: 1px solid var(--contact-border);
    border-top: 3px solid var(--contact-gold);
    padding: 1.05rem 1.15rem;
  }

  .contact-card h3 {
    margin-top: 0;
  }

  .contact-card p:last-child {
    margin-bottom: 0;
  }

  .contact-panel {
    background: #f4eee4;
    border: 1px solid var(--contact-border);
    padding: 1rem 1.1rem;
  }

  .contact-panel h3 {
    margin-top: 0;
  }

  .contact-links {
    display: flex;
    flex-wrap: wrap;
    gap: 0.8rem;
    margin-top: 1.2rem;
  }

  .contact-links a {
    display: inline-block;
    padding: 0.55rem 0.95rem;
    border: 1px solid rgba(36, 64, 65, 0.18);
    text-decoration: none;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    font-size: 0.75rem;
    font-weight: 700;
    color: var(--contact-ink);
  }

  .contact-links a:hover {
    background: rgba(36, 64, 65, 0.06);
  }

  .contact-footer-panel {
    background: var(--contact-panel);
    color: rgba(245, 239, 230, 0.88);
    padding: 2rem;
    margin-top: 2.75rem;
  }

  .contact-footer-panel h2 {
    color: var(--contact-paper);
    border-bottom-color: var(--contact-gold);
  }

  .contact-footer-panel p,
  .contact-footer-panel a {
    color: rgba(245, 239, 230, 0.88);
  }

  .contact-footer-panel .contact-links a {
    border-color: rgba(245, 239, 230, 0.18);
    color: rgba(245, 239, 230, 0.9);
  }

  .contact-footer-panel .contact-links a:hover {
    background: rgba(245, 239, 230, 0.08);
  }

  @media (max-width: 760px) {
    .contact-report {
      margin: -1.5rem 0 0;
    }

    .contact-masthead {
      margin-left: -1rem;
      margin-right: -1rem;
    }
  }
</style>

<div class="contact-report">
  <header class="contact-masthead">
    <div class="contact-masthead-inner">
      <p class="contact-masthead-top">Contact and correspondence</p>
      <div class="contact-masthead-rule"></div>
      <h1>Research contact</h1>
      <div class="contact-masthead-rule"></div>
      <p class="contact-masthead-sub">Food systems, agricultural policy, and Eastern Europe</p>
      <p class="subtitle">I welcome correspondence related to research collaboration, academic events, and policy discussion.</p>
    </div>
  </header>

  <div class="contact-container">
    <section>
      <span class="contact-label">Overview</span>
      <h2>How to reach me</h2>
      <p>I welcome messages from researchers, policy practitioners, journalists, and students who work on food systems, agricultural governance, Eastern Europe, or climate adaptation.</p>
      <div class="contact-callout">
        <strong>Best contact method:</strong> Email remains the most reliable channel for research inquiries, invitations, and requests related to talks or collaboration.
      </div>
      <div class="contact-links">
        <a href="mailto:samsky@utexas.edu">samsky@utexas.edu</a>
        <a href="https://linkedin.com/in/evan-samsky">LinkedIn</a>
        <a href="https://evansamsky.com">Website</a>
      </div>
    </section>

    <section>
      <span class="contact-label">Affiliation</span>
      <h2>Institutional base</h2>
      <div class="contact-grid">
        <div class="contact-card">
          <h3>University of Texas at Austin</h3>
          <p>I am based in the LBJ School of Public Affairs and the Department of Slavic and Eurasian Studies.</p>
        </div>
        <div class="contact-card">
          <h3>Current research areas</h3>
          <p>My current work addresses food systems, agricultural policy, post-Soviet political economy, and the institutional dimensions of climate adaptation.</p>
        </div>
      </div>
    </section>

    <section>
      <span class="contact-label">Topics</span>
      <h2>Common reasons for contact</h2>
      <div class="contact-grid">
        <div class="contact-panel">
          <h3>Research collaboration</h3>
          <p>I welcome inquiries related to collaborative research on agriculture, food security, EU governance, or Eastern European political economy.</p>
        </div>
        <div class="contact-panel">
          <h3>Speaking and events</h3>
          <p>I welcome invitations to conferences, workshops, classrooms, and public discussions that align with my research areas.</p>
        </div>
        <div class="contact-panel">
          <h3>Fieldwork and language exchange</h3>
          <p>I also welcome correspondence on fieldwork methods, language study, and research preparation in the region.</p>
        </div>
      </div>
    </section>

    <section>
      <span class="contact-label">Languages and travel</span>
      <h2>Working languages and regional experience</h2>
      <div class="contact-grid">
        <div class="contact-card">
          <h3>Languages</h3>
          <p>I work in Russian and Arabic at advanced levels. I also use Czech, Ukrainian, French, and Spanish in research settings at varying levels of proficiency.</p>
        </div>
        <div class="contact-card">
          <h3>Field experience</h3>
          <p>I have lived, studied, or conducted research in Ukraine, Morocco, Estonia, Moldova, and Kyrgyzstan. My current research planning also involves Czechia.</p>
        </div>
      </div>
    </section>

    <section class="contact-footer-panel">
      <span class="contact-label">Availability</span>
      <h2>Current correspondence</h2>
      <p>I typically respond to email within one to two business days. If your message concerns a time-sensitive event or deadline, please note that in the subject line.</p>
      <div class="contact-links">
        <a href="mailto:samsky@utexas.edu">Email</a>
        <a href="https://linkedin.com/in/evan-samsky">LinkedIn</a>
      </div>
    </section>
  </div>
</div>
