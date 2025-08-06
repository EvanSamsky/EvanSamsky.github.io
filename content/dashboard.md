---
title: "COMECON Data Dashboard"
---

<style>
.dashboard-container {
    max-width: 100%;
    margin: 20px 0;
}

.dashboard-description {
    background: #f8f9fa;
    padding: 20px;
    border-radius: 8px;
    margin-bottom: 20px;
    border-left: 4px solid #3498db;
}

.dashboard-frame {
    width: 100%;
    height: 800px;
    border: 1px solid #dee2e6;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.citation-box {
    background: #e9ecef;
    padding: 15px;
    border-radius: 6px;
    margin: 20px 0;
    font-size: 0.9em;
    border-left: 3px solid #6c757d;
}

@media (max-width: 768px) {
    .dashboard-frame {
        height: 600px;
    }
}
</style>

<div class="dashboard-container">

<div class="dashboard-description">
<h3>Interactive COMECON Data Visualization</h3>
<p>This dashboard provides interactive visualizations of historical economic data from the Council for Mutual Economic Assistance (COMECON), the Soviet-led economic organization that coordinated economic planning across socialist countries from 1949-1991.</p>

<p>The visualizations explore economic indicators, trade patterns, and development metrics across COMECON member states, offering insights into the economic structures and relationships within the socialist bloc during the Cold War era.</p>

<div class="citation-box">
<strong>Data Source:</strong> The Vienna Institute for International Economic Studies (wiiw) COMECON Database<br>
<strong>URL:</strong> <a href="https://comecon.wiiw.ac.at" target="_blank" rel="noopener">https://comecon.wiiw.ac.at</a><br>
<em>This database provides comprehensive historical economic data for former socialist countries and their economic relationships within COMECON.</em>
</div>

<p><a href="https://samsky.shinyapps.io/dashboard_deploy/" target="_blank" rel="noopener">🔗 Open dashboard in new tab</a></p>
</div>

<iframe 
    src="https://samsky.shinyapps.io/dashboard_deploy/" 
    class="dashboard-frame"
    title="COMECON Data Dashboard">
</iframe>

<div style="margin-top: 20px; text-align: center; color: #666; font-size: 0.9em;">
<p>If the dashboard doesn't load properly, <a href="https://samsky.shinyapps.io/dashboard_deploy/" target="_blank" rel="noopener">click here to open it in a new window</a>.</p>
</div>

</div>
