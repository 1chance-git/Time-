# TimelineAI - Project Structure

Welcome to the official **TimelineAI** repository.

This document outlines the full structure of the project.  
Every folder and file plays a key role in building a **monolithic**, **modular**, and **scalable** TimeChain TimelineAI system.

---

## Main Directory Layout

```plaintext
timelineai/
│
├── .github/
│   ├── workflows/
│   ├── ISSUE_TEMPLATE.md
│   └── PULL_REQUEST_TEMPLATE.md
│
├── assets/
│   ├── logo.png
│   └── images/
│       └── background.jpg
│
├── docs/
│   ├── roadmap.md
│   ├── business_model.md
│   └── user_guide.md
│
├── public/
│   ├── index.html
│   ├── manifest.json
│   ├── service-worker.js
│   └── robots.txt
│
├── src/
│   ├── components/
│   │   ├── TimelineView.js
│   │   ├── Suggestions.js
│   │   └── Header.js
│   ├── utils/
│   │   ├── dateFormatter.js
│   │   └── apiCalls.js
│   ├── styles/
│   │   ├── index.css
│   │   ├── timeline.css
│   │   └── header.css
│   ├── App.js
│   └── index.js
│
├── tests/
│   ├── timeline.test.js
│   └── suggestions.test.js
│
├── .gitignore
├── LICENSE
├── README.md
├── package.json
├── package-lock.json
└── CONTRIBUTING.md
