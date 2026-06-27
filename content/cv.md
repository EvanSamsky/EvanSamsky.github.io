---
title: "CV"
markup: "html"
layout: "profile"
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,600;0,700;1,400&family=Source+Serif+4:wght@300;400;600;700&display=swap');

  :root {
    --cv-ink: #244041;
    --cv-paper: #f5efe6;
    --cv-aged: #d9d8c7;
    --cv-rust: #7b463a;
    --cv-gold: #d2a75f;
    --cv-sage: #5f7f69;
    --cv-muted: #6f7d74;
    --cv-border: #c8bda9;
    --cv-panel: #1f3439;
  }

  .cv-report {
    font-family: 'Source Serif 4', Georgia, serif;
    color: var(--cv-ink);
    font-size: 17px;
    line-height: 1.72;
    margin: -2rem -1rem 0;
  }

  .cv-report p {
    color: var(--cv-ink);
    margin-bottom: 1rem;
  }

  .cv-report section {
    margin-bottom: 3.6rem;
  }

  .cv-report h2 {
    font-family: 'Playfair Display', Georgia, serif;
    font-size: 1.8rem;
    font-weight: 700;
    color: var(--cv-ink);
    margin-bottom: 0.45rem;
    padding-bottom: 0.55rem;
    border-bottom: 2px solid var(--cv-gold);
  }

  .cv-report h3 {
    font-family: 'Playfair Display', Georgia, serif;
    font-size: 1.12rem;
    font-weight: 400;
    font-style: italic;
    color: var(--cv-rust);
    margin: 0 0 0.45rem;
  }

  .cv-report ul {
    margin: 0.7rem 0 0 1.2rem;
    padding: 0;
  }

  .cv-report li {
    margin-bottom: 0.55rem;
  }

  .cv-masthead {
    background:
      linear-gradient(135deg, rgba(31, 52, 57, 0.96), rgba(46, 73, 66, 0.94) 60%, rgba(123, 70, 58, 0.9)),
      var(--cv-panel);
    color: var(--cv-paper);
    padding: 3.1rem 2rem 2.5rem;
    position: relative;
    overflow: hidden;
    margin: 0 -2rem;
  }

  .cv-masthead::before {
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

  .cv-masthead::after {
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

  .cv-masthead-inner {
    position: relative;
    max-width: 900px;
    margin: 0 auto;
    text-align: center;
  }

  .cv-masthead-top,
  .cv-masthead-sub {
    font-family: 'Source Serif 4', serif;
    font-weight: 700;
    font-size: 0.82rem;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: #f3d7d0;
    background: rgba(123, 70, 58, 0.36);
    border: 1px solid rgba(243, 215, 208, 0.16);
    border-radius: 999px;
    display: inline-block;
    padding: 0.16rem 0.62rem;
    text-shadow: none;
  }

  .cv-masthead-rule {
    width: 72px;
    height: 2px;
    background: var(--cv-gold);
    margin: 1rem auto 1.1rem;
  }

  .cv-masthead h1 {
    font-family: 'Playfair Display', Georgia, serif;
    font-size: clamp(2rem, 4.8vw, 3.15rem);
    font-weight: 700;
    line-height: 1.12;
    letter-spacing: -0.02em;
    margin: 0 auto 0.85rem;
    max-width: 860px;
    color: var(--cv-paper);
  }

  .cv-masthead .subtitle {
    max-width: 720px;
    margin: 0.9rem auto 0;
    font-size: 1rem;
    color: rgba(245, 239, 230, 0.94);
  }

  .cv-contact-strip {
    display: flex;
    flex-wrap: wrap;
    gap: 0.8rem 1rem;
    justify-content: center;
    margin-top: 1.1rem;
  }

  .cv-contact-strip a,
  .cv-contact-strip span {
    font-family: 'Source Serif 4', serif;
    font-size: 0.82rem;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: rgba(245, 239, 230, 0.88);
    text-decoration: none;
  }

  .cv-contact-strip a:hover {
    color: var(--cv-paper);
  }

  .cv-container {
    max-width: 900px;
    margin: 0 auto;
    padding: 3rem 0 1rem;
  }

  .cv-label {
    display: block;
    margin-bottom: 0.55rem;
    font-size: 0.72rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--cv-muted);
    font-family: 'Source Serif 4', serif;
    font-weight: 700;
  }

  .cv-callout {
    border-left: 3px solid var(--cv-rust);
    background: rgba(234, 214, 199, 0.45);
    padding: 1rem 1.2rem;
    margin: 1.5rem 0;
    font-size: 0.95rem;
    color: var(--cv-ink);
  }

  .cv-callout strong {
    color: var(--cv-rust);
  }

  .cv-card-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 1rem;
    margin-top: 1.5rem;
  }

  .cv-card {
    background: #f6f0e6;
    border: 1px solid var(--cv-border);
    border-top: 3px solid var(--cv-gold);
    padding: 1.05rem 1.15rem;
  }

  .cv-card-date {
    font-size: 0.8rem;
    font-weight: 700;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--cv-muted);
    margin-bottom: 0.45rem;
  }

  .cv-card h3 {
    margin-top: 0;
  }

  .cv-card p:last-child {
    margin-bottom: 0;
  }

  .cv-entry {
    padding: 1.1rem 0;
    border-bottom: 1px solid var(--cv-border);
  }

  .cv-entry:last-child {
    border-bottom: none;
  }

  .cv-entry-head {
    display: flex;
    justify-content: space-between;
    gap: 1rem;
    align-items: baseline;
    margin-bottom: 0.25rem;
  }

  .cv-entry-title {
    font-family: 'Playfair Display', Georgia, serif;
    font-size: 1.2rem;
    color: var(--cv-ink);
  }

  .cv-entry-date {
    font-size: 0.82rem;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--cv-muted);
    white-space: nowrap;
  }

  .cv-entry-sub {
    color: var(--cv-rust);
    font-style: italic;
    margin-bottom: 0.55rem;
  }

  .cv-two-col {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1.1rem;
  }

  .cv-skill-box,
  .cv-lang-box {
    background: #f4eee4;
    border: 1px solid var(--cv-border);
    padding: 1rem 1.1rem;
  }

  .cv-skill-box h3,
  .cv-lang-box h3 {
    margin-top: 0;
  }

  .cv-biblio {
    list-style: none;
    margin: 1rem 0 0;
    padding: 0;
  }

  .cv-biblio li {
    padding: 0.85rem 0;
    border-bottom: 1px solid var(--cv-border);
    margin: 0;
  }

  .cv-biblio li:last-child {
    border-bottom: none;
  }

  .cv-footer-panel {
    background: var(--cv-panel);
    color: rgba(245, 239, 230, 0.88);
    padding: 2rem;
    margin-top: 2.75rem;
  }

  .cv-footer-panel h2 {
    color: var(--cv-paper);
    border-bottom-color: var(--cv-gold);
  }

  .cv-footer-panel p,
  .cv-footer-panel a {
    color: rgba(245, 239, 230, 0.88);
  }

  .cv-links {
    display: flex;
    flex-wrap: wrap;
    gap: 0.8rem;
    margin-top: 1.2rem;
  }

  .cv-links a {
    display: inline-block;
    padding: 0.55rem 0.95rem;
    border: 1px solid rgba(245, 239, 230, 0.18);
    text-decoration: none;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    font-size: 0.75rem;
    font-weight: 700;
  }

  .cv-links a:hover {
    background: rgba(245, 239, 230, 0.08);
  }

  @media (max-width: 760px) {
    .cv-report {
      margin: -1.5rem 0 0;
    }

    .cv-masthead {
      margin-left: -1rem;
      margin-right: -1rem;
    }

    .cv-entry-head {
      flex-direction: column;
      align-items: flex-start;
    }
  }
</style>

<div class="cv-report">
  <header class="cv-masthead">
    <div class="cv-masthead-inner">
      <p class="cv-masthead-top">Curriculum vitae</p>
      <div class="cv-masthead-rule"></div>
      <h1>Evan Samsky</h1>
      <div class="cv-masthead-rule"></div>
      <p class="cv-masthead-sub">Global Policy Studies and Russian, East European, and Eurasian Studies</p>
      <p class="subtitle">University of Texas at Austin</p>
      <div class="cv-contact-strip">
        <a href="mailto:samsky@utexas.edu">samsky@utexas.edu</a>
        <span>+1 (940) 453-1633</span>
        <a href="https://evansamsky.com">evansamsky.com</a>
        <a href="https://linkedin.com/in/evan-samsky">LinkedIn</a>
      </div>
    </div>
  </header>

  <div class="cv-container">
    <section>
      <span class="cv-label">Overview</span>
      <h2>Current profile</h2>
      <p>I am a master's candidate in Global Policy Studies and Russian, East European, and Eurasian Studies at the University of Texas at Austin. My research addresses food systems, agricultural policy, and institutional capacity in Eastern Europe, with current work focused on Ukraine, Czechia, and regional questions of climate adaptation and reconstruction.</p>
      <div class="cv-callout">
        <strong>Current research focus:</strong> I am conducting thesis research on farmer networks and environmental solutions in EU agricultural governance while preparing for fieldwork in Czechia.
      </div>
    </section>

    <section>
      <span class="cv-label">Earned degrees</span>
      <h2>Education</h2>
      <div class="cv-card-grid">
        <div class="cv-card">
          <div class="cv-card-date">August 2026, anticipated</div>
          <h3>Master of Arts in Global Policy Studies</h3>
          <p>The University of Texas at Austin, LBJ School of Public Affairs.</p>
          <p>I hold a 3.93 GPA. My thesis is titled "Bridging Policy and Practice: Farmer Networks and Environmental Solutions in EU Agricultural Governance." My advisors are Mary Neuburger and Raj Patel.</p>
        </div>
        <div class="cv-card">
          <div class="cv-card-date">August 2026, anticipated</div>
          <h3>Master of Arts in Russian, East European, and Eurasian Studies</h3>
          <p>The University of Texas at Austin, Department of Slavic and Eurasian Studies.</p>
        </div>
        <div class="cv-card">
          <div class="cv-card-date">May 2022</div>
          <h3>Bachelor of Science and Arts in Biology with Honors</h3>
          <p>The University of Texas at Austin, College of Natural Sciences. I graduated through the Polymathic Scholars Honors Program with a 3.68 GPA.</p>
          <p>My honors thesis examined the Soviet stolovaya as a system of public food aid before and after 1991.</p>
        </div>
        <div class="cv-card">
          <div class="cv-card-date">May 2022</div>
          <h3>Bachelor of Arts in Middle Eastern Languages and Culture</h3>
          <p>The University of Texas at Austin, College of Liberal Arts.</p>
          <p>My capstone analyzed the food system of Bahrain.</p>
        </div>
      </div>
    </section>

    <section>
      <span class="cv-label">Research and employment</span>
      <h2>Selected experience</h2>

      <div class="cv-entry">
        <div class="cv-entry-head">
          <div class="cv-entry-title">Visiting Researcher</div>
          <div class="cv-entry-date">January 2025 to August 2026</div>
        </div>
        <div class="cv-entry-sub">Czech University of Life Sciences</div>
        <p>I am conducting thesis research on farmer networks and environmental solutions in EU agricultural governance. I am working with Mary Neuburger, Raj Patel, and local advisor Lukas Zagata.</p>
      </div>

      <div class="cv-entry">
        <div class="cv-entry-head">
          <div class="cv-entry-title">Research Fellow and Coauthor</div>
          <div class="cv-entry-date">May 2025 to August 2025</div>
        </div>
        <div class="cv-entry-sub">The University of Texas at Austin, with Mary Neuburger</div>
        <ul>
          <li>I conducted archival research with Bulgarian National Statistical Institute materials in multiple languages.</li>
          <li>I analyzed agricultural data from 1944 through 1989, including wheat yields, fertilizer production, and consumption patterns.</li>
          <li>I contributed to coauthored articles on agricultural transformation and environmental politics in Eastern Europe.</li>
        </ul>
      </div>

      <div class="cv-entry">
        <div class="cv-entry-head">
          <div class="cv-entry-title">Policy Research Project Researcher</div>
          <div class="cv-entry-date">January 2025 to July 2025</div>
        </div>
        <div class="cv-entry-sub">Systems Approach to Climate Adaptation Policy in Ukraine</div>
        <ul>
          <li>I applied fuzzy cognitive mapping and systems thinking methods to climate adaptation questions in Ukrainian agriculture.</li>
          <li>I developed risk reduction frameworks that connected Ukrainian institutional capacity to EU Common Agricultural Policy alignment.</li>
          <li>I collaborated with Polissia National University and the U.S. Department of the Interior International Technical Assistance Program.</li>
        </ul>
      </div>

      <div class="cv-entry">
        <div class="cv-entry-head">
          <div class="cv-entry-title">Policy Research Project Researcher</div>
          <div class="cv-entry-date">August 2024 to May 2025</div>
        </div>
        <div class="cv-entry-sub">Tracking Global Development Finance, with Publish What You Fund</div>
        <ul>
          <li>I conducted transparency assessments for development finance institutions across sovereign and non-sovereign portfolios.</li>
          <li>I analyzed transparency practices used in the 2025 DFI Transparency Index across core information, impact management, ESG and accountability, and financial information.</li>
        </ul>
      </div>

      <div class="cv-entry">
        <div class="cv-entry-head">
          <div class="cv-entry-title">Policy Researcher</div>
          <div class="cv-entry-date">May 2024 to August 2024</div>
        </div>
        <div class="cv-entry-sub">U.S. Department of the Interior</div>
        <p>I conducted mixed-methods research on Ukrainian agriculture and environmental resilience for U.S. and Ukrainian government audiences. I produced briefing materials on food security, agricultural recovery, and environmental sustainability in conflict-affected regions.</p>
      </div>

      <div class="cv-entry">
        <div class="cv-entry-head">
          <div class="cv-entry-title">Earlier experience</div>
          <div class="cv-entry-date">2018 to 2023</div>
        </div>
        <div class="cv-entry-sub">Selected appointments</div>
        <p>I worked as a project manager at Epic Systems, an agricultural volunteer in Meknes, Morocco, and an undergraduate research assistant in the Chen Laboratory at UT Austin, where I conducted plant genomics and epigenetics research for three years.</p>
      </div>
    </section>

    <section>
      <span class="cv-label">Fellowships and awards</span>
      <h2>Selected funding and recognition</h2>
      <div class="cv-card-grid">
        <div class="cv-card">
          <div class="cv-card-date">Spring 2026</div>
          <h3>Czech Studies Endowment Scholarship</h3>
          <p>This award funded on-site thesis research in the Czech Republic. The award amount was $11,500.</p>
        </div>
        <div class="cv-card">
          <div class="cv-card-date">2025</div>
          <h3>Graduate School Summer Excellence Fellowship and FLAS Czech Fellowship</h3>
          <p>I received a UT Austin Summer Excellence Fellowship and a FLAS Graduate Fellowship for Czech language study at Indiana University.</p>
        </div>
        <div class="cv-card">
          <div class="cv-card-date">2024 to 2025</div>
          <h3>FLAS Graduate Fellowship in Ukrainian</h3>
          <p>I studied Ukrainian in residence at UT Austin and conducted independent research with support totaling $38,000.</p>
        </div>
        <div class="cv-card">
          <div class="cv-card-date">2025</div>
          <h3>Fulbright Study and Research Grant Semifinalist</h3>
          <p>I proposed a mixed-methods project on Polish farmers' perspectives on sustainable agriculture policy under the Common Agricultural Policy 2023-27.</p>
        </div>
      </div>
    </section>

    <section>
      <span class="cv-label">Publications</span>
      <h2>Selected publications and reports</h2>
      <ul class="cv-biblio">
        <li>Neuburger, Mary, and Evan Samsky. "Bulgaria's Green Revolutions?: Agricultural Transformation, Environmental Politics, and the Cold War 1960-1989." Under review.</li>
        <li>Simanovskyy, Mykhaylo, Volodymyr Kulikov, Nicholas Pierce, and Evan Samsky. "Narrative Warfare: Food Insecurity in the Russia-Ukraine War." <em>RIDL</em>, May 23, 2024.</li>
        <li>Shah, Sachin D., Vitalii Dankevych, Marina L. Tomer, et al. "Climate Risk Reduction for Ukraine's Food Security: A Policy Blueprint for European Union Integration." Policy Research Project, LBJ School of Public Affairs, 2025.</li>
        <li>James, Paul, Ryan Anderton, and Ella Remande-Guyard. "DFI Transparency Index 2025: Ranking the World's Leading Development Finance Institutions." Publish What You Fund, 2025. I contributed research support under the supervision of Catherine Weaver.</li>
        <li>Samsky, Evan. "Institutional Capacity for Climate Action in Ukraine's Agricultural Sector: A General Assessment." U.S. Department of the Interior, 2024.</li>
      </ul>
    </section>

    <section>
      <span class="cv-label">Presentations and teaching</span>
      <h2>Selected academic activity</h2>
      <div class="cv-two-col">
        <div class="cv-skill-box">
          <h3>Presentations</h3>
          <ul>
            <li>I presented "Russian Arteries of Influence: Eastern Europe, Bulgaria, and the Power of Oil and Gas" with Mary Neuburger and Cole Smith at the University of Texas at Austin in April 2026.</li>
            <li>I presented "CAP Funding Mechanisms for Ukrainian EU Accession" with Annabelle Sala in Warsaw in July 2025.</li>
            <li>I presented "Strengthening Institutional Implementation Processes" at the LBJ School of Public Affairs in May 2025.</li>
            <li>I presented work in Arabic at the Arabic Language Flagship Capstone Student Panel in Fès in March 2022.</li>
          </ul>
        </div>
        <div class="cv-skill-box">
          <h3>Teaching</h3>
          <ul>
            <li>I served as a graduate teaching assistant for Political Ideologies and Manifestos in Fall 2025.</li>
            <li>I led three weekly discussion sections for Hidden Lives of Maps in Spring 2025.</li>
            <li>I served as a graduate teaching assistant for Intelligence and Espionage in the Eastern Bloc in Fall 2024.</li>
            <li>I served as resident director for American Councils programs in Narva during the summers of 2022 and 2023.</li>
          </ul>
        </div>
      </div>
    </section>

    <section>
      <span class="cv-label">Skills</span>
      <h2>Methods, languages, and service</h2>
      <div class="cv-two-col">
        <div class="cv-skill-box">
          <h3>Technical and research methods</h3>
          <ul>
            <li>I use Python, including Pandas, NumPy, scikit-learn, natural language processing tools, and web scraping workflows.</li>
            <li>I use R for statistical modeling, econometric analysis, and data visualization.</li>
            <li>I work with SQL, ArcGIS Pro, MAXQDA, computational text analysis, survey design, and mixed-methods research design.</li>
            <li>I also have laboratory experience in PCR, DNA and RNA extraction, fluorescence microscopy, and ImageJ analysis.</li>
          </ul>
        </div>
        <div class="cv-lang-box">
          <h3>Languages and service</h3>
          <ul>
            <li>I hold ACTFL-certified Advanced Low proficiency in Russian and Advanced Mid proficiency in Arabic.</li>
            <li>I hold ACTFL-certified Intermediate High proficiency in Czech, and I use Ukrainian at an intermediate level.</li>
            <li>I serve as an associate editor for <em>Constitutional Studies: A Global Comparative Journal</em>.</li>
            <li>I have also served as an Arabic tutor and as a judge for the Olympiada of Spoken Russian at UT Austin.</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="cv-footer-panel">
      <span class="cv-label">Full record</span>
      <h2>Download the current PDF CV</h2>
      <p>The PDF version remains the most complete version of the record and includes the full conference list, earlier fellowships, and detailed technical skills.</p>
      <div class="cv-links">
        <a href="/files/Evan_Samsky_CV.pdf" target="_blank">Download PDF</a>
        <a href="mailto:samsky@utexas.edu">Email</a>
        <a href="https://linkedin.com/in/evan-samsky">LinkedIn</a>
      </div>
    </section>
  </div>
</div>
