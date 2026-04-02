---
title: "CV"
markup: "html"
---

<style>
/* ─── Reset & Base ─────────────────────────────────────────── */
*, *::before, *::after { box-sizing: border-box; }

.cv-wrap {
    max-width: 860px;
    margin: 0 auto;
    padding: 0 0 60px;
    font-family: 'Georgia', 'Times New Roman', serif;
    color: #4B3034;
    line-height: 1.6;
}

/* ─── Header ───────────────────────────────────────────────── */
.cv-header {
    padding: 32px 0 24px;
    border-bottom: 2px solid #2D4739;
    margin-bottom: 36px;
}

.cv-name {
    font-size: 2.2em;
    font-weight: bold;
    color: #160F29;
    letter-spacing: -0.5px;
    margin-bottom: 6px;
    line-height: 1.1;
}

.cv-title {
    font-size: 0.95em;
    color: #4B3034;
    font-style: italic;
    margin-bottom: 2px;
    line-height: 1.5;
}

.cv-contact {
    margin-top: 14px;
    font-size: 0.85em;
    color: #4B3034;
    display: flex;
    flex-wrap: wrap;
    gap: 6px 0;
    align-items: center;
}

.cv-contact a {
    color: #2D4739;
    text-decoration: none;
    border-bottom: 1px solid #CBD7C1;
    transition: border-color 0.15s;
}

.cv-contact a:hover {
    border-bottom-color: #2D4739;
}

.cv-contact-sep {
    margin: 0 10px;
    color: #CBD7C1;
}

/* ─── Sections ─────────────────────────────────────────────── */
.cv-section {
    margin-bottom: 36px;
}

.cv-section-title {
    font-size: 0.72em;
    font-weight: bold;
    color: #2D4739;
    letter-spacing: 0.13em;
    text-transform: uppercase;
    padding-bottom: 8px;
    border-bottom: 1.5px solid #2D4739;
    margin-bottom: 22px;
}

/* ─── Items ────────────────────────────────────────────────── */
.cv-item {
    padding: 16px 0;
    border-bottom: 1px solid #CBD7C1;
}

.cv-item:last-child {
    border-bottom: none;
    padding-bottom: 0;
}

.cv-item-header {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    gap: 16px;
    margin-bottom: 2px;
}

.cv-item-title {
    font-size: 0.97em;
    font-weight: bold;
    color: #160F29;
    flex: 1;
    line-height: 1.4;
}

.cv-item-date {
    font-size: 0.8em;
    color: #4B3034;
    white-space: nowrap;
    flex-shrink: 0;
    font-style: italic;
}

.cv-item-subtitle {
    font-size: 0.88em;
    color: #4B3034;
    font-style: italic;
    margin-bottom: 7px;
}

.cv-item-body {
    font-size: 0.88em;
    color: #4B3034;
    line-height: 1.65;
    margin-top: 6px;
}

.cv-item-body strong {
    color: #160F29;
    font-weight: bold;
}

.cv-item-body ul {
    margin: 6px 0 0 18px;
    padding: 0;
}

.cv-item-body ul li {
    margin-bottom: 4px;
}

/* ─── Publication list ─────────────────────────────────────── */
.cv-pub-list {
    list-style: none;
    padding: 0;
    margin: 0;
}

.cv-pub-list li {
    font-size: 0.88em;
    color: #4B3034;
    padding: 10px 0;
    border-bottom: 1px solid #CBD7C1;
    line-height: 1.6;
}

.cv-pub-list li:last-child {
    border-bottom: none;
}

.cv-pub-list .pub-sub {
    font-size: 0.88em;
    color: #2D4739;
    font-style: italic;
    display: block;
    margin-top: 3px;
}

.cv-pub-subhead {
    font-size: 0.78em;
    font-weight: bold;
    color: #4B3034;
    text-transform: uppercase;
    letter-spacing: 0.07em;
    margin: 18px 0 8px;
}

.cv-pub-subhead:first-child {
    margin-top: 0;
}

/* ─── Conference list ──────────────────────────────────────── */
.cv-conf-list {
    list-style: none;
    padding: 0;
    margin: 0;
}

.cv-conf-list li {
    font-size: 0.88em;
    color: #4B3034;
    padding: 7px 0;
    border-bottom: 1px solid #CBD7C1;
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    gap: 14px;
    flex-wrap: wrap;
    line-height: 1.5;
}

.cv-conf-list li:last-child {
    border-bottom: none;
}

.cv-conf-list .conf-date {
    font-size: 0.82em;
    font-style: italic;
    white-space: nowrap;
    flex-shrink: 0;
    color: #4B3034;
}

.cv-conf-list .conf-note {
    font-style: italic;
    color: #2D4739;
    font-size: 0.9em;
}

/* ─── Skills grid ──────────────────────────────────────────── */
.cv-skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(195px, 1fr));
    gap: 22px;
}

.cv-skill-cat h4 {
    font-size: 0.78em;
    font-weight: bold;
    color: #2D4739;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    margin-bottom: 10px;
    padding-bottom: 4px;
    border-bottom: 1px solid #CBD7C1;
}

.cv-skill-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 5px;
}

.cv-skill-tag {
    background: #CBD7C1;
    color: #2D4739;
    padding: 3px 9px;
    font-size: 0.8em;
    letter-spacing: 0.02em;
    display: inline-block;
}

/* ─── Languages ────────────────────────────────────────────── */
.cv-lang-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(165px, 1fr));
    gap: 1px;
    background: #CBD7C1;
    border: 1px solid #CBD7C1;
    margin-bottom: 20px;
}

.cv-lang-item {
    background: #faf9f7;
    padding: 10px 14px;
}

.cv-lang-name {
    font-size: 0.9em;
    font-weight: bold;
    color: #160F29;
    display: block;
}

.cv-lang-level {
    font-size: 0.78em;
    color: #2D4739;
    display: block;
    margin-top: 1px;
}

.cv-lang-note {
    font-size: 0.76em;
    color: #4B3034;
    font-style: italic;
    display: block;
    margin-top: 2px;
}

/* ─── Download ─────────────────────────────────────────────── */
.cv-download {
    margin-top: 48px;
    padding-top: 24px;
    border-top: 1.5px solid #2D4739;
    display: flex;
    align-items: center;
    gap: 20px;
}

.cv-download-label {
    font-size: 0.8em;
    color: #4B3034;
    text-transform: uppercase;
    letter-spacing: 0.1em;
}

.cv-download-btn {
    display: inline-block;
    background: #2D4739;
    color: #CBD7C1;
    padding: 9px 22px;
    text-decoration: none;
    font-size: 0.82em;
    letter-spacing: 0.09em;
    text-transform: uppercase;
    transition: background 0.2s, color 0.2s;
}

.cv-download-btn:hover {
    background: #160F29;
    color: #E3BCB5;
}

/* ─── Responsive ───────────────────────────────────────────── */
@media (max-width: 600px) {
    .cv-name { font-size: 1.7em; }

    .cv-item-header { flex-direction: column; gap: 1px; }

    .cv-contact { flex-direction: column; }
    .cv-contact-sep { display: none; }

    .cv-lang-grid { grid-template-columns: 1fr 1fr; }

    .cv-conf-list li { flex-direction: column; gap: 2px; }
}
</style>

<div class="cv-wrap">

  <header class="cv-header">
    <h1 class="cv-name">Evan Samsky</h1>
    <p class="cv-title">Dual MA Candidate — Global Policy Studies &amp; Russian, East European, and Eurasian Studies</p>
    <p class="cv-title">The University of Texas at Austin</p>
    <div class="cv-contact">
      <a href="https://linkedin.com/in/evan-samsky" target="_blank">LinkedIn</a>
      <span class="cv-contact-sep">·</span>
      <a href="https://evansamsky.github.io" target="_blank">evansamsky.github.io</a>
    </div>
  </header>

  <!-- EDUCATION -->
  <section class="cv-section">
    <h2 class="cv-section-title">Education</h2>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Master of Arts in Global Policy Studies</div>
        <div class="cv-item-date">Anticipated August 2026</div>
      </div>
      <div class="cv-item-subtitle">The University of Texas at Austin, LBJ School of Public Affairs · GPA 3.93/4.0</div>
      <div class="cv-item-body">
        <em>Thesis:</em> "Bridging Policy and Practice: Farmer Networks and Environmental Solutions in EU Agricultural Governance"<br>
        <em>Advisors:</em> Dr. Mary Neuburger (History) and Dr. Raj Patel (Sociology, LBJ School)<br><br>
        <strong>Selected Coursework:</strong> World Food System 1450–2050 (Dr. Raj Patel) · International Economics (Dr. James Galbraith) · Analytical Methods for Policy Studies · Research Methods in Social Science and Humanities · Systems Approach to Climate Adaptation · European Union in the World
      </div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Master of Arts in Russian, East European, and Eurasian Studies</div>
        <div class="cv-item-date">Anticipated August 2026</div>
      </div>
      <div class="cv-item-subtitle">The University of Texas at Austin, Department of Slavic and Eurasian Studies</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Bachelor of Science and Arts in Biology with Honors</div>
        <div class="cv-item-date">May 2022</div>
      </div>
      <div class="cv-item-subtitle">The University of Texas at Austin, College of Natural Sciences · Polymathic Scholars Honors Program · GPA 3.68/4.0</div>
      <div class="cv-item-body">
        <em>Honors Thesis:</em> "The Soviet Stolovaya and 1991: A Culture of Food Aid Before and After the USSR"
      </div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Bachelor of Arts in Middle Eastern Languages and Culture (Arabic)</div>
        <div class="cv-item-date">May 2022</div>
      </div>
      <div class="cv-item-subtitle">The University of Texas at Austin, College of Liberal Arts</div>
      <div class="cv-item-body">
        <em>Capstone:</em> "The Food System of Bahrain: Analyzing Risks and Possibilities"
      </div>
    </div>
  </section>

  <!-- FELLOWSHIPS, HONORS & AWARDS -->
  <section class="cv-section">
    <h2 class="cv-section-title">Fellowships, Honors &amp; Awards</h2>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Czech Studies Endowment Scholarship</div>
        <div class="cv-item-date">Spring 2026 · $11,500</div>
      </div>
      <div class="cv-item-body">Funded on-site thesis research in the Czech Republic.</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">UT Austin Graduate School Summer Excellence Fellowship</div>
        <div class="cv-item-date">Summer 2025 · $9,000</div>
      </div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">FLAS Graduate Fellowship — Czech Language</div>
        <div class="cv-item-date">Summer 2025 · $7,500</div>
      </div>
      <div class="cv-item-subtitle">Indiana University Summer Language Workshop</div>
      <div class="cv-item-body">Intensive Czech study and independent research in preparation for thesis fieldwork in Czechia.</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">FLAS Graduate Fellowship — Ukrainian Language</div>
        <div class="cv-item-date">Academic Year 2024–2025 · $38,000</div>
      </div>
      <div class="cv-item-subtitle">University of Texas at Austin</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Fulbright Study/Research Grant — Semifinalist</div>
        <div class="cv-item-date">2025</div>
      </div>
      <div class="cv-item-body">
        Proposed research: "Bridging the Gap: Polish Farmers' Perspectives on Sustainable Agriculture Policy" — mixed-methods analysis of EU Common Agricultural Policy (CAP) 2023–27 implementation challenges, examining farmer responses to climate-smart agriculture incentives.
      </div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">FLAS Graduate Fellowship — Russian Language</div>
        <div class="cv-item-date">Academic Year 2023–2024 · $38,000</div>
      </div>
      <div class="cv-item-subtitle">University of Texas at Austin</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Polymathic Scholars Honors Program</div>
        <div class="cv-item-date">2017–2022</div>
      </div>
      <div class="cv-item-subtitle">The University of Texas at Austin</div>
      <div class="cv-item-body">Distinguished honors program focused on interdisciplinary research and applications of STEM outside standard contexts, requiring honors-level coursework, ongoing interdisciplinary seminars, an honors thesis, and strict GPA requirements.</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Boren Scholarship — Arabic Language</div>
        <div class="cv-item-date">Academic Year 2021–2022 · $25,000</div>
      </div>
      <div class="cv-item-subtitle">National Security Education Program, U.S. Department of Defense</div>
      <div class="cv-item-body">Studied Arabic (Modern Standard, Moroccan dialect, Levantine dialect) in Morocco through the Arabic Flagship Capstone Year Program.</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">FLAS Scholarship — Russian Language</div>
        <div class="cv-item-date">Summer 2020 · $7,500</div>
      </div>
      <div class="cv-item-subtitle">Indiana University Summer Language Workshop</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">FLAS Scholarship — Russian Language</div>
        <div class="cv-item-date">Summer 2018 · $7,500</div>
      </div>
      <div class="cv-item-subtitle">Bishkek, Kyrgyzstan</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">National Security Language Initiative for Youth Scholarship — Russian</div>
        <div class="cv-item-date">Academic Year 2016–2017 · ~$40,000</div>
      </div>
      <div class="cv-item-subtitle">U.S. Department of State · Chișinău, Moldova</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">National Security Language Initiative for Youth Scholarship — Arabic</div>
        <div class="cv-item-date">Summer 2015 · ~$10,000</div>
      </div>
      <div class="cv-item-subtitle">U.S. Department of State · Qalam wa Lawh Center for Arabic, Rabat, Morocco</div>
    </div>
  </section>

  <!-- RESEARCH EXPERIENCE & EMPLOYMENT -->
  <section class="cv-section">
    <h2 class="cv-section-title">Research Experience &amp; Selected Employment</h2>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Thesis Researcher</div>
        <div class="cv-item-date">January 2025 – August 2026</div>
      </div>
      <div class="cv-item-subtitle">Czech University of Life Sciences (Česká zemědělská univerzita v Praze)</div>
      <div class="cv-item-body">
        Thesis: "Bridging Policy and Practice: Farmer Networks and Environmental Solutions in EU Agricultural Governance"<br>
        <em>Advisors:</em> Dr. Mary Neuburger, Dr. Raj Patel &nbsp;·&nbsp; <em>Local Advisor:</em> Dr. Lukas Zagat
      </div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Research Fellow / Co-Author</div>
        <div class="cv-item-date">May – August 2025</div>
      </div>
      <div class="cv-item-subtitle">The University of Texas at Austin · Supervisor: Dr. Mary Neuburger</div>
      <div class="cv-item-body">
        <ul>
          <li>Conducted archival research with Bulgarian National Statistical Institute materials in multiple languages</li>
          <li>Analyzed quantitative agricultural data spanning 1944–1989, including wheat yields, fertilizer production, and consumption patterns</li>
          <li>Integrated historical methodology with data analysis to examine Cold War-era agricultural transformation and environmental politics</li>
          <li>Co-authored academic articles on Soviet-led agricultural modernization and environmental backlash in Eastern Europe</li>
        </ul>
      </div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Course Term Paper: "Detecting Policy Divergence Through Computational Methods: A Mixed-Method Analysis of GM Crop Regulation in EU Development"</div>
        <div class="cv-item-date">Spring 2025</div>
      </div>
      <div class="cv-item-body">
        <ul>
          <li>Employed Latent Dirichlet Allocation (LDA) topic modeling and Large Language Model analysis to examine several hundred EU development aid project documents collected via the IATI database</li>
          <li>Used Python (scikit-learn, NLP) for text analysis and computational pattern detection</li>
          <li>Identified likely policy divergence between EU institutions and member states regarding agricultural biotechnology approaches in international development projects</li>
        </ul>
      </div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Course Term Paper: "Rethinking Agricultural Innovation: A Contextualized Evaluation of Seed Systems in Smallholders in Sub-Saharan Africa"</div>
        <div class="cv-item-date">Spring 2025</div>
      </div>
      <div class="cv-item-body">
        <ul>
          <li>Designed a 9-year randomized controlled trial comparing GM cowpea, hybrid varieties, landraces, and farmer-saved seeds across African contexts with econometric methods</li>
          <li>Integrated agronomic, economic, environmental, and behavioral factors to analyze farmer decision-making under technological transitions</li>
        </ul>
      </div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Policy Research Project (PRP) Researcher — Systems Approach to Climate Adaptation Policy in Ukraine</div>
        <div class="cv-item-date">January – July 2025</div>
      </div>
      <div class="cv-item-subtitle">The University of Texas at Austin · Supervisor: Mr. Sachin Shah, U.S. Geological Survey</div>
      <div class="cv-item-body">
        <ul>
          <li>Applied fuzzy cognitive mapping (FCM) and systems thinking methodologies to analyze climate adaptation strategies for Ukrainian agriculture</li>
          <li>Developed risk reduction frameworks integrating EU Common Agricultural Policy alignment with Ukrainian institutional capacity</li>
          <li>Collaborated with Polissia National University (Ukraine) and U.S. Department of Interior International Technical Assistance Program (DOI-ITAP)</li>
          <li>Conducted climate vulnerability assessments and barrier analysis for agricultural adaptation measures</li>
          <li>Led research efforts to analyze climate adaptive institutional options for Ukraine under initial oversight of USAID</li>
        </ul>
      </div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Policy Research Project (PRP) Researcher — Tracking Global Development Finance</div>
        <div class="cv-item-date">August 2024 – May 2025</div>
      </div>
      <div class="cv-item-subtitle">The University of Texas at Austin / Publish What You Fund · Supervisor: Dr. Catherine Weaver</div>
      <div class="cv-item-body">
        <ul>
          <li>Conducted primary data collection and transparency assessments for Development Finance Institutions (DFIs) across multiple sovereign and non-sovereign institutions</li>
          <li>Performed systematic coding and analysis of institutional transparency practices for the 2025 DFI Transparency Index across four components: core information, impact management, ESG &amp; accountability, and financial information</li>
          <li>Collaborated directly with CEO Gary Forster and Research Manager Paul James</li>
          <li>Analyzed development finance landscape trends and private capital mobilization strategies</li>
        </ul>
      </div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Course Term Paper: "Who Belongs? New Perspectives for Rusyn Minorities in the Ukrainian National Project"</div>
        <div class="cv-item-date">Fall 2024</div>
      </div>
      <div class="cv-item-body">
        Applied nationalism theory and conducted primary interviews to analyze minority integration in multi-ethnic states; examined institutional responses and social dynamics in communities facing political and economic transitions.
      </div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Policy Researcher</div>
        <div class="cv-item-date">May – August 2024</div>
      </div>
      <div class="cv-item-subtitle">U.S. Department of the Interior</div>
      <div class="cv-item-body">
        <ul>
          <li>Conducted mixed-methods research on Ukrainian agriculture and environmental resilience for U.S. and Ukrainian government officials</li>
          <li>Synthesized primary and secondary sources to assess agricultural recovery strategies in conflict-affected regions</li>
          <li>Produced policy briefing materials examining intersections of food security, environmental sustainability, and geopolitical stability</li>
        </ul>
      </div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Project Manager</div>
        <div class="cv-item-date">September 2022 – May 2023</div>
      </div>
      <div class="cv-item-subtitle">Epic Systems Corporation</div>
      <div class="cv-item-body">Oversaw healthcare IT implementation timelines and compliance for U.S. hospitals, with experience in revenue cycle and electronic medical claims.</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Agricultural Volunteer</div>
        <div class="cv-item-date">January – May 2022</div>
      </div>
      <div class="cv-item-subtitle">Coopérative Meknassate Azaytoune · Meknes, Morocco</div>
      <div class="cv-item-body">
        <ul>
          <li>Assisted in land improvement and irrigation infrastructure installation on a 2-hectare cooperative farm</li>
          <li>Conducted maintenance and repair of agricultural equipment</li>
          <li>Assessed and treated olive and apricot trees for fungal diseases and pests</li>
        </ul>
      </div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Undergraduate Research Assistant</div>
        <div class="cv-item-date">September 2018 – May 2021</div>
      </div>
      <div class="cv-item-subtitle">Chen Laboratory, Department of Molecular Biosciences · The University of Texas at Austin</div>
      <div class="cv-item-body">
        <ul>
          <li>Three years of molecular biology research on plant genomics and epigenetics under Dr. Jeffrey Chen and Dr. Xiaoya Song</li>
          <li>Performed laboratory techniques including PCR, flower dissection, GFP microscopy, DNA/RNA extraction and genotyping, bacterial and plant transformation</li>
          <li>Maintained greenhouse facilities; supported postdoctoral researchers in experimental design and data collection</li>
          <li>Utilized R programming for statistical analysis, data visualization, and interpretation of genomic datasets</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- PUBLICATIONS -->
  <section class="cv-section">
    <h2 class="cv-section-title">Publications</h2>

    <p class="cv-pub-subhead">Peer-Reviewed Articles (Under Review)</p>
    <ul class="cv-pub-list">
      <li>
        Neuburger, Mary and Evan Samsky. "Bulgaria's Green Revolutions?: Agricultural Transformation, Environmental Politics, and the Cold War 1960–1989." <em>[Under review]</em>
      </li>
    </ul>

    <p class="cv-pub-subhead">Articles in Preparation</p>
    <ul class="cv-pub-list">
      <li>
        Song, Xiaoya, et al. "The Central Cell Is Essential for Maintaining Female Gametophyte Cell Fates via CRP Signaling." <em>[In preparation]</em>
        <span class="pub-sub">Contributing author: genotyping, microscopic phenotyping, ImageJ analysis, microscopy imaging</span>
      </li>
      <li>Two additional articles with Dr. Mary Neuburger <em>[in preparation]</em></li>
    </ul>

    <p class="cv-pub-subhead">Policy Analysis &amp; Commentary</p>
    <ul class="cv-pub-list">
      <li>
        Simanovskyy, Mykhaylo, Volodymyr Kulikov, Nicholas Pierce, and Evan Samsky. "Narrative Warfare: Food Insecurity in the Russia–Ukraine War." <em>RIDL (Research, Innovation, and Discourse Launchpad)</em>, May 23, 2024.
      </li>
    </ul>

    <p class="cv-pub-subhead">Policy Reports &amp; Government Publications</p>
    <ul class="cv-pub-list">
      <li>
        Shah, Sachin D., Vitalii Dankevych, Marina L. Tomer, et al. "Climate Risk Reduction for Ukraine's Food Security: A Policy Blueprint for European Union Integration." Policy Research Project, LBJ School of Public Affairs, University of Texas at Austin, June 2025.
      </li>
      <li>
        James, Paul, Ryan Anderton, and Ella Remande-Guyard. "DFI Transparency Index 2025: Ranking the World's Leading Development Finance Institutions." Publish What You Fund, 2025.
        <span class="pub-sub">Research support contributor under supervision of Dr. Catherine Weaver</span>
      </li>
      <li>Samsky, Evan. "Learning from CEE Agricultural Integration for Ukraine's EU Accession." <em>[forthcoming]</em></li>
      <li>Samsky, Evan. "Institutional Capacity for Climate Action in Ukraine's Agricultural Sector: A General Assessment." U.S. Department of the Interior, 2024.</li>
      <li>Contributing author, policy white paper from "A Blueprint for Ukraine's European Union Integration: Creating Risk Reduction and Climate Adaptation Strategies in the Agriculture Sector" workshop (Warsaw, July 2025, forthcoming).</li>
    </ul>
  </section>

  <!-- PRESENTATIONS -->
  <section class="cv-section">
    <h2 class="cv-section-title">Presentations</h2>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">"CAP Funding Mechanisms for Ukrainian EU Accession"</div>
        <div class="cv-item-date">July 2025</div>
      </div>
      <div class="cv-item-subtitle">With Annabelle Sala · A Blueprint for Ukraine's European Union Integration: Creating Risk Reduction and Climate Adaptation Strategies in the Agriculture Sector · Polish Academy of Sciences, Warsaw, Poland, July 1–3, 2025</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">"Strengthening Institutional Implementation Processes"</div>
        <div class="cv-item-date">May 2025</div>
      </div>
      <div class="cv-item-subtitle">Policy Research Project: Ukraine Agricultural Restoration and Food Security · LBJ School of Public Affairs, UT Austin, May 1, 2025</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">"History of the City of Alexandria" (in Arabic)</div>
        <div class="cv-item-date">March 2022</div>
      </div>
      <div class="cv-item-subtitle">Arabic Language Flagship Capstone Student Panel · University Sidi Mohammed Ben Abdellah, Fès, Morocco, March 18, 2022</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">"The Soviet Stolovaya and 1991: A Culture of Food Assistance During and After the USSR"</div>
        <div class="cv-item-date">2021</div>
      </div>
      <div class="cv-item-subtitle">Longhorn Research Poster Session · University of Texas at Austin, 2021 <em>(Honorable Mention)</em></div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">"Food Production and Trade in Bahrain"</div>
        <div class="cv-item-date">May 2020</div>
      </div>
      <div class="cv-item-subtitle">Middle Eastern Languages &amp; Culture Capstone Colloquium · University of Texas at Austin, May 13, 2020</div>
    </div>
  </section>

  <!-- TEACHING -->
  <section class="cv-section">
    <h2 class="cv-section-title">Teaching Experience</h2>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Graduate Teaching Assistant — Political Ideologies &amp; Manifestos</div>
        <div class="cv-item-date">Fall 2025</div>
      </div>
      <div class="cv-item-subtitle">Dr. Kiril Avramov &amp; Dr. Jason Roberts · University of Texas at Austin · 86 students</div>
      <div class="cv-item-body">Course management, student communications, grading précis papers and discussion posts, academic support and progress monitoring.</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Graduate Teaching Assistant — Hidden Lives of Maps</div>
        <div class="cv-item-date">Spring 2025</div>
      </div>
      <div class="cv-item-subtitle">Dr. Steven Seegel · University of Texas at Austin · 98 students</div>
      <div class="cv-item-body">Led three weekly discussion sections, developing original curriculum and teaching materials; facilitated student discussions on cartographic analysis and geographic representation.</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Graduate Teaching Assistant — Intelligence and Espionage in the Eastern Bloc</div>
        <div class="cv-item-date">Fall 2024</div>
      </div>
      <div class="cv-item-subtitle">Dr. Kiril Avramov · University of Texas at Austin · 87 students</div>
      <div class="cv-item-body">Managed student communications, assignment coordination, attendance records, and Canvas course management.</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Resident Director</div>
        <div class="cv-item-date">Summers 2022 &amp; 2023</div>
      </div>
      <div class="cv-item-subtitle">American Councils for International Education · Narva, Estonia</div>
      <div class="cv-item-body">Managed U.S. State Department youth exchange programs with 24/7 student support; coordinated academic programming, crisis response, and cross-cultural mentorship.</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Undergraduate Teaching Assistant — NSC 109: Originality in Science Research</div>
        <div class="cv-item-date">Fall 2018</div>
      </div>
      <div class="cv-item-subtitle">University of Texas at Austin</div>
      <div class="cv-item-body">Served as cohort leader and mentor for honors students; guided independent research inquiries and collaborative grant proposal projects; provided weekly mentoring on research design and scientific methodology.</div>
    </div>
  </section>

  <!-- TECHNICAL SKILLS -->
  <section class="cv-section">
    <h2 class="cv-section-title">Technical &amp; Research Skills</h2>

    <div class="cv-skills-grid">
      <div class="cv-skill-cat">
        <h4>Programming &amp; Computation</h4>
        <div class="cv-skill-tags">
          <span class="cv-skill-tag">Python</span>
          <span class="cv-skill-tag">Pandas / NumPy</span>
          <span class="cv-skill-tag">scikit-learn</span>
          <span class="cv-skill-tag">NLP / web scraping</span>
          <span class="cv-skill-tag">R (ggplot2, dplyr)</span>
          <span class="cv-skill-tag">SQL</span>
          <span class="cv-skill-tag">LDA topic modeling</span>
        </div>
    </section>

    <section class="section">
        <h2 class="section-title">Research & Publications</h2>

        <div class="item">
            <div class="item-header">
                <div>
                    <div class="item-title">Food Systems and Agricultural Resilience in Eastern Europe</div>
                    <div class="item-subtitle">Graduate Thesis Research (In Development)</div>
                </div>
                <div class="item-date">2023 – Present</div>
            </div>
            <div class="item-details">
                Examining how food systems in Eastern Europe adapt to political, economic, and environmental challenges. Preparing for fieldwork in Czechia on agricultural cooperation models and regional food security strategies, supported by a FLAS Fellowship for Czech language study.
            </div>
        </div>

        <div class="item">
            <div class="item-header">
                <div>
                    <div class="item-title">Ukrainian Agriculture and Environmental Resilience</div>
                    <div class="item-subtitle">Policy Research, U.S. Department of the Interior</div>
                </div>
                <div class="item-date">Summer 2024</div>
            </div>
            <div class="item-details">
                Conducted mixed-methods assessment of Ukraine's institutional capacity for climate action across four indicator areas: demographics, agricultural and land trends, climate mandate and legislation, and civil service capacity. Produced briefing materials for U.S. and Ukrainian government officials.
            </div>
        </div>

        <div class="item">
            <div class="item-header">
                <div>
                    <div class="item-title">The Soviet Stolovaya and 1991: A Culture of Food Aid Before and After the USSR</div>
                    <div class="item-subtitle">Undergraduate Honors Thesis · UT Austin, College of Natural Sciences</div>
                </div>
                <div class="item-date">2022</div>
            </div>
            <div class="item-details">
                Analyzed the evolution of the Soviet stolovaya (cafeteria) system as a form of public food aid. Methods: interviews, content analysis of Soviet film and media, and historical research on state welfare policy from early Soviet history through post-1991 privatization.
            </div>
        </div>

        <div class="item">
            <div class="item-header">
                <div>
                    <div class="item-title">The Food System of Bahrain: Analyzing Risks and Possibilities</div>
                    <div class="item-subtitle">Undergraduate Capstone White Paper · UT Austin, College of Liberal Arts</div>
                </div>
                <div class="item-date">2022</div>
            </div>
            <div class="item-details">
                Assessed food security challenges in Bahrain: historical fisheries, land use, import dependence, climate vulnerabilities, and traditional crop systems. Proposed food sovereignty strategies combining traditional knowledge with modern agricultural technologies.
            </div>
        </div>

        <h2 class="section-title" style="margin-top: 2rem;">Conferences & Presentations</h2>

        <div class="item">
            <div class="item-header">
                <div>
                    <div class="item-title">"CAP Common Agricultural Policy Funding Mechanisms"</div>
                    <div class="item-subtitle">A Policy Blueprint for Ukraine's EU Integration Workshop · Warsaw, Poland</div>
                </div>
                <div class="item-date">July 2025</div>
            </div>
            <div class="item-details">
                Presenter and member of the workshop organizing team.
            </div>
        </div>

        <div class="item">
            <div class="item-header">
                <div>
                    <div class="item-title">Conference Attendance</div>
                </div>
            </div>
            <div class="item-details">
                <strong>ESRS (European Society for Rural Sociology) Conference</strong> — Riga, Latvia (July 2025)<br>
                <strong>ASEEES Annual Convention</strong> — Boston, MA (November 2024)<br>
                <strong>Climate Adaptation Scenario Planning Workshop for Ukraine's Food Security</strong> — LBJ Washington Center (October 2024) <em>(organizing team)</em><br>
                <strong>Russia in Contemporary World History</strong> — UT Austin (November 2024)<br>
                <strong>TREEES Conference</strong> — UT Austin (2023)
            </div>
        </div>
    </section>

    <section class="section">
        <h2 class="section-title">Technical & Research Skills</h2>
        
        <div class="skills-grid">
            <div class="skill-category">
                <h4>Quantitative Tools</h4>
                <div class="skill-tags">
                    <span class="skill-tag">R (ggplot2, dplyr)</span>
                    <span class="skill-tag">Python (Pandas, NumPy)</span>
                    <span class="skill-tag">SQL</span>
                    <span class="skill-tag">ArcGIS</span>
                </div>
            </div>

            <div class="skill-category">
                <h4>Qualitative Methods</h4>
                <div class="skill-tags">
                    <span class="skill-tag">MAXQDA</span>
                    <span class="skill-tag">Interviews</span>
                    <span class="skill-tag">Participant Observation</span>
                    <span class="skill-tag">Discourse Analysis</span>
                </div>
            </div>

            <div class="skill-category">
                <h4>Molecular Biology</h4>
                <div class="skill-tags">
                    <span class="skill-tag">PCR</span>
                    <span class="skill-tag">DNA/RNA extraction</span>
                    <span class="skill-tag">Transformation</span>
                    <span class="skill-tag">Microscopy</span>
                </div>
            </div>

            <div class="skill-category">
                <h4>Software</h4>
                <div class="skill-tags">
                    <span class="skill-tag">Microsoft 365</span>
                    <span class="skill-tag">Google Workspace</span>
                    <span class="skill-tag">Qualtrics</span>
                    <span class="skill-tag">Slack</span>
                </div>
            </div>
        </div>
      </div>

      <div class="cv-skill-cat">
        <h4>Qualitative &amp; Mixed Methods</h4>
        <div class="cv-skill-tags">
          <span class="cv-skill-tag">MAXQDA</span>
          <span class="cv-skill-tag">Interview design &amp; transcription</span>
          <span class="cv-skill-tag">Participant observation</span>
          <span class="cv-skill-tag">Discourse analysis</span>
          <span class="cv-skill-tag">LLM-assisted analysis</span>
          <span class="cv-skill-tag">Fuzzy cognitive mapping</span>
        </div>
      </div>

      <div class="cv-skill-cat">
        <h4>Geospatial &amp; Lab</h4>
        <div class="cv-skill-tags">
          <span class="cv-skill-tag">ArcGIS Pro</span>
          <span class="cv-skill-tag">PCR &amp; genotyping</span>
          <span class="cv-skill-tag">DNA/RNA extraction</span>
          <span class="cv-skill-tag">Fluorescence microscopy</span>
          <span class="cv-skill-tag">ImageJ</span>
        </div>
      </div>
    </div>
  </section>

  <!-- LANGUAGES -->
  <section class="cv-section">
    <h2 class="cv-section-title">Language Skills</h2>

    <div class="cv-lang-grid">
      <div class="cv-lang-item">
        <span class="cv-lang-name">Russian</span>
        <span class="cv-lang-level">Advanced Low (ACTFL 2024) · ≈ B2 CEFR</span>
        <span class="cv-lang-note">Moldova, Kyrgyzstan; multiple FLAS fellowships</span>
      </div>
      <div class="cv-lang-item">
        <span class="cv-lang-name">Arabic</span>
        <span class="cv-lang-level">Advanced Mid (ACTFL 2025) · ≈ B2 CEFR</span>
        <span class="cv-lang-note">Arabic Flagship graduate; Boren Scholar; Morocco fieldwork</span>
      </div>
      <div class="cv-lang-item">
        <span class="cv-lang-name">Czech</span>
        <span class="cv-lang-level">Intermediate High (ACTFL 2025) · ≈ B1 CEFR</span>
        <span class="cv-lang-note">Indiana University intensive; thesis fieldwork in Czechia</span>
      </div>
      <div class="cv-lang-item">
        <span class="cv-lang-name">Ukrainian</span>
        <span class="cv-lang-level">Intermediate</span>
        <span class="cv-lang-note">FLAS Fellow 2024–2025; policy research &amp; translation</span>
      </div>
      <div class="cv-lang-item">
        <span class="cv-lang-name">French</span>
        <span class="cv-lang-level">Intermediate</span>
        <span class="cv-lang-note">Academic and professional reading proficiency</span>
      </div>
      <div class="cv-lang-item">
        <span class="cv-lang-name">Spanish</span>
        <span class="cv-lang-level">Intermediate</span>
        <span class="cv-lang-note">Academic and professional reading proficiency</span>
      </div>
    </div>
  </section>

  <!-- SERVICE -->
  <section class="cv-section">
    <h2 class="cv-section-title">Service</h2>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Associate Editor</div>
        <div class="cv-item-date">2024 – Present</div>
      </div>
      <div class="cv-item-subtitle">Constitutional Studies: A Global Comparative Journal</div>
      <div class="cv-item-body">Serve on editorial team for international peer-reviewed constitutional law journal; translate and localize website content and editorial materials into Spanish, French, Russian, and Arabic; support journal relaunch and international localization initiatives.</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Arabic Language Tutor</div>
        <div class="cv-item-date">2023–2024</div>
      </div>
      <div class="cv-item-subtitle">Arabic Flagship Program · University of Texas at Austin</div>
      <div class="cv-item-body">Provided individualized Arabic language instruction; assisted students in developing proficiency in Modern Standard Arabic and dialect.</div>
    </div>

    <div class="cv-item">
      <div class="cv-item-header">
        <div class="cv-item-title">Judge, Olympiada of Spoken Russian</div>
        <div class="cv-item-date">2024–2025</div>
      </div>
      <div class="cv-item-subtitle">Center for Russian, East European, and Eurasian Studies · University of Texas at Austin</div>
      <div class="cv-item-body">Evaluated student Russian language proficiency in a competitive academic setting; supported K–12 Russian language education and student achievement recognition.</div>
    </div>
  </section>

  <!-- CONFERENCES & WORKSHOPS -->
  <section class="cv-section">
    <h2 class="cv-section-title">Conferences &amp; Workshops</h2>

    <div class="cv-item" style="padding-top: 0; border-bottom: none;">
      <p class="cv-pub-subhead" style="margin-top:0;">Presenter / Participant</p>
      <ul class="cv-conf-list">
        <li>
          <span>Round Table Panelist — <strong>Symposium: Transatlantic Ties and Opportunities in a Transformative Age</strong>, "Perspectives on Transatlantic Cooperation: EU Cohesion and Integration" · Texas Global at UT Austin</span>
          <span class="conf-date">November 11, 2025</span>
        </li>
        <li>
          <span>Presenter (with Dr. Mary Neuburger) — <strong>TREEES Conference</strong>, "Bulgaria's Green Revolutions? Agricultural Transformation, Cold War Encounters and Environmental Backlash, 1930–1989" · Rice University</span>
          <span class="conf-date">September 27, 2025</span>
        </li>
        <li>
          <span><strong>KIU Ukrainian Summer School</strong> · Frankfurt (Oder), Germany</span>
          <span class="conf-date">September 8–19, 2025</span>
        </li>
        <li>
          <span><strong>A Blueprint for Ukraine's European Union Integration</strong>: Creating Risk Reduction and Climate Adaptation Strategies in the Agriculture Sector · Polish Academy of Sciences, Warsaw <span class="conf-note">(funded by LBJ School for Public Affairs)</span></span>
          <span class="conf-date">July 1–3, 2025</span>
        </li>
        <li>
          <span><strong>Climate Adaptation Scenario Planning for Ukraine's Food Security Workshop</strong> · LBJ Washington Center <span class="conf-note">(funded by U.S. Dept. of State; implemented by U.S. Dept. of Interior)</span></span>
          <span class="conf-date">October 22–24, 2024</span>
        </li>
      </ul>

      <p class="cv-pub-subhead" style="margin-top: 20px;">Attended</p>
      <ul class="cv-conf-list">
        <li>
          <span><strong>30th European Society for Rural Sociology Congress</strong> · Riga, Latvia</span>
          <span class="conf-date">July 2025</span>
        </li>
        <li>
          <span><strong>Central Asia Policy Symposium</strong> · Austin, Texas</span>
          <span class="conf-date">February 2025</span>
        </li>
        <li>
          <span><strong>2024 ASEEES Annual Convention</strong> · Boston, Massachusetts</span>
          <span class="conf-date">November 2024</span>
        </li>
        <li>
          <span><strong>Russia in Contemporary World History Conference</strong> · Austin, Texas</span>
          <span class="conf-date">November 2024</span>
        </li>
      </ul>
    </div>
  </section>

  <!-- DOWNLOAD -->
  <div class="cv-download">
    <span class="cv-download-label">Full CV</span>
    <a href="/files/Evan_Samsky_CV.pdf" class="cv-download-btn" target="_blank">Download PDF</a>
  </div>

</div>
