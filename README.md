<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Michelle · Automation & Integration Specialist</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Mono:ital,wght@0,300;0,400;0,500;1,300&family=Sora:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #0a0a0f;
  --surface: #111118;
  --surface2: #18181f;
  --border: rgba(255,255,255,0.07);
  --border2: rgba(255,255,255,0.12);
  --text: #f0f0f5;
  --muted: #8888a0;
  --dim: #55556a;
  --accent: #00e5a0;
  --accent2: #4f7fff;
  --accent3: #ff6b6b;
  --amber: #ffb347;
  --mono: 'DM Mono', monospace;
  --sans: 'Sora', sans-serif;
}
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body {
  background: var(--bg);
  color: var(--text);
  font-family: var(--sans);
  font-size: 15px;
  line-height: 1.6;
  min-height: 100vh;
  overflow-x: hidden;
}

/* Grid background */
body::before {
  content: '';
  position: fixed;
  inset: 0;
  background-image:
    linear-gradient(rgba(0,229,160,0.03) 1px, transparent 1px),
    linear-gradient(90deg, rgba(0,229,160,0.03) 1px, transparent 1px);
  background-size: 40px 40px;
  pointer-events: none;
  z-index: 0;
}

/* NAV */
nav {
  position: fixed;
  top: 0; left: 0; right: 0;
  z-index: 100;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem 2.5rem;
  background: rgba(10,10,15,0.85);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid var(--border);
}
.nav-logo {
  font-family: var(--mono);
  font-size: 13px;
  color: var(--accent);
  letter-spacing: 0.04em;
}
.nav-links {
  display: flex;
  gap: 2rem;
  list-style: none;
}
.nav-links a {
  font-size: 12px;
  color: var(--muted);
  text-decoration: none;
  font-family: var(--mono);
  letter-spacing: 0.05em;
  transition: color 0.2s;
}
.nav-links a:hover { color: var(--text); }
.nav-cta {
  font-size: 12px;
  font-family: var(--mono);
  padding: 6px 16px;
  background: transparent;
  border: 1px solid var(--accent);
  color: var(--accent);
  border-radius: 4px;
  cursor: pointer;
  text-decoration: none;
  transition: background 0.2s, color 0.2s;
}
.nav-cta:hover { background: var(--accent); color: var(--bg); }

/* MAIN WRAPPER */
main { position: relative; z-index: 1; }

/* HERO */
.hero {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 8rem 2.5rem 4rem;
  max-width: 900px;
  margin: 0 auto;
}
.hero-eyebrow {
  font-family: var(--mono);
  font-size: 12px;
  color: var(--accent);
  letter-spacing: 0.1em;
  margin-bottom: 1.5rem;
  display: flex;
  align-items: center;
  gap: 10px;
}
.hero-eyebrow::before {
  content: '';
  display: inline-block;
  width: 24px;
  height: 1px;
  background: var(--accent);
}
.hero h1 {
  font-size: clamp(2.2rem, 5vw, 3.8rem);
  font-weight: 600;
  line-height: 1.15;
  margin-bottom: 1.5rem;
  letter-spacing: -0.02em;
}
.hero h1 span {
  color: transparent;
  -webkit-text-stroke: 1px rgba(255,255,255,0.3);
}
.hero h1 em {
  font-style: normal;
  color: var(--accent);
}
.hero-summary {
  font-size: 16px;
  color: var(--muted);
  max-width: 580px;
  line-height: 1.75;
  margin-bottom: 2.5rem;
}
.hero-actions {
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
  margin-bottom: 4rem;
}
.btn {
  font-family: var(--mono);
  font-size: 12px;
  letter-spacing: 0.06em;
  padding: 10px 22px;
  border-radius: 4px;
  cursor: pointer;
  text-decoration: none;
  transition: all 0.2s;
  display: inline-flex;
  align-items: center;
  gap: 8px;
  border: none;
}
.btn-accent { background: var(--accent); color: var(--bg); }
.btn-accent:hover { background: #00c88a; }
.btn-ghost { background: transparent; border: 1px solid var(--border2); color: var(--muted); }
.btn-ghost:hover { border-color: var(--text); color: var(--text); }

.hero-stats {
  display: flex;
  gap: 3rem;
  padding-top: 2.5rem;
  border-top: 1px solid var(--border);
}
.stat-num {
  font-size: 2rem;
  font-weight: 600;
  color: var(--text);
  line-height: 1;
}
.stat-num span { color: var(--accent); }
.stat-label {
  font-size: 12px;
  color: var(--dim);
  font-family: var(--mono);
  margin-top: 4px;
}

/* SECTION COMMON */
section {
  max-width: 960px;
  margin: 0 auto;
  padding: 5rem 2.5rem;
  border-top: 1px solid var(--border);
}
.section-header {
  display: flex;
  align-items: baseline;
  gap: 1rem;
  margin-bottom: 3rem;
}
.section-num {
  font-family: var(--mono);
  font-size: 11px;
  color: var(--accent);
  letter-spacing: 0.1em;
}
.section-title {
  font-size: 1.5rem;
  font-weight: 500;
  letter-spacing: -0.01em;
}
.section-line {
  flex: 1;
  height: 1px;
  background: var(--border);
}

/* PROJECTS */
.projects-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
}
.project-card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 1.5rem;
  transition: border-color 0.2s, transform 0.2s;
  position: relative;
  overflow: hidden;
}
.project-card::before {
  content: '';
  position: absolute;
  top: 0; left: 0;
  right: 0; height: 2px;
  background: var(--card-accent, var(--accent));
  opacity: 0;
  transition: opacity 0.2s;
}
.project-card:hover { border-color: var(--border2); transform: translateY(-2px); }
.project-card:hover::before { opacity: 1; }
.project-card.wide { grid-column: span 2; }

.card-top {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  margin-bottom: 1rem;
}
.card-icon {
  width: 36px; height: 36px;
  border-radius: 6px;
  display: flex; align-items: center; justify-content: center;
  font-size: 17px;
}
.card-role {
  font-family: var(--mono);
  font-size: 10px;
  color: var(--muted);
  background: var(--surface2);
  padding: 3px 8px;
  border-radius: 20px;
  border: 1px solid var(--border);
}
.card-title {
  font-size: 15px;
  font-weight: 500;
  margin-bottom: 0.5rem;
  line-height: 1.3;
}
.card-desc {
  font-size: 13px;
  color: var(--muted);
  line-height: 1.65;
  margin-bottom: 1.25rem;
}

/* Flow pipeline */
.flow {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 4px;
  margin-bottom: 1.25rem;
}
.flow-node {
  font-family: var(--mono);
  font-size: 10px;
  padding: 3px 8px;
  border-radius: 3px;
  background: var(--surface2);
  border: 1px solid var(--border);
  color: var(--muted);
  white-space: nowrap;
}
.flow-arrow {
  font-size: 10px;
  color: var(--dim);
}

.tags {
  display: flex;
  flex-wrap: wrap;
  gap: 5px;
}
.tag {
  font-family: var(--mono);
  font-size: 10px;
  padding: 2px 8px;
  border-radius: 20px;
  border: 1px solid var(--border);
  color: var(--dim);
}
.tag.accent { border-color: rgba(0,229,160,0.3); color: var(--accent); }
.tag.blue { border-color: rgba(79,127,255,0.3); color: var(--accent2); }
.tag.amber { border-color: rgba(255,179,71,0.3); color: var(--amber); }

/* COLOR VARIANTS */
.c-green { --card-accent: #00e5a0; }
.c-green .card-icon { background: rgba(0,229,160,0.1); color: var(--accent); }
.c-blue { --card-accent: #4f7fff; }
.c-blue .card-icon { background: rgba(79,127,255,0.1); color: var(--accent2); }
.c-amber { --card-accent: #ffb347; }
.c-amber .card-icon { background: rgba(255,179,71,0.1); color: var(--amber); }
.c-red { --card-accent: #ff6b6b; }
.c-red .card-icon { background: rgba(255,107,107,0.1); color: var(--accent3); }
.c-purple { --card-accent: #a78bfa; }
.c-purple .card-icon { background: rgba(167,139,250,0.1); color: #a78bfa; }
.c-teal { --card-accent: #2dd4bf; }
.c-teal .card-icon { background: rgba(45,212,191,0.1); color: #2dd4bf; }
.c-coral { --card-accent: #fb923c; }
.c-coral .card-icon { background: rgba(251,146,60,0.1); color: #fb923c; }

/* SKILLS */
.skills-categories {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
}
.skill-group {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 1.25rem;
}
.skill-group-title {
  font-family: var(--mono);
  font-size: 10px;
  color: var(--accent);
  letter-spacing: 0.08em;
  margin-bottom: 1rem;
  text-transform: uppercase;
}
.skill-list {
  display: flex;
  flex-direction: column;
  gap: 8px;
}
.skill-item {
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 12px;
  color: var(--muted);
}
.skill-dot {
  width: 5px; height: 5px;
  border-radius: 50%;
  flex-shrink: 0;
}

/* TOOLS STRIP */
.tools-strip {
  margin-top: 2rem;
  padding: 1.25rem 1.5rem;
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 8px;
  display: flex;
  align-items: center;
  gap: 1rem;
  flex-wrap: wrap;
}
.tools-label {
  font-family: var(--mono);
  font-size: 10px;
  color: var(--dim);
  letter-spacing: 0.08em;
  white-space: nowrap;
}
.tools-divider { width: 1px; height: 20px; background: var(--border); }
.tools-items {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}
.tool-pill {
  font-family: var(--mono);
  font-size: 11px;
  padding: 4px 10px;
  background: var(--surface2);
  border: 1px solid var(--border);
  border-radius: 20px;
  color: var(--muted);
}

/* ABOUT */
.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
  align-items: start;
}
.about-text p {
  font-size: 15px;
  color: var(--muted);
  line-height: 1.8;
  margin-bottom: 1rem;
}
.about-text p strong { color: var(--text); font-weight: 500; }
.about-meta {
  display: flex;
  flex-direction: column;
  gap: 12px;
}
.meta-item {
  display: flex;
  align-items: flex-start;
  gap: 12px;
  padding: 1rem;
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 8px;
}
.meta-icon { font-size: 18px; flex-shrink: 0; }
.meta-label { font-family: var(--mono); font-size: 10px; color: var(--dim); margin-bottom: 2px; }
.meta-value { font-size: 13px; color: var(--text); }

/* CONTACT */
.contact-inner {
  text-align: center;
  padding: 3rem 2rem;
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 12px;
  position: relative;
  overflow: hidden;
}
.contact-inner::after {
  content: '';
  position: absolute;
  inset: 0;
  background: radial-gradient(ellipse at center top, rgba(0,229,160,0.06) 0%, transparent 70%);
  pointer-events: none;
}
.contact-inner h2 {
  font-size: 1.8rem;
  font-weight: 500;
  margin-bottom: 0.75rem;
  letter-spacing: -0.02em;
}
.contact-inner p { color: var(--muted); margin-bottom: 2rem; font-size: 14px; }
.contact-links { display: flex; gap: 12px; justify-content: center; flex-wrap: wrap; }

/* FOOTER */
footer {
  border-top: 1px solid var(--border);
  padding: 2rem 2.5rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 960px;
  margin: 0 auto;
}
footer p { font-family: var(--mono); font-size: 11px; color: var(--dim); }

/* ANIMATIONS */
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}
.hero > * {
  animation: fadeUp 0.6s ease both;
}
.hero-eyebrow { animation-delay: 0.1s; }
.hero h1 { animation-delay: 0.2s; }
.hero-summary { animation-delay: 0.3s; }
.hero-actions { animation-delay: 0.4s; }
.hero-stats { animation-delay: 0.5s; }

/* RESPONSIVE */
@media (max-width: 700px) {
  nav { padding: 1rem 1.25rem; }
  .nav-links { display: none; }
  .hero { padding: 7rem 1.25rem 3rem; }
  .hero h1 { font-size: 2rem; }
  .hero-stats { gap: 1.5rem; flex-wrap: wrap; }
  section { padding: 3rem 1.25rem; }
  .projects-grid { grid-template-columns: 1fr; }
  .project-card.wide { grid-column: span 1; }
  .skills-categories { grid-template-columns: 1fr; }
  .about-grid { grid-template-columns: 1fr; }
  footer { flex-direction: column; gap: 1rem; text-align: center; }
}
</style>
</head>
<body>

<nav>
  <span class="nav-logo">michelle.dev</span>
  <ul class="nav-links">
    <li><a href="#projects">projects</a></li>
    <li><a href="#skills">skills</a></li>
    <li><a href="#about">about</a></li>
    <li><a href="#contact">contact</a></li>
  </ul>
  <a href="#contact" class="nav-cta">hire me →</a>
</nav>

<main>

<!-- HERO -->
<div class="hero">
  <div class="hero-eyebrow">Available for freelance · Remote · Philippines</div>
  <h1>
    Google Workspace <em>Automation</em><br>
    &amp; <span>API Integration</span><br>
    Specialist
  </h1>
  <p class="hero-summary">
    I build automated business workflows using Google Apps Script, APIs, webhooks, and Google Workspace tools — streamlining reporting, CRM processes, document generation, and data pipelines.
  </p>
  <div class="hero-actions">
    <a href="#projects" class="btn btn-accent">view projects ↓</a>
    <a href="https://github.com/mitchsanchez29" class="btn btn-ghost" target="_blank">GitHub ↗</a>
    <a href="#contact" class="btn btn-ghost">get in touch</a>
  </div>
  <div class="hero-stats">
    <div>
      <div class="stat-num">9<span>+</span></div>
      <div class="stat-label">// automation projects</div>
    </div>
    <div>
      <div class="stat-num">15<span>+</span></div>
      <div class="stat-label">// tools & APIs</div>
    </div>
    <div>
      <div class="stat-num">5<span>+</span></div>
      <div class="stat-label">// reporting dashboards</div>
    </div>
  </div>
</div>

<!-- PROJECTS -->
<section id="projects">
  <div class="section-header">
    <span class="section-num">01 //</span>
    <h2 class="section-title">Projects</h2>
    <div class="section-line"></div>
  </div>

  <div class="projects-grid">

    <!-- 1. Quotation CRM -->
    <div class="project-card c-green">
      <div class="card-top">
        <div class="card-icon">📄</div>
        <span class="card-role">sole builder</span>
      </div>
      <div class="card-title">Automated Quotation & CRM System</div>
      <div class="flow">
        <span class="flow-node">Google Forms</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Sheets</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Docs</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">PDF</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Gmail</span>
      </div>
      <div class="card-desc">
        Auto-generates unique quote numbers, produces PDF documents via Apps Script, tracks status in Sheets, and delivers to clients via Gmail — all triggered on form submission.
      </div>
      <div class="tags">
        <span class="tag accent">Apps Script</span>
        <span class="tag">CRM</span>
        <span class="tag">PDF Generation</span>
        <span class="tag">Drive</span>
      </div>
    </div>

    <!-- 2. YouTube Analytics -->
    <div class="project-card c-blue">
      <div class="card-top">
        <div class="card-icon">📊</div>
        <span class="card-role">sole builder</span>
      </div>
      <div class="card-title">YouTube Analytics Reporting Pipeline</div>
      <div class="flow">
        <span class="flow-node">YouTube API</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Apps Script</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Sheets</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Looker Studio</span>
      </div>
      <div class="card-desc">
        Daily automated data pull from YouTube Analytics API into a Sheets data warehouse, powering a live Looker Studio dashboard for channel performance reporting.
      </div>
      <div class="tags">
        <span class="tag blue">YouTube API</span>
        <span class="tag">Looker Studio</span>
        <span class="tag">REST API</span>
        <span class="tag">JSON</span>
      </div>
    </div>

    <!-- 3. Facebook Ads Dashboard -->
    <div class="project-card c-blue">
      <div class="card-top">
        <div class="card-icon">📱</div>
        <span class="card-role">sole builder</span>
      </div>
      <div class="card-title">Facebook Ads Performance Dashboard</div>
      <div class="flow">
        <span class="flow-node">Facebook Ads</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">OAuth Token</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Partner Connector</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Looker Studio</span>
      </div>
      <div class="card-desc">
        Connected Facebook Ads to Looker Studio via OAuth token and partner connector. Live dashboard shows campaign spend, reach, CPM, CTR, and results — no manual exports needed.
      </div>
      <div class="tags">
        <span class="tag blue">Facebook Ads API</span>
        <span class="tag">OAuth Token</span>
        <span class="tag">Looker Studio</span>
        <span class="tag">Marketing Analytics</span>
      </div>
    </div>

    <!-- 4. Google Ads + Analytics Dashboard -->
    <div class="project-card c-amber">
      <div class="card-top">
        <div class="card-icon">📈</div>
        <span class="card-role">sole builder</span>
      </div>
      <div class="card-title">Google Ads & Analytics Performance Report</div>
      <div class="flow">
        <span class="flow-node">Google Ads</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Google Analytics</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Native Connectors</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Looker Studio</span>
      </div>
      <div class="card-desc">
        Multi-page Looker Studio report connected to Google Ads and Analytics via native connectors. Features Week-over-Week, Month-over-Month, and Year-to-Date views across separate report pages.
      </div>
      <div class="tags">
        <span class="tag amber">Google Ads</span>
        <span class="tag">Google Analytics</span>
        <span class="tag">Looker Studio</span>
        <span class="tag">WoW · MoM · YTD</span>
      </div>
    </div>

    <!-- 5. Airtable / Zapier -->
    <div class="project-card c-purple">
      <div class="card-top">
        <div class="card-icon">🗂️</div>
        <span class="card-role">team project</span>
      </div>
      <div class="card-title">Closer & Setter EOD Data Pipeline</div>
      <div class="flow">
        <span class="flow-node">Airtable Form</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Zapier</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Google Sheets</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Looker Studio</span>
      </div>
      <div class="card-desc">
        My role: daily monitoring, data cleaning, and structuring of EOD sales data (cash collected, payments, commissions) submitted by closers and setters — then building and maintaining the Looker Studio performance report.
      </div>
      <div class="tags">
        <span class="tag">Airtable</span>
        <span class="tag">Zapier</span>
        <span class="tag">Data Cleaning</span>
        <span class="tag">Looker Studio</span>
        <span class="tag">Commissions</span>
      </div>
    </div>

    <!-- 6. Upcoming & Delayed Payments Tracker -->
    <div class="project-card c-coral">
      <div class="card-top">
        <div class="card-icon">💰</div>
        <span class="card-role">sole builder</span>
      </div>
      <div class="card-title">Upcoming & Delayed Payments Tracker</div>
      <div class="flow">
        <span class="flow-node">Installment Tracker</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Apps Script</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Upcoming / Delayed</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Slack + Looker Studio</span>
      </div>
      <div class="card-desc">
        Apps Script reads the master installment tracker, calculates payment aging, and auto-routes clients: 0–90 days due → Upcoming sheet, 1+ days overdue → Delayed sheet + Slack follow-up alert. Paid entries are auto-removed. Two separate Looker Studio dashboards for each sheet.
      </div>
      <div class="tags">
        <span class="tag accent">Apps Script</span>
        <span class="tag">Slack Webhook</span>
        <span class="tag">Looker Studio</span>
        <span class="tag">Aging Logic</span>
        <span class="tag">Finance</span>
      </div>
    </div>

    <!-- 7. Payment Performance Dashboard -->
    <div class="project-card c-teal">
      <div class="card-top">
        <div class="card-icon">📊</div>
        <span class="card-role">sole builder</span>
      </div>
      <div class="card-title">Payment Performance Dashboard</div>
      <div class="flow">
        <span class="flow-node">Payment Tracker</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Google Sheets</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Looker Studio</span>
      </div>
      <div class="card-desc">
        Looker Studio dashboard using a Google Sheets payment tracker as data source. Visualizes total payments, collected amounts, pending balances, and payment status — centralized, real-time, no manual checking needed.
      </div>
      <div class="tags">
        <span class="tag">Looker Studio</span>
        <span class="tag">Google Sheets</span>
        <span class="tag">Financial Reporting</span>
        <span class="tag">Data Visualization</span>
      </div>
    </div>

    <!-- 8. Financial Dashboard & P&L -->
    <div class="project-card c-green">
      <div class="card-top">
        <div class="card-icon">📉</div>
        <span class="card-role">sole builder</span>
      </div>
      <div class="card-title">Financial Dashboard & Profit/Loss Reporting</div>
      <div class="flow">
        <span class="flow-node">Income + Expenses</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Google Sheets</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">P&L Dashboard</span>
      </div>
      <div class="card-desc">
        Google Sheets dashboard consolidating income, expenses, net cash collected, and profit/loss. Monthly and quarterly performance tracking with automated calculations — business performance visible in one place.
      </div>
      <div class="tags">
        <span class="tag accent">Google Sheets</span>
        <span class="tag">P&L Reporting</span>
        <span class="tag">Monthly · Quarterly</span>
        <span class="tag">Financial Dashboard</span>
      </div>
    </div>

    <!-- 9. Webhook & Notifications -->
    <div class="project-card c-red">
      <div class="card-top">
        <div class="card-icon">🔔</div>
        <span class="card-role">sole builder</span>
      </div>
      <div class="card-title">Webhook & Notification Automation</div>
      <div class="flow">
        <span class="flow-node">Trigger Event</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Apps Script</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Webhook</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Slack</span>
      </div>
      <div class="card-desc">
        Real-time Slack notifications triggered by workflow events via webhook integrations. Eliminates manual status updates and keeps teams in sync automatically.
      </div>
      <div class="tags">
        <span class="tag">Webhooks</span>
        <span class="tag">Slack</span>
        <span class="tag">REST API</span>
        <span class="tag">Real-time</span>
      </div>
    </div>

    <!-- 10. AI Workflows -->
    <div class="project-card c-purple">
      <div class="card-top">
        <div class="card-icon">🤖</div>
        <span class="card-role">in development</span>
      </div>
      <div class="card-title">AI-Powered Workflow Automation</div>
      <div class="flow">
        <span class="flow-node">Apps Script</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">ChatGPT API</span>
        <span class="flow-arrow">→</span>
        <span class="flow-node">Gmail draft</span>
      </div>
      <div class="card-desc">
        Integrating ChatGPT API with Google Apps Script for AI-assisted email drafting and intelligent business workflow automation. Actively expanding this capability.
      </div>
      <div class="tags">
        <span class="tag">ChatGPT API</span>
        <span class="tag">AI Integration</span>
        <span class="tag">Gmail</span>
        <span class="tag">Learning</span>
      </div>
    </div>

  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="section-header">
    <span class="section-num">02 //</span>
    <h2 class="section-title">Skills & Tools</h2>
    <div class="section-line"></div>
  </div>

  <div class="skills-categories">
    <div class="skill-group">
      <div class="skill-group-title">// automation</div>
      <div class="skill-list">
        <div class="skill-item"><span class="skill-dot" style="background:var(--accent)"></span>Google Apps Script</div>
        <div class="skill-item"><span class="skill-dot" style="background:var(--accent)"></span>Google Sheets Automation</div>
        <div class="skill-item"><span class="skill-dot" style="background:var(--accent)"></span>Gmail Automation</div>
        <div class="skill-item"><span class="skill-dot" style="background:var(--accent)"></span>Google Docs Generation</div>
        <div class="skill-item"><span class="skill-dot" style="background:var(--accent)"></span>Google Drive Automation</div>
        <div class="skill-item"><span class="skill-dot" style="background:var(--accent)"></span>Google Forms</div>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-title">// apis & integrations</div>
      <div class="skill-list">
        <div class="skill-item"><span class="skill-dot" style="background:var(--accent2)"></span>REST APIs</div>
        <div class="skill-item"><span class="skill-dot" style="background:var(--accent2)"></span>JSON</div>
        <div class="skill-item"><span class="skill-dot" style="background:var(--accent2)"></span>Webhooks</div>
        <div class="skill-item"><span class="skill-dot" style="background:var(--accent2)"></span>YouTube Analytics API</div>
        <div class="skill-item"><span class="skill-dot" style="background:var(--accent2)"></span>Facebook Ads API</div>
        <div class="skill-item"><span class="skill-dot" style="background:var(--accent2)"></span>ChatGPT API (learning)</div>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-title">// reporting & data</div>
      <div class="skill-list">
        <div class="skill-item"><span class="skill-dot" style="background:var(--amber)"></span>Looker Studio</div>
        <div class="skill-item"><span class="skill-dot" style="background:var(--amber)"></span>Data Cleaning</div>
        <div class="skill-item"><span class="skill-dot" style="background:var(--amber)"></span>Data Merging</div>
        <div class="skill-item"><span class="skill-dot" style="background:var(--amber)"></span>Financial Reporting</div>
        <div class="skill-item"><span class="skill-dot" style="background:var(--amber)"></span>P&L Dashboards</div>
        <div class="skill-item"><span class="skill-dot" style="background:var(--amber)"></span>CRM Automation</div>
        <div class="skill-item"><span class="skill-dot" style="background:var(--amber)"></span>Workflow Automation</div>
      </div>
    </div>
  </div>

  <div class="tools-strip">
    <span class="tools-label">ALSO WORKED WITH</span>
    <div class="tools-divider"></div>
    <div class="tools-items">
      <span class="tool-pill">Zapier</span>
      <span class="tool-pill">Slack</span>
      <span class="tool-pill">Google Ads</span>
      <span class="tool-pill">Facebook Ads</span>
      <span class="tool-pill">Airtable</span>
      <span class="tool-pill">PDF Generation</span>
      <span class="tool-pill">Google Drive API</span>
      <span class="tool-pill">Looker Studio Connectors</span>
      <span class="tool-pill">UrlFetchApp</span>
      <span class="tool-pill">ChatGPT API</span>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="section-header">
    <span class="section-num">03 //</span>
    <h2 class="section-title">About</h2>
    <div class="section-line"></div>
  </div>

  <div class="about-grid">
    <div class="about-text">
      <p>
        I'm <strong>Michelle</strong>, a Google Workspace Automation & API Integration Specialist based in the Philippines. I turn repetitive manual tasks into reliable automated systems — so teams can focus on what actually matters.
      </p>
      <p>
        My work spans the full automation stack: from building <strong>Google Apps Script pipelines</strong> that generate PDFs and send emails, to connecting <strong>third-party APIs</strong> like YouTube Analytics and ChatGPT, to building <strong>Looker Studio dashboards</strong> that give decision-makers clear, real-time reporting.
      </p>
      <p>
        I also bring a strong eye for <strong>data quality</strong> — cleaning, merging, and structuring messy datasets before they hit any report. Clean data in, trustworthy insights out.
      </p>
    </div>
    <div class="about-meta">
      <div class="meta-item">
        <span class="meta-icon">📍</span>
        <div>
          <div class="meta-label">LOCATION</div>
          <div class="meta-value">Philippines · Remote-ready</div>
        </div>
      </div>
      <div class="meta-item">
        <span class="meta-icon">💼</span>
        <div>
          <div class="meta-label">AVAILABILITY</div>
          <div class="meta-value">Open to freelance & full-time</div>
        </div>
      </div>
      <div class="meta-item">
        <span class="meta-icon">🎯</span>
        <div>
          <div class="meta-label">SPECIALIZATION</div>
          <div class="meta-value">Google Workspace · APIs · Reporting</div>
        </div>
      </div>
      <div class="meta-item">
        <span class="meta-icon">📡</span>
        <div>
          <div class="meta-label">PLATFORMS</div>
          <div class="meta-value">OnlineJobs.ph · Upwork</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-header">
    <span class="section-num">04 //</span>
    <h2 class="section-title">Get in Touch</h2>
    <div class="section-line"></div>
  </div>

  <div class="contact-inner">
    <h2>Let's build something automated.</h2>
    <p>Available for freelance projects, VA roles, and automation consulting. Based in the Philippines — remote-ready worldwide.</p>
    <div class="contact-links">
      <a href="mailto:sanchezmitch77@email.com" class="btn btn-accent">email me →</a>
      <a href="https://github.com/mitchsanchez29" class="btn btn-ghost" target="_blank">GitHub ↗</a>
      <a href="https://v2.onlinejobs.ph/jobseekers/info/1257742" class="btn btn-ghost" target="_blank">OnlineJobs.ph ↗</a>
    </div>
  </div>
</section>

</main>

<footer>
  <p>// michelle · google workspace automation specialist</p>
  <p>// built with HTML · CSS · hosted on GitHub Pages</p>
</footer>

</body>
</html>
