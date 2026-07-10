# 🌐 SPONA Intl. Management Repository

Welcome to the internal administration and code repository for **SPONA Intl. (The Student-led Peer Outreach and Neuroscience Association)**. 

This repository hosts our public-facing informational website via GitHub Pages. 

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

To update the website, open the `index.html` file, click the **pencil icon (Edit)**, and insert the relevant code snippets below. Always verify your changes by clicking **Commit changes**.

### 1. Adding Recent Mini-Project Posts (Resources Collection)
When adding student review papers, posters, animations, or translated works, copy and paste this code layout inside your resource list:

```html
<li>
    <strong>[Category - e.g., Review Paper / Poster / Animation / Translation]:</strong> 
    <a href="INSERT_LINK_HERE" target="_blank">"Title of the Project/Resource"</a> 
    <br><small style="color: #94a3b8;">Contributors: SI-XX-XX-XXXXXX, SI-YY-YY-YYYYYY</small>
</li>
```

* **Live Example (Animation with UIDs):**
  ```html
  <li>
      <strong>Animation:</strong> <a href="https://youtube.com..." target="_blank">"Action Potentials Visualized"</a> 
      <br><small style="color: #94a3b8;">Contributors: SI-CN-MA-400125, SI-US-DD-402911</small>
  </li>
  ```
* **Live Example (Translated Paper with UIDs):**
  ```html
  <li>
      <strong>Translated Paper:</strong> <a href="https://google.com..." target="_blank">"Synaptic Pruning Summary (Spanish Edition)"</a> 
      <br><small style="color: #94a3b8;">Contributors: SI-MX-MT-500147</small>
  </li>
  ```

### 2. Adding New Events to the Schedule
To announce an upcoming workshop, regional study group, or global meeting, copy and paste this event block:

```html
<div class="card" style="border-left: 4px solid var(--accent-color);">
    <h3>📅 [Event Title]</h3>
    <p><strong>Date & Time:</strong> [Month Day, Year @ Time UTC]</p>
    <p><strong>Description:</strong> [Brief 1-2 sentence overview of the event.]</p>
    <p><a href="INSERT_REGISTRATION_OR_STREAM_LINK" target="_blank">👉 Access Event Here</a></p>
</div>
```

---

## 🚦 Pre-Publishing Checklist
1. **UID Syntax Check:** Ensure the UID strictly follows the `SI-[Country]-[Role]-[6Digits]` pattern before committing. Never publish a student's real name alongside their UID on this public site.
2. **Zero-Data Platform Integrity:** Do not paste any JavaScript analytic trackers or background user loggers into `index.html`.
3. **Safe Form Redirection:** Route event registration actions securely to external third-party form providers (e.g., Google Forms).
