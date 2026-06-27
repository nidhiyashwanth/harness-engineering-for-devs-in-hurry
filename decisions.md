# Decisions

## D-001 — One standalone HTML file per lecture

Each lecture will be delivered as a self-contained HTML file with inline CSS and minimal JavaScript. This keeps the notes portable and easy to open without a build step.

## D-002 — Editorial field-guide design

The series uses an editorial technical-notes aesthetic instead of a dashboard or generic card layout. The established palette, typography hierarchy, rules, diagrams, and spacing from Lecture 04 are the baseline for later chapters.

## D-003 — Consistent system, lecture-specific composition

Later pages should feel like one series, but they should not be clones. Reuse tokens, navigation behavior, typography, and interaction patterns while choosing diagrams and section rhythm that reflect each lecture’s argument.

## D-004 — Concision over transcript-style coverage

The HTML should capture what is necessary for recall: thesis, concepts, relationships, evidence, procedures, and takeaways. It should not reproduce the lecture paragraph by paragraph.

## D-005 — Source lecture is authoritative

Handwritten notes are used as recall aids and gap detectors. When wording or figures differ, verify against the source lecture and preserve the source’s meaning and numbers.

## D-006 — Code-native content

Headings, diagrams, labels, metrics, navigation, and controls remain HTML/CSS rather than being embedded in raster images. This preserves accessibility, responsiveness, and editability.

## D-007 — Built-in theme support

Each page includes a light/dark theme toggle, persists the selected theme in local storage, and respects reduced-motion preferences.

## D-008 — Canonical location

The canonical user-facing files live in `outputs/`. Temporary concepts, screenshots, and QA artifacts belong in `work/` and should not be treated as deliverables.

## D-009 — Verification threshold

A lecture page is complete only after desktop and mobile checks confirm readable typography, no horizontal overflow, working navigation and theme controls, and no relevant console errors.

## D-010 — Bidirectional series navigation

Every completed lecture links to the previous and next available local lecture. The newest lecture may show the next chapter as “Coming next” until its file exists; when a chapter is added, update both neighboring pages so navigation remains bidirectional.
## D-011 - Visual source capture

Lecture extraction must include diagrams and images, not just prose. For Mermaid, SVG, image, or other visual assets, inspect the source asset or rendered page and convert the important relationship into code-native HTML/CSS notes so the final page captures the full lecture argument.
