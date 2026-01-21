# ColorFont — Live Color & Typography Playground

ColorFont is an interactive playground for testing color systems and typography in real UI contexts. Instead of previewing colors or fonts in isolation, it applies them instantly across realistic interface layouts such as landing pages, dashboards, emails, mobile screens, blogs, and social cards.

The project focuses on understanding how color, contrast, and typography behave together in real designs, not just how they look in a palette.

---

## What Problem It Explores

Design decisions often fail when tested only in isolation.

Common issues include:

- colors that look fine alone but clash in layouts
- poor contrast that breaks accessibility
- typography that feels right but scales poorly
- gradients that don’t translate across components
- themes that break when switching light/dark modes

ColorFont solves this by letting users preview and test design systems directly inside realistic UI mockups.

---

## Feature Overview (User-Level)

Users can:

- pick primary, secondary, background, and text colors
- preview contrast quality (WCAG-aware)
- switch between light and dark themes
- generate accessible random color combinations
- preview color changes across multiple layouts
- select Google Fonts for titles and body text
- search and preview fonts live
- adjust gradients and angles in real time
- copy colors in HEX, RGB, or HSL formats
- share designs via URL state serialization

All changes update instantly across the entire UI.

---

## Core UI Surfaces

ColorFont applies design changes across:

- landing page sections
- dashboards
- registration flows
- success and loading screens
- email templates
- mobile app mockups
- blog layouts
- social media cards

This allows designers to evaluate consistency, hierarchy, and readability across different contexts.

---

## Color System Logic

ColorFont includes built-in logic for color safety and accessibility:

- dynamic contrast calculation using WCAG standards
- relaxed contrast thresholds for extreme luminance cases
- real-time contrast indicators (good / medium / poor)
- automatic random color generation with minimum contrast guarantees
- safe color parsing and fallback handling

Contrast is evaluated not just against backgrounds, but also between primary and secondary colors where relevant.

---

## Typography System

Typography features include:

- live Google Fonts fetching
- searchable font selection
- separate title and body fonts
- instant font application across layouts
- font preview on hover
- realistic scaling across headings, body text, and UI labels

This helps validate font pairings beyond simple sample text.

---

## State & Interaction Model

ColorFont maintains a single shared design state:

- colors
- fonts
- gradients
- theme mode

Key behaviors:

- all components react to state changes
- no page reloads
- undo-friendly design iteration
- deterministic updates
- URL serialization for shareable previews

Design state can be restored entirely from the URL.

---

## Frontend Architecture

Frontend stack:

- React
- Styled Components
- Chroma.js (color math)
- TinyColor (validation)
- React Colorful (pickers)
- Google Fonts API

Architecture principles:

- component-driven UI
- centralized design state
- pure visual logic (no backend dependency)
- predictable rendering
- strong separation between logic and presentation

---

## Component Design

The system is composed of reusable primitives:

- dynamic control bar
- color pickers with portal rendering
- contrast indicators
- font selectors with autocomplete
- gradient playground
- themed UI sections
- layout-specific mockups

Each component responds only to design state, making the system easy to extend.

---

## Accessibility Considerations

Accessibility is treated as a first-class concern:

- contrast ratios calculated in real time
- visual indicators for WCAG compliance
- readable defaults for light and dark modes
- validation for invalid color input
- safe fallbacks to prevent broken UI states

---

## What This Project Demonstrates

ColorFont demonstrates:

- real-time design system tooling
- color theory applied programmatically
- accessibility-aware UI logic
- typography scaling across layouts
- state-driven UI architecture
- complex interactive UI without backend reliance
- practical UX tooling beyond static mockups

---

## Scope & Status

ColorFont is:

- a functional design playground
- focused on visual systems, not branding theory
- built for experimentation and iteration
- frontend-only by design

It is not:

- a production design tool
- a Figma replacement
- optimized for large teams or workflows
- focused on persistence or authentication

