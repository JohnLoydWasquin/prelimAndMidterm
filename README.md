# Fieldnotes — IT 414 SQA reviewer

A static, browser-based study platform for the IT 414 System Quality Assurance prelim and midterm materials. It uses semantic HTML, CSS, vanilla JavaScript modules, and local browser storage. No framework, backend, or database is required.

## Run locally

Serve this directory with any static server. For example:

```powershell
python -m http.server 8000
```

Then open `http://localhost:8000`. Opening `index.html` directly may block JavaScript modules in some browsers.

## Content inventory

The six supplied PDFs (94 pages total) were accessible and their text was extracted page by page. The site contains 38 course-topic notes in the instructor's lesson order:

- **Lesson I — Testing Fundamentals:** software testing and benefits; career skills; the seven principles in order; SDLC and STLC; six STLC phases in order; V-Model pairings; verification and validation.
- **Lesson II — Types of Testing:** execution method; black/white/gray-box technique; testing levels; functional and non-functional purpose; smoke, sanity, retesting, regression, API and interface testing; security, usability, reliability and compatibility; load, stress, spike, endurance/soak, volume, scalability; Big Bang, Top-Down, Bottom-Up, and Sandwich integration; maintenance, localization, globalization, and interoperability.
- **Lesson III — Test Case Development:** test documentation; policy, strategy, and plan; scenarios and cases; test data; test analysis; expected versus actual results and statuses; defect and summary reports; RTM.
- **Lesson IV — Testing Techniques:** BVA, equivalence classes, decision tables, state transitions, use cases, and error guessing.

Each topic includes a definition, Taglish explanation (toggleable), applied example, exam keywords, common confusion, generated situational practice with explanation, and recall note. Topic completion, bookmarks, lesson navigation, copy notes, diagrams, and search are included.

## Exam guide represented

The practice exams follow the supplied guide's item counts and point totals:

- **Prelim:** 20 multiple choice (40 points), 15 situational identification (30 points), and one testing-plan scenario (30 points) = 100.
- **Midterm:** 10 situational identification (20 points), five techniques-analysis tasks (40 points), and two practical test-case tasks (40 points) = 100.

Practice questions and scenario prompts are generated study exercises, not official questions. Multiple-choice items score automatically. Written sections include a self-check guide and ask the learner to self-assess points. The guide gives no exam duration; the mock practice timer is an optional, adjustable study timer and is not represented as an official duration.

## Features

- Dashboard with real local activity metrics, roadmap, continue-learning action, and personal goals.
- Interactive STLC and V-Model/level diagrams.
- Flashcards with known/review tracking.
- Mixed or topic-filtered quiz with answer feedback and persisted attempt statistics.
- Prelim and midterm mock exams, optional adjustable countdown, self-assessed written responses, and session recovery on refresh.
- BVA calculator, ECP partition builder, Boolean decision-table builder, login state simulator, and enrollment use-case simulator.
- Test-case builder with edit/delete and CSV export.
- Cram mode, global search, dark/light themes, keyboard focus styling, mobile drawer, JSON backup import/export, and reset.

## Data and privacy

Progress, preferences, goals, bookmarks, and test-case drafts are stored in `localStorage` on the current browser/device. A mock exam's in-progress responses use `sessionStorage` in the current tab. Use Settings to export/import a JSON backup; browser data is not synced to another device.

## Project layout

- `index.html` — semantic application shell
- `css/styles.css` — design system, components, themes, responsive rules, and motion preferences
- `js/data.js` — instructor-aligned content, quiz bank, flashcards, and exam configuration
- `js/app.js` — router, UI rendering, interactions, storage, and practice tools

## Source files reviewed

- `SQA-Prelims.pdf` (13 pages)
- `Prelims-and-Midterms-READ-THIS-TvT.pdf` (3 pages)
- `Lesson I Testing Fundamentals.pdf` (18 pages)
- `LESSON II Types of Testing.pdf` (15 pages)
- `LESSON III Test Case Development.pdf` (24 pages)
- `LESSON IV Testing Techniques.pdf` (21 pages)

Content is paraphrased and examples/questions are identified as generated study material. The source overview includes overlapping or broad categories (for example, regression appears in both functional and maintenance groupings); the site preserves these as context-dependent categories rather than silently forcing one universal classification. The overview extraction also runs “Smoke” and “UAT” together in a compact table; lesson text treats Smoke Testing and User Acceptance Testing as separate concepts, so the site presents them separately.

## Verification notes

JavaScript syntax and content/exam point totals were checked locally. The integrated browser automation host was unavailable during this build, so live visual browser checks at the requested viewport widths could not be completed in this environment. The supplied PDFs were text-extracted on every page; image-only artwork was not separately rendered for visual inspection. These are the remaining QA limits before describing this as production-ready.
