# ViYukti Project Progress

## [2026-06-05] Phase 1: Infrastructure & Data Modeling
- **Git Initialized**: Repository created and initial commit pushed.
- **Content Decoupling**: Created `src/data/siteData.json` containing all brand and service data for 6 sectors.
- **Architecture Defined**: Confirmed "Section Dispatcher" pattern for dynamic industry page rendering.
- **Tracking**: `PROGRESS.md` created for user-facing change logs.

## [2026-06-05] Phase 2: Core Framework & Dynamic Dispatcher
- **Astro Setup**: Initialized `package.json`, `astro.config.mjs`, and `tailwind.config.cjs`.
- **Global Layout**: Built `BaseLayout.astro` with GSAP integration and premium dark theme (Zinc-950).
- **Service Dispatcher**: Implemented `src/pages/services/[slug].astro` which dynamically renders content for all 6 industries from a single template.
- **Master Hub**: Created `index.astro` with a high-contrast industry selection grid.
- **Git Milestone**: Committed core framework changes.

## [2026-06-05] Phase 3: Interactive Industry Widgets
- **Global GSAP Enhancements**: Upgraded `BaseLayout.astro` with "Slide Up + Blur" hero reveals and "Fade-in + Scale" scroll reveals for all elements.
- **Solar Widget**: Built `SolarCalculator.astro` with GSAP-powered rolling number animations.
- **Recruitment Widget**: Built `JobBoard.astro` with client-side GSAP staggered filtering.
- **Digital Marketing Widget**: Built `MetricStats.astro` with GSAP ScrollTriggered counters.
- **IT Development Widget**: Built `EnterpriseBreakdown.astro` with custom GSAP accordions.
- **Real Estate Widget**: Built `LuxuryPortfolio.astro` with masonry-style grid and GSAP image hover reveals.
- **Corporate Gifting Widget**: Built `GiftingCatalog.astro` with premium product grid, GSAP hover overlays, and interactive quote triggers.
- **Device Compatibility**: Verified responsive grids and interaction touchpoints across all 6 sectors.
- **Git Milestone**: Final industry sector committed. Project architecture complete.

## [2026-06-05] Phase 4: Refinement & Global Data Binding
- **Homepage Redesign**: Upgraded `index.astro` from a simple grid to a premium landing page with a grand hero section, "Synergy" about section, and luxury service cards.
- **Global Data Binding**: Refactored the architecture so that the Company Name, Tagline, Footer Copyright, and Footer Credits are all strictly pulled from `siteData.json`.
- **Dynamic Navigation**: Updated the desktop and mobile dropdowns in `Navigation.astro` to auto-generate from the JSON data, ensuring perfect consistency if service names change.
- **Navigation Fluidity**: Implemented CSS smooth scrolling for anchor links (e.g., "Explore Sectors") and integrated Astro's `<ViewTransitions />` component. 
- **Bug Fixes**: Wrapped all individual widget GSAP scripts in `astro:page-load` listeners, resolved broken image URL in the Gifting catalog.
- **Smart Routing (Lead Gen)**: Upgraded the "Consult Our Experts" buttons to pass URL parameters (e.g., `?industry=solar`) and automatically pre-fill the form's "Industry of Interest" dropdown.
- **UI Cleanup**: Removed redundant "Explore Solutions" buttons from the dispatcher. Simplified the Corporate Gifting widget.

## [2026-06-05] Phase 5: Light/Dark Theme System
- **Tailwind Configuration**: Enabled explicit `darkMode: 'class'` in Tailwind config.
- **Global CSS Overrides**: Injected a clever CSS ruleset into `BaseLayout.astro` that automatically overrides the hardcoded dark utility classes (e.g., flipping `text-white` to `text-zinc-900` and `bg-white/5` to `bg-black/5`) when the light theme is active. This instantly enables a pristine light theme without requiring an exhaustive codebase rewrite.
- **Theme Toggle**: Added a fully functional Sun/Moon toggle button to the main navigation. It instantly switches the CSS context and saves the user's preference to `localStorage`, persisting perfectly across the SPA View Transitions.
- **Bug Fixes (Theme Integration)**: Resolved a bug where the theme reset during View Transitions by hooking the theme initialization logic into `astro:after-swap`. Fixed GSAP hover interactions and expanded global CSS overrides to ensure cards and buttons look perfect in both dark and light modes.
- **Git Milestone**: Fully committed Light/Dark mode functionality and SPA persistence fixes.
