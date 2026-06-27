# Rules for Course Notes

## Objective

Create concise, visually polished HTML study notes for each lecture in the Learn Harness Engineering course. The notes must support fast recall without replacing the source lecture.

## Content workflow

1. Open the lecture URL and read every section before drafting.
2. Extract the central argument, failure modes, core concepts, architecture or workflow, evidence, practical steps, exercises, and final takeaway.
3. Compare the lecture with any handwritten notes supplied by the user. Add useful recall cues that are missing from the HTML, but do not duplicate existing material.
4. Preserve exact figures and technical claims from the lecture. Do not invent metrics or examples.
5. Link back to the source lecture in the HTML.
6. Keep the writing concise. Prefer short definitions, diagrams, sequences, checklists, and contrasts over long paragraphs.
7. Inspect the source for diagrams, Mermaid blocks, images, SVGs, and linked assets. Render or read visual assets when possible, then summarize their meaning in the HTML with code-native diagrams or concise visual sections.

## Visual system

- Continue the established “Harness Notes” editorial field-guide style.
- Use a warm paper background, deep ink text, muted vermilion accent, and dark blue-green diagrams.
- Use professional serif headings, neutral sans-serif body text, and monospace for filenames and technical labels.
- Favor open layouts, thin rules, restrained diagrams, and varied section rhythm.
- Avoid generic card grids, decorative filler, excessive icons, gradients, glass effects, and fake metrics.
- Keep navigation quiet and sticky. Include a persistent light/dark theme toggle.
- Make all text and controls code-native.
- Maintain accessible semantic HTML, clear heading order, keyboard-friendly links and controls, reduced-motion support, and readable contrast.

## Structure for future lecture pages

Adapt the structure to the lecture rather than forcing every section, but normally include:

1. Hero with lecture title, one-sentence thesis, source link, and a visual summary.
2. Problem or failure sequence.
3. Core-concept recall map.
4. Better architecture, workflow, or mental model.
5. Evidence or concrete example when the lecture provides it.
6. Practical implementation steps.
7. Refactor or review checklist.
8. One memorable closing takeaway.

## File and verification rules

- Store user-facing HTML deliverables in `outputs/`.
- Use filenames such as `lecture-05-notes.html`.
- Keep temporary screenshots and research artifacts in `work/`; remove temporary QA files after verification.
- Treat `outputs/lecture-04-notes.html` as the visual reference for subsequent chapters.
- Verify every page in a browser at desktop and mobile widths.
- Check for horizontal overflow, clipped text, console errors, broken navigation, and theme-toggle behavior.
- Visually inspect the final render before handoff.
- Update `progress.md` after each lecture and record durable design or scope choices in `decisions.md`.
