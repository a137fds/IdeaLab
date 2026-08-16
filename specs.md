# IdeaLab Specification

## Architecture

- IdeaLab is a static, multi-page website.
- The site must be compatible with GitHub Pages and deployable directly from the GitHub repository.
- The site must not require a server-side runtime, database, backend service, or other server infrastructure.
- HTML and CSS are the primary technologies. JavaScript may be used when necessary for client-side interactivity.
- React, Angular, Vue, and similar application frameworks are not required for the current architecture.

## Navigation

- The home page is a collection of navigation cards.
- Cards lead to sections or pages within IdeaLab.
- Example structure:
  - `/` — home page
  - `/phrases/` — phrases
  - `/projects/` — projects
  - `/projects/wattmeter/` — Wattmeter project
- A project is a page within IdeaLab, not an external website.

## Cards

- Cards are the primary visual and navigation element of the home page and section pages.
- The global IdeaLab styles control the appearance and behavior of these cards: layout, dimensions, spacing, borders, rounded corners, shadows, hover effects, and related UI details.
- The visual style should be light, pleasant, lively, and welcoming rather than dark or gloomy.

## Project Isolation

- Individual projects may have their own HTML, CSS, JavaScript, and other assets.
- Project styles must remain independent from the global IdeaLab styles.
- Global IdeaLab styles and project styles must not cause naming, selector, inheritance, or specificity conflicts.
- Project-specific classes, IDs, and selectors should be scoped or named so that they cannot accidentally alter the IdeaLab shell or other projects.
- The global IdeaLab stylesheet must not unexpectedly change the appearance of an individual project.
- Individual project styles must not unexpectedly change the appearance of IdeaLab navigation, cards, or other global UI.

## Content

- Phrases are maintained in `phrases.md`.
- Each phrase is stored as a separate line without translation or explanation.
- Projects are represented by navigation cards and individual project pages.

## Current Projects

- Wattmeter — the first project to be integrated into IdeaLab.
- The existing Wattmeter project should retain its own HTML and CSS rather than being forced into the global IdeaLab visual style.
