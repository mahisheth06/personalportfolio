Mahi Sheth — Personal Portfolio


A responsive, multi-page personal portfolio website built from scratch using vanilla HTML, CSS, and JavaScript — no frameworks, no templates. Features a live GitHub analytics dashboard powered by the GitHub REST API, an interactive resume with JavaScript-animated skill bars, filterable project pages, and embedded project documentation.

**Live site:** [mahisheth06.github.io/personalportfolio](https://mahisheth06.github.io/personalportfolio/)

| Page | Description |
|------|-------------|
| `index.html` | Homepage with hero section, about me, and paginated project carousel |
| `analytics.html` | Live GitHub analytics dashboard — commit activity, language breakdown, repo stats |
| `resume.html` | Interactive resume with animated skill bars, LinkedIn-style experience timeline, and certifications |
| `project-brightbox.html` | Project detail page for Bright Box — embedded demo video, presentation PDF, and design notebook |
| `project-robot.html` | Project detail page for Autonomous Sorting Robot — embedded design notebook and progress tracker |
 
---
 
## Features
 
### Live GitHub Analytics Dashboard
- Pulls real-time data from the **GitHub REST API** on every page load
- Displays commit activity chart (last 26 weeks), language donut chart, repo stats, and follower count
- Filterable, searchable, sortable repository grid with language filter buttons
- Skeleton loading states while data fetches
 
### Interactive Resume
- Skill bars animated on scroll using the **IntersectionObserver API**
- LinkedIn-style experience timeline with role progression
- Filterable by category (Work / Education / Clubs)
- Paginated project carousel with left/right navigation and dot indicators
 
### Project Detail Pages
- Tabbed interface for Demo Video, Presentation PDF, and Design Notebook
- Embedded `<video>` and `<iframe>` PDF viewers
- Project stats overview cards
- Phase-by-phase progress tracker
 
### General
- Fully responsive — mobile, tablet, and desktop
- Shared `style.css` design system across all pages
- Smooth scroll with JavaScript-powered active nav link highlighting
- Pink-themed design with Playfair Display + Lato typography
- Contact form powered by Formspree (no backend required)
- Deployed via GitHub Pages with Git CI/CD
 
---

## Tech Stack
 
| Category | Technologies |
|----------|-------------|
| **Languages** | HTML5, CSS3, JavaScript (ES6+) |
| **APIs** | GitHub REST API |
| **Charts** | Chart.js |
| **Fonts** | Google Fonts — Playfair Display, Lato |
| **Forms** | Formspree |
| **Deployment** | GitHub Pages |
| **Version Control** | Git, GitHub |
| **Editor** | VS Code, GitHub Codespaces |
 
---
 
## Project Structure
 
```
personalportfolio/
├── index.html                          # Homepage
├── analytics.html                      # GitHub analytics dashboard
├── resume.html                         # Interactive resume
├── project-brightbox.html              # Bright Box project page
├── project-robot.html                  # Sorting Robot project page
├── style.css                           # Shared design system
├── script.js                           # Smooth scroll + nav highlighting
├── images/
│   └── me.jpg                          # Profile photo
├── Team_1_13_Presentation.pdf          # Bright Box presentation
├── Team_1_13_ENED_DESIGN_NOTEBOOK.pdf  # Bright Box design notebook
├── ENED_Design_Notebook_Team_10_15.pdf # Robot design notebook
└── Team1_13_Final_Presentation_BrightBox_ENED.mp4  # Demo video
```

## Running Locally
 
No build step or dependencies required — this is plain HTML/CSS/JS.

## Key JavaScript Features
 
```javascript
// Live GitHub API fetch — analytics.html
const response = await fetch(`https://api.github.com/users/${USERNAME}/repos?per_page=100`);
 
// IntersectionObserver for animated skill bars — resume.html
const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.querySelectorAll('.skill-bar-fill').forEach(bar => {
        bar.style.width = bar.dataset.width + '%';
      });
    }
  });
}, { threshold: 0.2 });
 
// Paginated project carousel — index.html + resume.html
function renderHomeProjects() {
  const start = homePage * HOME_PER_PAGE;
  const visible = HOME_PROJECTS.slice(start, start + HOME_PER_PAGE);
  // renders cards dynamically from JS data array
}
```
 
---
 
## Live Demo
 
**[mahisheth06.github.io/personalportfolio](https://mahisheth06.github.io/personalportfolio/)**
 
---
 
## Author
 
**Mahi H. Sheth**
CS Freshman — University of Cincinnati, Class of 2030
Available for Co-op: Fall 2026
 
[![LinkedIn](https://img.shields.io/badge/LinkedIn-mahisheth06-0077b5?style=flat-square&logo=linkedin)](https://linkedin.com/in/mahisheth06/)
[![GitHub](https://img.shields.io/badge/GitHub-mahisheth06-222?style=flat-square&logo=github)](https://github.com/mahisheth06)

