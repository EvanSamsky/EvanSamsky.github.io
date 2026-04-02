---
title: "Institutional Capacity for Climate Action in Ukraine's Agricultural Sector"
date: "2024-08-01"
description: "A policy assessment examining Ukraine's institutional capacity across four indicators: demographics, agricultural trends, climate mandate, and civil service capacity. Produced for the U.S. Department of the Interior."
tags: ["Ukraine", "agriculture", "climate policy", "institutional capacity", "food systems", "Eastern Europe"]
categories: ["Research"]
---

<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.min.js"></script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Source+Serif+4:wght@300;400;600&display=swap');

  :root {
    --ink: #2D4739;
    --paper: #f4f0ed;
    --aged: #CBD7C1;
    --rust: #4b3034;
    --gold: #4b3034;
    --slate: #2D4739;
    --muted: #7a8c7e;
    --ukraine-blue: #005BBB;
    --ukraine-yellow: #FFD500;
    --border: #b5c4ad;
    --chart-bg: #f9f6f3;
    --blush: #E3BCB5;
  }

  .ukraine-report {
    font-family: 'Source Serif 4', Georgia, serif;
    color: var(--ink);
    font-size: 17px;
    line-height: 1.75;
  }

  .ukraine-report section { margin-bottom: 4rem; }

  .ukraine-report h2 {
    font-family: 'Playfair Display', Georgia, serif;
    font-size: 1.75rem;
    font-weight: 700;
    color: var(--ink);
    margin-bottom: 0.5rem;
    padding-bottom: 0.5rem;
    border-bottom: 2px solid var(--ukraine-blue);
  }
  .ukraine-report h3 {
    font-family: 'Playfair Display', Georgia, serif;
    font-size: 1.2rem;
    font-weight: 400;
    font-style: italic;
    color: var(--rust);
    margin: 1.75rem 0 0.75rem;
  }
  .ukraine-report p { margin-bottom: 1rem; color: var(--ink); }

  .ukraine-report blockquote {
    border: none;
    padding: 1.5rem 2rem;
    background: #E3BCB533;
    margin: 2rem 0;
    position: relative;
  }
  .ukraine-report blockquote::before {
    content: '\201C';
    font-family: 'Playfair Display', serif;
    font-size: 5rem;
    color: var(--ukraine-yellow);
    opacity: 0.7;
    position: absolute;
    top: -0.5rem;
    left: 0.75rem;
    line-height: 1;
  }
  .ukraine-report blockquote p {
    font-style: italic;
    font-size: 1.05rem;
    line-height: 1.65;
    padding-left: 1.5rem;
  }
  .ukraine-report blockquote cite {
    display: block;
    font-size: 0.8rem;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    color: var(--muted);
    padding-left: 1.5rem;
    margin-top: 0.5rem;
  }

  .ukraine-report footer {
    background: var(--ink);
    color: rgba(245,240,232,0.5);
    padding: 2rem;
    text-align: center;
    font-size: 0.8rem;
    letter-spacing: 0.04em;
    margin-top: 3rem;
  }

  /* ── Header ── */
  .masthead {
    background: var(--ink);
    color: var(--paper);
    padding: 3rem 2rem 2.5rem;
    text-align: center;
    position: relative;
    overflow: hidden;
    margin: 0 -2rem 0;
  }
  .masthead::before {
    content: '';
    position: absolute; inset: 0;
    background: repeating-linear-gradient(
      45deg,
      transparent,
      transparent 40px,
      rgba(255,213,0,0.05) 40px,
      rgba(255,213,0,0.05) 41px
    );
  }
  .masthead-flag {
    display: flex;
    height: 8px;
    width: 120px;
    margin: 0 auto 1.5rem;
    border-radius: 2px;
    overflow: hidden;
    box-shadow: 0 1px 6px rgba(0,0,0,0.3);
  }
  .masthead-flag span:first-child { flex: 1; background: var(--ukraine-blue); }
  .masthead-flag span:last-child  { flex: 1; background: var(--ukraine-yellow); }
  .masthead h1 {
    font-family: 'Playfair Display', Georgia, serif;
    font-size: clamp(1.6rem, 4vw, 2.8rem);
    font-weight: 700;
    letter-spacing: -0.01em;
    line-height: 1.2;
    max-width: 820px;
    margin: 0 auto 1rem;
    position: relative;
    color: var(--paper);
  }
  .masthead .subtitle {
    font-family: 'Source Serif 4', serif;
    font-weight: 300;
    font-size: 0.95rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: rgba(245,240,232,0.65);
    position: relative;
  }
  .masthead-rule {
    width: 60px; height: 2px;
    background: var(--ukraine-yellow);
    margin: 1.25rem auto;
  }

  /* ── Nav ── */
  .toc-nav {
    background: #CBD7C1;
    border-bottom: 1px solid var(--border);
    padding: 0.75rem 2rem;
    display: flex;
    gap: 0.5rem 2rem;
    flex-wrap: wrap;
    justify-content: center;
    position: sticky;
    top: 0;
    z-index: 100;
    margin: 0 -2rem;
  }
  .toc-nav a {
    font-size: 0.78rem;
    letter-spacing: 0.07em;
    text-transform: uppercase;
    color: #4b3034;
    text-decoration: none;
    font-family: 'Source Serif 4', serif;
    font-weight: 600;
    transition: color 0.2s;
  }
  .toc-nav a:hover { color: var(--ink); }

  /* ── Layout ── */
  .report-container {
    max-width: 860px;
    margin: 0 auto;
    padding: 3rem 0;
  }

  /* ── Section label ── */
  .section-label {
    font-size: 0.7rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--muted);
    font-family: 'Source Serif 4', serif;
    font-weight: 600;
    margin-bottom: 0.6rem;
    display: block;
  }

  /* ── Callout box ── */
  .callout {
    border-left: 3px solid var(--rust);
    background: var(--aged);
    padding: 1rem 1.25rem;
    margin: 1.5rem 0;
    font-size: 0.93rem;
    color: var(--slate);
  }
  .callout strong { color: var(--rust); }

  /* ── Indicator cards ── */
  .indicator-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 1rem;
    margin: 1.5rem 0;
  }
  .indicator-card {
    background: var(--aged);
    border: 1px solid var(--border);
    padding: 1rem 1.25rem;
    border-top: 3px solid var(--ukraine-blue);
  }
  .indicator-card .ic-num {
    font-family: 'Playfair Display', serif;
    font-size: 2rem;
    color: var(--rust);
    line-height: 1;
    margin-bottom: 0.4rem;
  }
  .indicator-card .ic-label {
    font-size: 0.8rem;
    font-weight: 600;
    letter-spacing: 0.05em;
    text-transform: uppercase;
    color: var(--slate);
  }
  .indicator-card .ic-desc {
    font-size: 0.82rem;
    color: var(--muted);
    margin-top: 0.4rem;
  }

  /* ── Chart wrapper ── */
  .chart-wrap {
    background: var(--chart-bg);
    border: 1px solid var(--border);
    padding: 1.5rem 1.5rem 1rem;
    margin: 1.75rem 0;
  }
  .chart-title {
    font-family: 'Playfair Display', serif;
    font-size: 1rem;
    font-weight: 700;
    color: var(--ink);
    margin-bottom: 0.2rem;
  }
  .chart-source {
    font-size: 0.72rem;
    color: var(--muted);
    letter-spacing: 0.04em;
    margin-top: 0.6rem;
  }
  .chart-container {
    position: relative;
    height: 340px;
  }
  .chart-container.tall { height: 420px; }
  .chart-container.short { height: 260px; }

  /* ── Toggle controls ── */
  .chart-controls {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-bottom: 0.75rem;
  }
  .ctrl-btn {
    padding: 0.25rem 0.7rem;
    font-size: 0.75rem;
    font-family: 'Source Serif 4', serif;
    font-weight: 600;
    letter-spacing: 0.05em;
    text-transform: uppercase;
    border: 1px solid var(--border);
    background: transparent;
    color: var(--slate);
    cursor: pointer;
    transition: background 0.15s, color 0.15s;
  }
  .ctrl-btn.active {
    background: #2D4739;
    color: white;
    border-color: #2D4739;
  }
  .ctrl-btn:hover:not(.active) { background: var(--aged); }

  /* ── Horizontal bar chart ── */
  .hbar-chart { margin: 0.5rem 0; }
  .hbar-row {
    display: flex;
    align-items: center;
    margin-bottom: 0.5rem;
    font-size: 0.82rem;
  }
  .hbar-label {
    width: 220px;
    min-width: 220px;
    text-align: right;
    padding-right: 0.75rem;
    color: var(--slate);
    line-height: 1.3;
  }
  .hbar-track {
    flex: 1;
    background: var(--aged);
    height: 22px;
    position: relative;
    border-radius: 2px;
    overflow: hidden;
  }
  .hbar-fill {
    height: 100%;
    border-radius: 2px;
    transition: width 0.6s ease;
    display: flex;
    align-items: center;
    padding-left: 6px;
  }
  .hbar-val {
    font-size: 0.72rem;
    font-weight: 600;
    color: white;
    white-space: nowrap;
  }

  /* ── Conclusions list ── */
  .findings-list { list-style: none; padding: 0; }
  .findings-list li {
    padding: 0.85rem 0 0.85rem 2.5rem;
    border-bottom: 1px solid var(--border);
    position: relative;
    font-size: 0.93rem;
  }
  .findings-list li:last-child { border-bottom: none; }
  .findings-list li::before {
    content: attr(data-num);
    position: absolute;
    left: 0;
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    color: var(--ukraine-blue);
    font-weight: 700;
  }

  @media (max-width: 600px) {
    .hbar-label { width: 130px; min-width: 130px; font-size: 0.75rem; }
    .chart-container { height: 260px; }
    .chart-container.tall { height: 340px; }
  }
</style>

<div class="ukraine-report">

<header class="masthead">
  <div class="masthead-flag"><span></span><span></span></div>
  <p class="subtitle">Policy Assessment Report &middot; Draft</p>
  <div class="masthead-rule"></div>
  <h1>Institutional Capacity for Climate Action in Ukraine's Agricultural Sector</h1>
  <div class="masthead-rule"></div>
  <p class="subtitle">A General Assessment</p>
</header>

<nav class="toc-nav">
  <a href="#summary">Summary</a>
  <a href="#introduction">Introduction</a>
  <a href="#demographics">Demographics</a>
  <a href="#agriculture">Agriculture &amp; Land</a>
  <a href="#mandate">Climate Mandate</a>
  <a href="#civil-service">Civil Service</a>
  <a href="#conclusions">Conclusions</a>
</nav>

<div class="report-container">

<section id="summary">
  <span class="section-label">Overview</span>
  <h2>Executive Summary</h2>
  <p>Estimating each country's ability to implement climate resilience policies and enhance environmental sustainability is essential to tackling the collective threat of climate change. Agriculture and water management are key areas that directly enhance resilience to climate change, but perhaps remain under addressed. For Ukraine, Russia's full-scale invasion and war of aggression has exacerbated environmental damage, calling into question how rebuilding the agricultural sector of the country will progress.</p>
  <p>Additionally, efforts towards accession to the European Union may require approximation of legislation and efforts associated with the EU Green Deal and Common Agricultural Policy 2023&ndash;27, which promote sustainable agriculture.</p>

  <div class="indicator-grid">
    <div class="indicator-card">
      <div class="ic-num">01</div>
      <div class="ic-label">Population &amp; Demographics</div>
      <div class="ic-desc">Outmigration, casualty, and displacement impacts on workforce</div>
    </div>
    <div class="indicator-card">
      <div class="ic-num">02</div>
      <div class="ic-label">Agricultural &amp; Land Trends</div>
      <div class="ic-desc">Arable land, fertilizer use, sustainable farming adoption</div>
    </div>
    <div class="indicator-card">
      <div class="ic-num">03</div>
      <div class="ic-label">Climate Mandate</div>
      <div class="ic-desc">Legislation and policy framework for sustainable agriculture</div>
    </div>
    <div class="indicator-card">
      <div class="ic-num">04</div>
      <div class="ic-label">Civil Service Capacity</div>
      <div class="ic-desc">Independence, satisfaction, and capacity of key ministries</div>
    </div>
  </div>
</section>

<section id="introduction">
  <span class="section-label">Background</span>
  <h2>Introduction</h2>
  <p>This report provides an overview of institutional challenges within Ukraine's agricultural sector, focusing on the concept of institutional capacity. Originating at the time of the Marshall Plan, institutional capacity and capacity building have been crucial in contextualising post-conflict reconstruction efforts.</p>
  <blockquote>
    <p>Institutional capacity is defined as the quality of leadership, incentives, systems, resources, and personnel that produce results based on the mission, goals, and objectives of the institution.</p>
    <cite>USAID, Institutional Capacity Assessment Tool (2013)</cite>
  </blockquote>
  <p>This assessment aims to provide policymakers and stakeholders with insights into Ukraine's agricultural institutional landscape, identifying areas for potential improvement and international cooperation. Comparison countries include Poland, Romania, Bulgaria, Netherlands, Moldova, Georgia, and France &mdash; nations that share historical circumstances or represent EU agricultural benchmarks.</p>
</section>

<section id="demographics">
  <span class="section-label">Indicator 01</span>
  <h2>Population &amp; Demographic Trends</h2>
  <div class="callout">
    <strong>Key challenges:</strong> Outmigration of skilled individuals &middot; Growth in elderly and disabled population &middot; Conflict-related casualties. Ukraine's population within its 1991 borders has decreased by approximately <strong>14 million people</strong> since the escalation of conflict in 2022.
  </div>
  <p>Estimating Ukraine's current resident population presents unique challenges due to territorial occupation, outmigration of skilled individuals, and refugee and internally displaced person movements. Employment in agriculture accounts for 14% of total formally registered employment in Ukraine, down from 23% in 1998.</p>

  <div class="chart-wrap">
    <div class="chart-title">Fig. 1 &mdash; Population Growth Rate (annual %)</div>
    <div class="chart-controls" id="ctrl-pop-growth">
      <button class="ctrl-btn active" data-chart="popGrowth" data-action="all">All Countries</button>
      <button class="ctrl-btn" data-chart="popGrowth" data-action="ukraine">Highlight Ukraine</button>
    </div>
    <div class="chart-container">
      <canvas id="chartPopGrowth"></canvas>
    </div>
    <p class="chart-source">Source: World Bank Group (2024) World Development Indicators. https://doi.org/10.57966/6rwy-0b07</p>
  </div>

  <div class="chart-wrap">
    <div class="chart-title">Fig. 2 &mdash; Demographic Pressures Index (lower is better, scale 1&ndash;10)</div>
    <div class="chart-controls" id="ctrl-demog">
      <button class="ctrl-btn active" data-chart="demogPressure" data-action="all">All Countries</button>
      <button class="ctrl-btn" data-chart="demogPressure" data-action="ukraine">Highlight Ukraine</button>
    </div>
    <div class="chart-container">
      <canvas id="chartDemogPressure"></canvas>
    </div>
    <p class="chart-source">Source: The Fund for Peace (2023) Fragile States Index. https://fragilestatesindex.org/</p>
  </div>

  <div class="chart-wrap">
    <div class="chart-title">Fig. 3 &amp; 4 &mdash; Human Flight / Brain Drain &amp; Refugees / IDPs</div>
    <div class="chart-controls">
      <button class="ctrl-btn active" id="tab-brain" onclick="switchFSITab('brain')">Human Flight &amp; Brain Drain</button>
      <button class="ctrl-btn" id="tab-refugee" onclick="switchFSITab('refugee')">Refugees &amp; IDPs</button>
    </div>
    <div class="chart-container" id="fsi-panel-brain">
      <canvas id="chartBrainDrain"></canvas>
    </div>
    <div class="chart-container" id="fsi-panel-refugee" style="display:none">
      <canvas id="chartRefugees"></canvas>
    </div>
    <p class="chart-source">Source: The Fund for Peace (2023) Fragile States Index. Scale 1&ndash;10, lower is better. Note the sharp 2022&ndash;23 increases for Ukraine.</p>
  </div>
</section>

<section id="agriculture">
  <span class="section-label">Indicator 02</span>
  <h2>Agricultural &amp; Land Trends</h2>
  <div class="callout">
    <strong>Key findings:</strong> Ukraine has ~32.7 million hectares of arable land (approx. 1/3 of the EU total). Estimates of farmland potentially impacted by landmines range from <strong>1.4% to 15%</strong>, with NASA Harvest satellite analysis suggesting up to <strong>6.9 million hectares</strong> of abandoned farmland in 2023.
  </div>

  <p>Fertilizer and pesticide consumption both enables Ukraine to produce export-oriented crops to fund its war effort, but also contributes toward environmental degradation. Compared with other European countries, Ukraine's use of fertilizers is relatively low, though inorganic fertilizer use has increased since the early 1990s.</p>

  <div class="chart-wrap">
    <div class="chart-title">Fig. 6 &mdash; Fertilizer Consumption (kg per hectare of arable land)</div>
    <div class="chart-controls" id="ctrl-fert">
      <button class="ctrl-btn active" data-chart="fertComp" data-action="all">All Countries</button>
      <button class="ctrl-btn" data-chart="fertComp" data-action="ukraine">Highlight Ukraine</button>
    </div>
    <div class="chart-container">
      <canvas id="chartFertComp"></canvas>
    </div>
    <p class="chart-source">Source: FAO (2021) via World Bank DataBank. https://data.worldbank.org/indicator/AG.CON.FERT.ZS</p>
  </div>

  <p>Inorganic fertilizer use by crop type reveals a structural shift: industrial crops and maize have grown substantially as a share of total fertilizer use, reflecting wartime reallocation of agricultural resources toward export-oriented production.</p>

  <div class="chart-wrap">
    <div class="chart-title">Fig. 7 &mdash; Inorganic Fertilizer Use in Ukraine by Crop Type (thousands of tonnes)</div>
    <div class="chart-container tall">
      <canvas id="chartFertCrop"></canvas>
    </div>
    <p class="chart-source">Source: State Statistics Service of Ukraine (2023). https://ukrstat.gov.ua</p>
  </div>

  <div class="chart-wrap">
    <div class="chart-title">Fig. 8 &mdash; % of Land Area Treated with Pesticide in Ukraine by Crop Type</div>
    <div class="chart-container">
      <canvas id="chartPesticide"></canvas>
    </div>
    <p class="chart-source">Source: State Statistics Service of Ukraine (2023). https://ukrstat.gov.ua</p>
  </div>

  <p>Sustainable agriculture currently takes place in Ukraine, but the full extent of its utilisation is difficult to ascertain. Official reports only capture organic agriculture, likely undercounting farms using sustainable techniques without formal certification. Data on organic agriculture shows more limited adoption compared to EU counterpart countries, with all comparison countries increasing organic agriculture over time.</p>
</section>

<section id="mandate">
  <span class="section-label">Indicator 03</span>
  <h2>Climate Change Mandate &amp; Legislation</h2>
  <div class="callout">
    <strong>Status:</strong> Ukraine adopted the State Environmental Policy until 2030 in 2019. A draft Strategy for Agriculture and Rural Development until 2030 has been introduced. However, key components of a comprehensive climate mandate &mdash; including monitoring and evaluation, subnational mandates, and cross-ministry coordination &mdash; remain unaddressed.
  </div>

  <p>While several pieces of legislation for climate adaptation and sustainability have been approved and have come into force &mdash; first in 2019 but also as recently as 2024 &mdash; a need remains for connection between the State Environmental Policy and agriculture.</p>

  <h3>Recommended mandate components not yet fully addressed</h3>
  <ul class="findings-list">
    <li data-num="&rarr;">A mandate for regular policy review to reflect new data</li>
    <li data-num="&rarr;">A mandate for Monitoring and Evaluation of climate change itself and progression of adaptation strategies</li>
    <li data-num="&rarr;">A mandate for engaging stakeholders for support and input</li>
    <li data-num="&rarr;">A mandate for action at subnational levels and across national ministries</li>
    <li data-num="&rarr;">Compatibility between adaptation strategies and other national mandates</li>
  </ul>

  <p>Interest in EU accession and policy approximation for the Association Agreement has provided impetus for environmental policy reforms. However, more needs-based assessments have only recognised environmental sustainability in terms of damage suffered as a result of conflict, with criticism of recovery plans focusing primarily on production volumes over sustainability.</p>
</section>

<section id="civil-service">
  <span class="section-label">Indicator 04</span>
  <h2>Civil Service Independence &amp; Capacity</h2>
  <div class="callout">
    <strong>Data note:</strong> The Civil Service Feedback Loop Initiative survey was conducted Oct 31 &ndash; Dec 7, 2018, across Ukrainian government ministries in partnership with Stanford University's Center for Democracy, Development, and the Rule of Law. Results focus on the Ministry of Agrarian Policy and Food (MINAGRO) and the Ministry of Environmental Protection and Natural Resources.
  </div>

  <h3>Do formal rules hinder or help meeting job objectives?</h3>
  <div class="chart-wrap">
    <div class="chart-title">Fig. 10 &mdash; How frequently do formal rules hinder or help meeting job objectives?</div>
    <div class="chart-container short">
      <canvas id="chartRules"></canvas>
    </div>
    <p class="chart-source">Source: Moskalu et al. (2019) Civil Service Feedback Loop Initiative Survey, Q3.3</p>
  </div>

  <h3>Ease of interaction with different parties</h3>
  <p>Respondents reported the most ease interacting with colleagues in their own work unit and their direct supervisor. Interaction with political leadership, specialists on civil service reform, and external experts was comparatively harder.</p>
  <div class="chart-wrap">
    <div class="chart-title">Fig. 11 &mdash; Ease of Interaction ("Rather easy" or "Very easy" responses, %)</div>
    <div class="chart-container">
      <canvas id="chartInteraction"></canvas>
    </div>
    <p class="chart-source">Source: Moskalu et al. (2019) Civil Service Feedback Loop Initiative Survey, Q3.6</p>
  </div>

  <h3>Does management take expert suggestions into account?</h3>
  <div class="chart-wrap">
    <div class="chart-title">Fig. 12 &mdash; Does management take your expert suggestions into account?</div>
    <div class="chart-container short">
      <canvas id="chartExpert"></canvas>
    </div>
    <p class="chart-source">Source: Moskalu et al. (2019) Civil Service Feedback Loop Initiative Survey, Q3.8</p>
  </div>

  <h3>Factors important for securing a posting</h3>
  <p>Professional knowledge and work experience were identified as most important for being hired. Loyalty to superiors, personal connections, and political connections were reported as less important &mdash; though with meaningful variation in responses.</p>
  <div class="chart-wrap">
    <div class="chart-title">Fig. 14 &mdash; Importance of factors for securing a posting (% "Rather important" or "Very important")</div>
    <div class="chart-container short">
      <canvas id="chartHiring"></canvas>
    </div>
    <p class="chart-source">Source: Moskalu et al. (2019) Civil Service Feedback Loop Initiative Survey, Q4.6</p>
  </div>

  <h3>Reported discrimination in the civil service</h3>
  <p>Discrimination based on gender, sexual orientation, and religion were not strongly reported. However, discrimination based on age, rank, and tenure appear more prominent.</p>
  <div class="chart-wrap">
    <div class="chart-title">Fig. 15 &mdash; Reported Discrimination (% who responded "Sometimes," "Often," or "Most of the time")</div>
    <div class="chart-container short">
      <canvas id="chartDiscrim"></canvas>
    </div>
    <p class="chart-source">Source: Moskalu et al. (2019) Civil Service Feedback Loop Initiative Survey, Q4.9</p>
  </div>

  <h3>Ability to report violations without fear of reprisal</h3>
  <div class="chart-wrap">
    <div class="chart-title">Fig. 17 &mdash; "I can disclose a suspected violation without fear of reprisal"</div>
    <div class="chart-container short">
      <canvas id="chartWhistle"></canvas>
    </div>
    <p class="chart-source">Source: Moskalu et al. (2019) Civil Service Feedback Loop Initiative Survey, Q5.4</p>
  </div>

  <h3>Civil service vs. private sector preference</h3>
  <div class="chart-wrap">
    <div class="chart-title">Fig. 18 &mdash; If offered equal salary: civil service or private sector?</div>
    <div class="chart-container short">
      <canvas id="chartPreference"></canvas>
    </div>
    <p class="chart-source">Source: Moskalu et al. (2019) Civil Service Feedback Loop Initiative Survey, Q6.8</p>
  </div>
</section>

<section id="conclusions">
  <span class="section-label">Findings</span>
  <h2>Conclusions</h2>
  <p>Collectively, these four indicator areas form a holistic view of Ukraine's institutional capacity to implement sustainable agriculture and water management. Although not all are directly related to climate action, these measures combine both climate <em>relevant</em> and climate <em>specific</em> indicators:</p>
  <ul class="findings-list">
    <li data-num="1">Ukraine faces <strong>severe demographic challenges</strong> distinct from comparable nations &mdash; including outmigration of skilled workers, an increasing population with disabilities, and conflict-related casualties &mdash; which directly reduce available workforce for institutional implementation of climate policy.</li>
    <li data-num="2">Ukraine presents <strong>large areas of arable land</strong>, but faces significant conflict-related land contamination. Comparatively poor measured utilisation of sustainable farming techniques and limited data collection hinder full assessment.</li>
    <li data-num="3">Ukraine has adopted several measures aimed at developing sustainable agriculture, though <strong>implementation and evaluation remain difficult</strong> during the ongoing conflict. Key mandate components &mdash; including monitoring, subnational action, and cross-ministry coordination &mdash; remain unaddressed.</li>
    <li data-num="4">Ukraine's civil service data (2018) suggest <strong>salary-based dissatisfaction and discrimination based on tenure and rank</strong>. However, employees demonstrated professional initiative and relatively merit-based hiring, suggesting underlying institutional capability.</li>
  </ul>
</section>

</div><!-- /report-container -->

<footer>
  <p>Draft report &middot; Institutional Capacity for Climate Action in Ukraine&rsquo;s Agricultural Sector</p>
  <p style="margin-top:0.5rem">Compiled from World Bank, FAO, Fund for Peace, State Statistics Service of Ukraine, and Stanford CDDRL sources.</p>
</footer>

</div><!-- /ukraine-report -->

<script>
const COUNTRIES = ['Bulgaria','France','Georgia','Moldova','Netherlands','Poland','Romania','Ukraine'];
const YEARS_LONG = Array.from({length:25},(_,i)=>(1999+i).toString());
const YEARS_FSI  = Array.from({length:9}, (_,i)=>(2015+i).toString());

const COLORS = {
  Bulgaria:   '#7a8c7e',
  France:     '#2D4739',
  Georgia:    '#8faa83',
  Moldova:    '#E3BCB5',
  Netherlands:'#b5c4ad',
  Poland:     '#4b3034',
  Romania:    '#CBD7C1',
  Ukraine:    '#005BBB',
};
const COLORS_FADE = Object.fromEntries(
  Object.entries(COLORS).map(([k,v])=>[k, v+'55'])
);

const popGrowthRaw = {
  Bulgaria: [-0.561,-0.494,-1.99,-2.17,-0.792,-0.755,-0.753,-0.760,-0.735,-0.702,-0.644,-0.658,-0.641,-0.579,-0.560,-0.568,-0.638,-0.701,-0.730,-0.722,-0.704,-0.600,-0.815,-3.47,-3.01],
  France:   [0.516,0.686,0.729,0.727,0.706,0.733,0.752,0.696,0.618,0.558,0.513,0.493,0.483,0.484,0.517,0.475,0.356,0.264,0.290,0.358,0.333,0.325,0.357,0.327,0.326],
  Georgia:  [-2.06,-1.94,-1.55,-0.897,-0.675,-0.619,-0.635,-0.568,-0.522,-0.304,-0.888,-0.729,-0.802,-0.737,-0.301,0.0470,0.157,0.0598,0.0134,-0.0390,-0.172,0.0687,-0.380,0.105,0.0803],
  Moldova:  [-0.157,-0.203,-0.224,-0.232,-0.282,-0.247,-0.243,-0.278,-0.232,-0.190,-0.126,-0.0998,-0.0578,-0.0131,-0.0268,-0.0610,-0.767,-1.16,-1.73,-1.76,-1.60,-1.10,-1.50,-2.62,-2.84],
  Netherlands:[0.665,0.715,0.755,0.638,0.472,0.347,0.234,0.161,0.218,0.389,0.514,0.513,0.466,0.370,0.295,0.360,0.443,0.532,0.591,0.584,0.655,0.556,0.523,0.953,0.990],
  Poland:   [-0.00830,-1.04,-0.0276,-0.0463,-0.0675,-0.0585,-0.0439,-0.0634,-0.0543,0.0136,0.0678,-0.286,0.0538,-0.000239,-0.0604,-0.0748,-0.0666,-0.0430,0.0125,-0.000200,-0.0244,-0.175,-2.45,-0.433,-0.366],
  Romania:  [-0.157,-0.129,-1.40,-1.83,-0.721,-0.570,-0.618,-0.592,-1.48,-1.67,-0.833,-0.594,-0.492,-0.445,-0.371,-0.375,-0.470,-0.574,-0.578,-0.587,-0.527,-0.551,-0.746,-0.385,0.0576],
  Ukraine:  [-0.804,-0.844,-0.912,-0.879,-0.747,-0.697,-0.824,-0.647,-0.458,-0.519,-0.418,-0.360,-0.319,-0.211,-0.180,-0.335,-0.409,-0.368,-0.397,-0.501,-0.558,-0.619,-0.857,-7.62,-8.42],
};

const demogPressureRaw = {
  Bulgaria:    [4.2,3.9,3.7,3.4,3.5,3.2,5.2,5.7,5.4],
  France:      [2.8,3.0,2.8,2.5,2.2,1.9,3.9,3.4,3.1],
  Georgia:     [3.9,4.2,3.7,3.4,3.1,2.95,4.5,5.0,4.7],
  Moldova:     [5.3,5.0,4.8,4.5,4.2,3.9,5.4,5.7,5.4],
  Netherlands: [3.0,2.7,2.5,2.2,1.9,1.61,3.1,2.8,2.5],
  Poland:      [3.3,3.0,3.0,2.7,2.4,2.1,3.6,4.1,3.8],
  Romania:     [3.7,3.4,3.2,2.9,2.6,2.3,4.3,4.8,4.5],
  Ukraine:     [4.5,4.4,4.2,3.9,3.6,3.3,4.3,4.8,7.3],
};

const brainDrainRaw = {
  Bulgaria:    [4.6,4.3,4.2,3.9,4.2,4.5,5.0,5.1,5.2],
  France:      [2.2,1.9,2.2,2.46,2.3,2.17,2.1,2.1,2.0],
  Georgia:     [5.4,5.1,4.9,4.6,4.9,5.2,5.5,5.8,6.5],
  Moldova:     [6.4,6.3,6.6,6.39,6.7,7.0,7.5,7.8,8.1],
  Netherlands: [2.6,2.3,2.6,2.47,2.5,2.45,2.4,2.4,2.3],
  Poland:      [4.4,4.2,4.5,4.46,4.7,4.62,4.6,4.6,4.6],
  Romania:     [4.5,4.2,4.5,4.2,4.5,4.91,5.4,5.3,5.6],
  Ukraine:     [5.5,5.4,5.2,4.9,5.2,5.50,5.8,5.9,8.9],
};

const refugeesRaw = {
  Bulgaria:    [3.5,4.0,4.5,4.2,4.3,4.0,3.7,3.4,4.4],
  France:      [2.2,2.7,2.5,2.48,2.2,2.5,2.7,2.7,2.4],
  Georgia:     [7.4,7.7,7.5,7.2,6.9,6.6,6.3,6.0,6.5],
  Moldova:     [4.4,4.1,3.9,3.6,3.3,3.3,3.0,2.8,6.0],
  Netherlands: [2.1,4.0,3.8,3.5,3.2,2.9,2.6,2.3,2.4],
  Poland:      [2.8,3.8,3.6,3.3,3.0,2.7,2.4,2.5,5.9],
  Romania:     [2.7,3.0,2.8,2.56,2.3,2.3,2.1,2.0,4.0],
  Ukraine:     [4.4,4.3,4.6,4.9,4.7,4.4,4.2,4.2,10.0],
};

const fertCompRaw = {
  Bulgaria:    [34.3,43.0,57.7,114,147,80.9,74.2,73.9,102,111,105,97.1,133,95.9,109,109,122,138,131,132,136,139,131,null],
  France:      [259,226,228,211,223,212,192,190,209,152,121,151,141,161,169,168,170,163,178,171,158,163,156,119],
  Georgia:     [50.6,53.0,35.2,33.0,14.4,31.5,53.3,47.5,41.3,40.2,48.3,46.9,46.5,58.1,73.4,68.7,64.5,75.1,65.6,68.8,68.6,100,95.9,83.0],
  Moldova:     [1.77,2.79,17.6,8.14,7.53,8.32,9.00,8.46,11.0,12.5,9.36,11.1,13.0,19.1,24.7,25.9,30.2,41.9,48.6,59.4,51.2,48.8,50.6,40.4],
  Netherlands: [466,409,412,387,364,357,338,353,302,268,238,293,247,290,231,248,267,292,291,274,274,277,273,247],
  Poland:      [108,115,116,116,129,129,162,159,181,158,147,180,170,178,179,164,174,190,190,173,177,155,156,155],
  Romania:     [25.4,32.4,39.4,34.8,38.6,42.6,51.4,40.6,44.6,45.6,48.5,52.5,54.1,49.8,56.2,51.5,60.7,59.9,68.1,83.2,83.6,87.1,98.3,90.3],
  Ukraine:     [12.8,13.5,14.6,15.9,15.8,16.4,17.2,21.6,27.6,32.8,27.3,32.7,38.9,41.4,45.6,44.9,43.2,52.7,61.9,65.4,65.1,75.6,78.5,55.6],
};

const FERT_YEARS = ['1990','1996','2000','2001','2002','2003','2004','2005','2006','2007','2008','2009','2010','2011','2012','2013','2014','2015','2016','2017','2018','2019','2020','2021','2022','2023'];
const fertCropRaw = {
  'Cereals & Legumes': [1602,237,161,248,252,185,282,306,352,433,519,469,492,545,527,555,541,576,698,780,850,832,919,990,600,388],
  'Industrial Crops':  [961,161,64,86.5,86.8,109,117,153,235,292,320,262,342,410,424,447,479,455,572,717,773,736,856,861,732,567],
  'Maize':             [252,13.1,13,19.3,24.3,47.9,84.7,65.9,75.1,127,183,123,185,262,341,440,405,342,411,479,482,528,660,683,470,415],
  'Forage Crops':      [1248,101,35.1,40.7,31.8,31,27.9,25.6,26.6,31.6,29.5,20.8,27.5,29.7,35,33.2,29,25.3,29.2,33.9,28.5,27,32.8,29.2,18.1,17.2],
};

const PEST_YEARS = ['2018','2019','2020','2021','2022','2023'];
const pesticideRaw = {
  'Industrial Crops': [90.8,90.6,92.3,92.4,90.7,92.9],
  'Legumes':          [89.7,89.8,91.1,91.3,87.1,91.2],
  'Maize':            [93.3,92.4,94.4,93.6,92.1,94.0],
  'Forage Crops':     [48.6,51.5,57.2,56.9,53.9,57.0],
  'Total (all crops)':[77.3,77.8,78.6,80.6,59.7,58.3],
};

Chart.defaults.font.family = "'Source Serif 4', Georgia, serif";
Chart.defaults.font.size   = 11;
Chart.defaults.color       = '#4a5568';

function makeLineDatasets(raw, years, highlightOnly = false) {
  return COUNTRIES.map(c => ({
    label: c,
    data: raw[c] ? years.map((_,i) => raw[c][i] ?? null) : [],
    borderColor: highlightOnly && c!=='Ukraine' ? COLORS[c]+'55' : COLORS[c],
    backgroundColor: 'transparent',
    borderWidth: c === 'Ukraine' ? 2.5 : 1.5,
    pointRadius: c === 'Ukraine' ? 3 : 0,
    pointHoverRadius: 5,
    tension: 0.3,
    borderDash: c === 'Ukraine' ? [] : (highlightOnly ? [4,3] : []),
    order: c === 'Ukraine' ? 0 : 1,
  }));
}

function lineChart(id, raw, years) {
  const ctx = document.getElementById(id).getContext('2d');
  return new Chart(ctx, {
    type: 'line',
    data: { labels: years, datasets: makeLineDatasets(raw, years) },
    options: {
      responsive: true, maintainAspectRatio: false,
      interaction: { mode: 'index', intersect: false },
      plugins: {
        legend: { position: 'bottom', labels: { boxWidth: 12, padding: 12 } },
        tooltip: { mode: 'index', intersect: false }
      },
      scales: {
        x: { grid: { color: '#e8dfc8' }, ticks: { maxTicksLimit: 10 } },
        y: { grid: { color: '#e8dfc8' } }
      }
    }
  });
}

const charts = {};
charts.popGrowth     = lineChart('chartPopGrowth',     popGrowthRaw,     YEARS_LONG);
charts.demogPressure = lineChart('chartDemogPressure', demogPressureRaw, YEARS_FSI);
charts.brainDrain    = lineChart('chartBrainDrain',    brainDrainRaw,    YEARS_FSI);
charts.refugees      = lineChart('chartRefugees',      refugeesRaw,      YEARS_FSI);
charts.fertComp      = lineChart('chartFertComp',      fertCompRaw,      YEARS_LONG.slice(0,24));

(function() {
  const CROP_COLORS = ['#2D4739','#005BBB','#4b3034','#CBD7C1'];
  const cropKeys = Object.keys(fertCropRaw);
  const ctx = document.getElementById('chartFertCrop').getContext('2d');
  charts.fertCrop = new Chart(ctx, {
    type: 'bar',
    data: {
      labels: FERT_YEARS,
      datasets: cropKeys.map((k,i) => ({
        label: k,
        data: fertCropRaw[k],
        backgroundColor: CROP_COLORS[i]+'cc',
        borderColor: CROP_COLORS[i],
        borderWidth: 1,
        stack: 'crops',
      }))
    },
    options: {
      responsive: true, maintainAspectRatio: false,
      plugins: { legend: { position: 'bottom', labels: { boxWidth: 12, padding: 10 } } },
      scales: {
        x: { stacked: true, grid: { color: '#e8dfc8' } },
        y: { stacked: true, grid: { color: '#e8dfc8' }, title: { display: true, text: 'Thousands of tonnes' } }
      }
    }
  });
})();

(function() {
  const PEST_COLORS = ['#4b3034','#2D4739','#FFD500','#CBD7C1','#7a8c7e'];
  const keys = Object.keys(pesticideRaw);
  const ctx = document.getElementById('chartPesticide').getContext('2d');
  new Chart(ctx, {
    type: 'line',
    data: {
      labels: PEST_YEARS,
      datasets: keys.map((k,i) => ({
        label: k,
        data: pesticideRaw[k],
        borderColor: PEST_COLORS[i],
        backgroundColor: PEST_COLORS[i]+'22',
        borderWidth: k.includes('Total') ? 2.5 : 1.5,
        borderDash: k.includes('Total') ? [] : [4,3],
        pointRadius: 4,
        tension: 0.2,
        fill: false,
      }))
    },
    options: {
      responsive: true, maintainAspectRatio: false,
      plugins: { legend: { position: 'bottom', labels: { boxWidth: 12, padding: 10 } } },
      scales: {
        x: { grid: { color: '#e8dfc8' } },
        y: { grid: { color: '#e8dfc8' }, min: 40, max: 100,
             title: { display: true, text: '% of land area treated' } }
      }
    }
  });
})();

function horzBar(id, labels, data, maxVal, colors) {
  const ctx = document.getElementById(id).getContext('2d');
  new Chart(ctx, {
    type: 'bar',
    data: {
      labels,
      datasets: [{ data, backgroundColor: colors || '#2D473999', borderColor: colors || '#2D4739', borderWidth: 1 }]
    },
    options: {
      indexAxis: 'y',
      responsive: true, maintainAspectRatio: false,
      plugins: { legend: { display: false } },
      scales: {
        x: { max: maxVal, grid: { color: '#e8dfc8' } },
        y: { grid: { display: false } }
      }
    }
  });
}

horzBar('chartRules',
  ['Frequently hinder','Neither','Frequently help','Sometimes help','Sometimes hinder'],
  [112,39,34,27,15], 120,
  ['#4b3034','#7a8c7e','#2D4739','#005BBB','#E3BCB5']
);
horzBar('chartInteraction',
  ['Same work unit','Head of unit','Other units (same ministry)','Other ministries','Specialists on reform','External experts','Political leadership'],
  [91, 80, 59, 56, 33, 39, 30], 100,
  ['#2D4739','#2D4739','#005BBB','#005BBB','#4b3034','#4b3034','#E3BCB5']
);
horzBar('chartExpert',
  ['Often','Rarely','Most of time','Difficult to say','Sometimes','Never','No experience'],
  [63,84,22,21,20,2,12], 90,
  ['#2D4739','#4b3034','#005BBB','#7a8c7e','#CBD7C1','#E3BCB5','#b5c4ad']
);
horzBar('chartHiring',
  ['Professional knowledge','Work experience','Loyalty to superiors','Personal connections','Political connections'],
  [94, 90, 42, 30, 13], 100,
  ['#2D4739','#005BBB','#4b3034','#E3BCB5','#CBD7C1']
);
horzBar('chartDiscrim',
  ['Rank','Tenure','Age','Gender','Sexual orientation','Faith'],
  [22, 18, 20, 10, 0.9, 1], 30,
  ['#4b3034','#4b3034','#FFD500','#7a8c7e','#b5c4ad','#CBD7C1']
);
horzBar('chartWhistle',
  ['Difficult to say','Strongly agree','Rather disagree','Strongly disagree','Rather agree'],
  [91,39,36,30,25], 100
);
horzBar('chartPreference',
  ['Strongly prefer civil service','Somewhat prefer civil service','Difficult to say','Somewhat prefer private','Strongly prefer private'],
  [88,83,25,17,6], 100,
  ['#2D4739','#005BBB','#7a8c7e','#4b3034','#E3BCB5']
);

function applyHighlight(chart, raw, years, highlightOnly) {
  chart.data.datasets = makeLineDatasets(raw, years, highlightOnly);
  chart.update();
}

document.querySelectorAll('.ctrl-btn[data-chart]').forEach(btn => {
  btn.addEventListener('click', function() {
    const chartName = this.dataset.chart;
    const action = this.dataset.action;
    const group = this.closest('.chart-controls');
    group.querySelectorAll('.ctrl-btn').forEach(b => b.classList.remove('active'));
    this.classList.add('active');
    const highlight = action === 'ukraine';
    const rawMap   = { popGrowth: popGrowthRaw, demogPressure: demogPressureRaw, fertComp: fertCompRaw };
    const yearsMap = { popGrowth: YEARS_LONG,   demogPressure: YEARS_FSI,        fertComp: YEARS_LONG.slice(0,24) };
    if (rawMap[chartName]) applyHighlight(charts[chartName], rawMap[chartName], yearsMap[chartName], highlight);
  });
});

function switchFSITab(tab) {
  document.getElementById('fsi-panel-brain').style.display   = tab==='brain'   ? 'block' : 'none';
  document.getElementById('fsi-panel-refugee').style.display = tab==='refugee' ? 'block' : 'none';
  document.getElementById('tab-brain').classList.toggle('active',   tab==='brain');
  document.getElementById('tab-refugee').classList.toggle('active', tab==='refugee');
}

document.querySelectorAll('.toc-nav a').forEach(a => {
  a.addEventListener('click', e => {
    e.preventDefault();
    document.querySelector(a.getAttribute('href')).scrollIntoView({ behavior: 'smooth' });
  });
});
</script>
