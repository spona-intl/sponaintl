# 🌐 SPONA Intl. Management Repository

Welcome to the internal administration and code repository for **SPONA Intl. (The Student-led Peer Outreach and Neuroscience Association)**. This repository hosts our public-facing informational website via GitHub Pages.

---

## 🆔 Student UID Formatting Rule

All student contributors must be credited using their official SPONA Unique Identifier.

* **Structure:** `SI-[2-Letter Country Code]-[Role Abbreviation]-[6-Digit Number]`
* **Official Role Abbreviation Guide:**
  * `CW` = Content Writer
  * `RA` = Research Analyst
  * `DD` = Digital Designer
  * `MA` = Media Animator
  * `MT` = Multilingual Translator
* **Examples:**
  * `SI-CN-RA-100245` (Research Analyst from China)
  * `SI-US-MA-301984` (Media Animator from the United States)
  * `SI-GB-CW-220411` (Content Writer from the United Kingdom)

---

## 🛠️ Website Contribution & Update Guidelines

To update the website, locate the correct target page (`index.html`, `resources.html`, or `events.html`), click the **pencil icon (Edit)**, insert the relevant code layouts below, and verify your changes by clicking **Commit changes**.

### 1. Adding Recent Peer Releases to the Homepage (index.html)
To feature a newly released project on the home page runway, copy the template below and paste it as the first item inside the `<div class="horizontal-scroll-runway">` container in `index.html`. 

> 📌 **Note:** The entire card component is a clickable link anchor. Keep descriptions brief to ensure clean horizontal mobile scrolling.

```html
<!-- START NEW RUNWAY CARD -->
<a href="INSERT_TARGET_PAGE.html" class="scroll-item-card">
  <div class="card-top-meta">
    <span>[Type - e.g., Review Paper / Translation / Animation]</span>
    <span style="color:var(--text-muted)">[Month Day, Year]</span>
  </div>
  <h3>[Short Project Title]</h3>
  <p>[Ultra-brief 1-sentence description fitting the scroll display footprint.]</p>
  <div class="card-contributor-footer">SI-XX-XX-XXXXXX • SI-XX-XX-XXXXXX</div>
</a>
<!-- END NEW RUNWAY CARD -->
```

* **Live Reference Example:**
```html
<a href="topic-neuroplasticity.html" class="scroll-item-card">
  <div class="card-top-meta"><span>Review Paper</span><span style="color:var(--text-muted)">July 12, 2026</span></div>
  <h3>Neuroplasticity in Adolescents</h3>
  <p>Tracking analysis detailing dynamic cortical reorganizations inside secondary student profiles.</p>
  <div class="card-contributor-footer">SI-CN-RA-100245 • SI-US-RA-105991</div>
</a>
```

### 2. Adding Recent Mini-Project Posts (Resources Collection)
When adding student review papers, posters, animations, or translated works, append a new list item inside the `<ul class="resource-list" id="resourceRegistry">` container in `resources.html`.

> ⚠️ **Critical Requirement:** You must copy all lowercase metadata strings, role codes, and structural tags inside the card's `data-search` attribute. If this is omitted, the live page search indexing filter will not pick up the item.

```html
<li class="resource-card" data-search="insert lowercase searchable terms keywords roles tags and uids here">
  <div class="resource-top">
    <a href="INSERT_LINK_HERE" target="_blank" rel="noopener noreferrer" class="resource-link">"Title of the Project/Resource"</a>
    <span class="badge">[ROLE ABBREVIATION - e.g., RA]</span>
  </div>
  <p>A brief 1-2 sentence description detailing the metrics, scope, or clinical data explored in this cohort mini-project.</p>
  <div class="uid-container">
    <span class="uid-token">SI-XX-XX-XXXXXX</span>
  </div>
</li>
```

* **Live Example (Animation with searchable attributes & UIDs):**
```html
<li class="resource-card" data-search="action potentials visualized video animations media animator ma dd digital designer si-gb-ma-300412 si-ca-dd-200951">
  <div class="resource-top">
    <a href="https://youtube.com" target="_blank" rel="noopener noreferrer" class="resource-link">"Action Potentials Visualized" Video Animation</a>
    <span class="badge">MA (Media Animator)</span>
  </div>
  <p>A sequence of high-fidelity vector rendering models depicting cellular membrane voltage changes during neural firings.</p>
  <div class="uid-container">
    <span class="uid-token">SI-GB-MA-300412</span>
    <span class="uid-token">SI-CA-DD-200951</span>
  </div>
</li>
```

### 3. Adding New Events to the Schedule
To announce an upcoming workshop, regional study group, or global meeting, copy and paste this standard card block inside the main `<div class="container">` component of `events.html`:

```html
<div class="card" style="border-left: 4px solid var(--accent-indigo);">
  <span class="badge" style="margin-bottom: 16px; display: inline-block;">Upcoming Event</span>
  <h3>[Event Title]</h3>
  <p><strong>Timeline Schedule:</strong> [Month Day, Year @ Time UTC]</p>
  <p>[Brief 1-2 sentence overview of what core analysts, translators, or team branches will present.]</p>
  <p style="margin-top: 15px; margin-bottom: 0;">
    <a href="INSERT_REGISTRATION_OR_STREAM_LINK" target="_blank" rel="noopener noreferrer" style="color: var(--accent-indigo); text-decoration: none; font-weight: 700;">👉 Access Event Here</a>
  </p>
</div>
```

---

## 🚦 Pre-Publishing Checklist

1. **UID Syntax Check:** Ensure the identifier strictly follows the `SI-[Country]-[Role]-[6Digits]` pattern before committing. Never publish a student's real name alongside their identifier on this public site.
2. **Zero-Data Platform Integrity:** Do not paste any JavaScript analytic trackers, pixel scripts, or background user tracking scripts into any file.
3. **Safe Form Redirection:** Route event registration actions securely to external third-party form providers (e.g., Google Forms). Do not execute raw text inputs on static sheets.
