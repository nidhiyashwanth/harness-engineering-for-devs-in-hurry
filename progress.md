# Progress

## Current status

The reusable visual direction and workflow have been established. Lectures 04 through 07 are complete and connected.

## Completed

### Lecture 04 — Split Instructions Across Files

- Source: <https://walkinglabs.github.io/learn-harness-engineering/en/lectures/lecture-04-why-one-giant-instruction-file-fails/>
- Deliverable: `outputs/lecture-04-notes.html`
- Status: complete
- Verification: desktop and mobile layouts checked; no horizontal overflow or console errors; theme toggle works.

Content included:

- Giant-instruction-file failure loop.
- Five failure modes: context budget, lost in the middle, priority conflicts, maintenance decay, and contradiction accumulation.
- Core definitions: instruction bloat, signal-to-noise ratio, entry file, reveal on demand, and inability to distinguish priorities.
- Routing-oriented `AGENTS.md` architecture.
- Recommended entry-file and topic-document sizes.
- Source, applicability, and expiry metadata for instructions.
- Guidance to keep type definitions, interfaces, comments, and configuration explanations near the code.
- Before/after evidence from the lecture.
- Splitting procedure and refactor checklist.
- Closing takeaway: “The entry file is a router, not an encyclopedia.”

User handwritten notes were reviewed and incorporated where they improved recall. Most original points were already present; the explicit core-concept recall map and “keep truth near the code” guidance were added afterward.

### Lecture 05 — Keeping Context Alive Across Sessions

- Source: <https://walkinglabs.github.io/learn-harness-engineering/en/lectures/lecture-05-why-long-running-tasks-lose-continuity/>
- Deliverable: `outputs/lecture-05-notes.html`
- Status: complete
- Navigation: Lecture 04 and Lecture 05 link to each other; Lecture 05 reserves the next position for Lecture 06.
- Verification: desktop and mobile layouts checked; no horizontal overflow or console errors; theme toggle and bidirectional lecture navigation work.

Content included:

- Finite context, compaction/reset, lost reasoning, rebuild cost, and drift.
- Context anxiety and rushed-finish behavior.
- State persistence, rebuild cost, drift, and compaction versus reset.
- Handoff stack using `PROGRESS.md`, `DECISIONS.md`, git checkpoints, and initialization flow.
- Clock-in and clock-out routines.
- Mixed strategy, the 60% handoff threshold, and model-specific harness behavior.
- Rebuild-time, completion-rate, and hidden-defect evidence.
- Handoff checklist and memorable takeaway.

User notes were used to emphasize preservation of the “why,” verification state, cumulative drift, the 60% threshold, and model-specific reset behavior.

### Lecture 06 — Make the Agent Initialize Before Every Work Session

- Source: <https://walkinglabs.github.io/learn-harness-engineering/en/lectures/lecture-06-why-initialization-needs-its-own-phase/>
- Deliverable: `outputs/lecture-06-notes.html`
- Status: complete
- Navigation: Lecture 05 links to Lecture 06; Lecture 06 links forward to Lecture 07.
- Verification: desktop and mobile layouts checked; no horizontal overflow or console errors; dark mode and bidirectional lecture navigation work.

Content included:

- Mixed-session versus dedicated-initialization lifecycle.
- Failure modes: competing objectives, weak infrastructure, unverified accumulation, context waste, and implicit assumption landmines.
- Initialization concepts and success metrics.
- Five-part initialization contract: runnable environment, verified test framework, readiness document, ordered task breakdown, and clean checkpoint.
- Four readiness gates: can start, can test, can see progress, and can pick up next steps.
- Template advantage and initialization acceptance checklist.
- Source evidence: 31% higher completion, recovery within 3–4 sessions, ~60% extra rebuild time for the mixed approach, and under-three-minute session-two rebuild.

### Lecture 07 â€” Draw Clear Task Boundaries for Agents

- Source: <https://walkinglabs.github.io/learn-harness-engineering/en/lectures/lecture-07-why-agents-overreach-and-under-finish/>
- Deliverable: `outputs/lecture-07-notes.html`
- Status: complete
- Navigation: Lecture 06 links to Lecture 07; Lecture 07 links forward to Lecture 08.
- Verification: desktop and mobile layouts checked; no horizontal overflow or console errors; theme toggle and lecture navigation work.

Content included:

- Overreach and under-finish as the core failure loop.
- WIP=1 workflow: pick one task, execute it, verify end-to-end, then checkpoint.
- Reasoning-budget diagram from the lecture: `C/k` attention split versus full budget on one active task.
- Core definitions: overreach, under-finish, WIP limit, completion evidence, scope surface, and completion pressure.
- Practical boundary rules for `AGENTS.md` or `CLAUDE.md`.
- Externalized scope surface and verified completion rate tracking.
- Real-world evidence: 20% unconstrained E2E pass rate versus 100% WIP=1 session-one pass rate and 87.5% completion by session 4.
- Closing takeaway: do less, but finish.

### Lecture 08 - Use Feature Lists to Constrain What the Agent Does

- Source: <https://walkinglabs.github.io/learn-harness-engineering/en/lectures/lecture-08-why-feature-lists-are-harness-primitives/>
- Deliverable: `outputs/lecture-08-notes.html`
- Status: complete
- Navigation: Lecture 07 now links forward to Lecture 08; Lecture 08 links back to Lecture 07 and reserves the next position for Lecture 09.
- Verification: desktop and mobile layouts checked; no horizontal overflow; no console errors after favicon suppression; theme toggle and lecture navigation work.

Content included:

- Feature lists as harness primitives rather than human memos.
- The "done" mismatch between agent interpretation and end-to-end behavior.
- The required feature-row triple: behavior, verification command, and current state.
- Feature state machine: `not_started`, `active`, `blocked`, and `passing`.
- Pass-state gating: the harness controls transition to `passing` after verification succeeds.
- Single source of truth and back-pressure concepts.
- Four harness consumers: scheduler, verifier, handoff reporter, and progress tracker.
- Minimal structured JSON example and agent-instruction rules.
- Granularity calibration around one-session-completable features.
- Real-world comparison: 20-minute memo-mode inference, 3-minute structured resume, 45% higher completion rate, and zero duplicate implementations.

## Next work

- Continue with the next lecture selected by the user.
- Read the entire lecture and identify its distinct visual metaphor before implementation.
- Reuse the established design tokens and component language while varying section composition to fit the new material.
- Create the next deliverable in `outputs/` and update this file.
