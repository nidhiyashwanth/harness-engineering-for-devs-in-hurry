# Progress

## Current status

The reusable visual direction and workflow have been established. Lectures 01 through 12 are complete and connected.

## Completed

### Lecture 01 - Strong Models Don't Mean Reliable Execution

- Source: <https://walkinglabs.github.io/learn-harness-engineering/en/lectures/lecture-01-why-capable-agents-still-fail/>
- Deliverable: `outputs/lecture-01-notes.html`
- Status: complete.
- Navigation: Lecture 01 links forward to Lecture 02; Lecture 02 links back to Lecture 01.
- Verification: desktop and mobile layouts checked through the in-app browser via local static server; no horizontal overflow; no console warnings/errors; theme toggle and lecture navigation work.

Content included:

- Model capability versus execution reliability as the central distinction.
- Anthropic same-model comparison: bare run at 20 minutes / $9 with broken core features versus full harness at 6 hours / $200 with playable result.
- Five failure layers: task specification, context provision, execution environment, verification feedback, and state management.
- Core terms: capability gap, harness, harness-induced failure, verification gap, diagnostic loop, and Definition of Done.
- Practical diagnostic loop: execute, observe failure, attribute layer, fix harness layer, rerun.
- Explicit Definition of Done example for a search endpoint.
- OpenAI million-line experiment: three engineers, five months, about one million lines, 1,500 PRs, 3.5 PRs per person per day.
- FastAPI team example: 40% context spent exploring before harness; same model succeeded in three independent runs after `AGENTS.md`, verification commands, and ADRs, with ~60% better context efficiency.

### Lecture 02 - What a Harness Actually Is

- Source: <https://walkinglabs.github.io/learn-harness-engineering/en/lectures/lecture-02-what-a-harness-actually-is/>
- Deliverable: `outputs/lecture-02-notes.html`
- Status: complete.
- Navigation: Lecture 01 links forward to Lecture 02; Lecture 02 links back to Lecture 01 and forward to Lecture 03.
- Verification: desktop and mobile layouts checked through the in-app browser via local static server; no horizontal overflow; no console warnings/errors; theme toggle and lecture navigation work.

Content included:

- Precise definition of harness as engineering infrastructure outside model weights, not merely a prompt file.
- Five-subsystem harness model: instructions, tools, environment, state, and feedback.
- Source Mermaid flow converted into a code-native subsystem diagram.
- Core concepts: repo as source of truth, map not manual, constrain instead of micromanage, and controlled subsystem exclusion.
- Practical verification command block and guidance to attribute failures before declaring bottlenecks.
- Real story from a TypeScript + React team: README-only 20% success, AGENTS.md 60%, verification 80%, progress templates 80-100%.
- Takeaway that feedback is often the lowest-investment, highest-return subsystem to improve first.

### Lecture 03 - Making the Repository the Single Source of Truth

- Source: <https://walkinglabs.github.io/learn-harness-engineering/en/lectures/lecture-03-why-the-repository-must-become-the-system-of-record/>
- Deliverable: `outputs/lecture-03-notes.html`
- Status: complete.
- Navigation: Lecture 02 links forward to Lecture 03; Lecture 03 links back to Lecture 02 and forward to Lecture 04.
- Verification: desktop and mobile layouts checked through the in-app browser via local static server; no horizontal overflow; no console warnings/errors; theme toggle and lecture navigation work.

Content included:

- Repository as the agent's system of record and highest-authority specification.
- Knowledge visibility gap: Slack, Confluence, Jira, and engineers' heads are invisible unless written into repo files.
- Source Mermaid relationships converted into code-native knowledge-map and fresh-session-test sections.
- Fresh session test questions: system purpose, organization, run path, verification path, and current progress.
- Core concepts: knowledge visibility gap, system of record, discovery cost, knowledge decay rate, and fresh session test.
- Practical repo map using `AGENTS.md`, module-local `ARCHITECTURE.md`, `CONSTRAINTS.md`, `PROGRESS.md`, and `Makefile`.
- ACID analogy for agent state: atomicity, consistency, isolation, and durability.
- E-commerce transformation story: 30 microservices, 70% human-intervention baseline, and repo-local documentation fixes.

### Lecture 04 — Split Instructions Across Files

- Source: <https://walkinglabs.github.io/learn-harness-engineering/en/lectures/lecture-04-why-one-giant-instruction-file-fails/>
- Deliverable: `outputs/lecture-04-notes.html`
- Status: complete
- Navigation: Lecture 03 links forward to Lecture 04; Lecture 04 links back to Lecture 03 and forward to Lecture 05.
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
- Navigation: Lecture 07 links forward to Lecture 08; Lecture 08 links back to Lecture 07 and forward to Lecture 09.
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

### Lecture 09 - Preventing Agents from Declaring Victory Too Early

- Source: <https://walkinglabs.github.io/learn-harness-engineering/en/lectures/lecture-09-why-agents-declare-victory-too-early/>
- Deliverable: `outputs/lecture-09-notes.html`
- Status: complete.
- Navigation: Lecture 08 links forward to Lecture 09; Lecture 09 links back to Lecture 08 and forward to Lecture 10.
- Verification: desktop and mobile layouts checked through the in-app browser via local static server; no horizontal overflow; no console warnings/errors; theme toggle and lecture navigation work.

Content included:

- Premature completion declaration as confidence replacing execution evidence.
- Password-reset failure case: missing email config, partial migration failure, and untested end-to-end reset flow.
- Three-layer termination check: static analysis, runtime behavior verification, and system-level confirmation.
- Unit-test limitation traps: interface mismatch, state propagation errors, and environment dependency.
- Core concepts: calibration bias, termination criteria, verification-validation dual gate, runtime feedback signals, and completion priority constraint.
- Worker-checker separation from Anthropic's harness comparison: single-agent bare run versus planner/generator/evaluator.
- Actionable error feedback pattern and runtime-signal capture checklist.
- Real-world cost tradeoff and 5-10x post-hoc repair savings claim from the lecture.

### Lecture 10 - Only a Full Pipeline Run Counts as Real Verification

- Source: <https://walkinglabs.github.io/learn-harness-engineering/en/lectures/lecture-10-why-end-to-end-testing-changes-results/>
- Deliverable: `outputs/lecture-10-notes.html`
- Status: complete.
- Navigation: Lecture 09 links forward to Lecture 10; Lecture 10 links back to Lecture 09 and forward to Lecture 11.
- Verification: desktop and mobile layouts checked through the in-app browser via local static server; no horizontal overflow; no console warnings/errors; theme toggle and lecture navigation work.

Content included:

- Full-pipeline verification as the only proof of system-level behavior.
- Electron file-export example across renderer, preload bridge, service layer, filesystem, and exported file.
- Unit-test blind spots: interface mismatch, state propagation, resource lifecycle, and environment dependency.
- E2E-driven behavior shifts: component interactions, architectural boundaries, and error paths.
- Core concepts: component boundary defects, testing adequacy gradient, executable architecture, review feedback promotion, and agent-oriented error messages.
- Layered Domain Architecture summary: Types -> Config -> Repo -> Service -> Runtime -> UI, with provider interfaces for cross-domain concerns.
- Review feedback promotion flow from recurring comment to automated harness check.
- Real-world defect table: five defects missed by unit tests and caught by E2E; runtime tradeoff from 2 seconds to 15 seconds.

### Lecture 11 - Making the Agent's Runtime Observable

- Source: <https://walkinglabs.github.io/learn-harness-engineering/en/lectures/lecture-11-why-observability-belongs-inside-the-harness/>
- Deliverable: `outputs/lecture-11-notes.html`
- Status: complete.
- Navigation: Lecture 10 links forward to Lecture 11; Lecture 11 links back to Lecture 10 and forward to Lecture 12.
- Verification: desktop and mobile layouts checked through the in-app browser via local static server; no horizontal overflow; no console warnings/errors; theme toggle and lecture navigation work.

Content included:

- Observability as a harness architecture property, not agent self-logging.
- Four missing-observability costs: "looks correct" ambiguity, mystical evaluation, blind retries, and session handoff cliffs.
- Dark-mode scenario comparison: vague 45-minute loop versus observable 15-minute loop.
- Layered observability diagram: runtime signals plus process artifacts feeding review and specific verdicts.
- Core concepts: task trace, sprint contract, evaluator rubric, runtime signals, and layered observability.
- Why agents cannot solve observability by printing logs: unknown unknowns, inconsistent formats, and missing process artifacts.
- Implementation steps: automatic signal collection, sprint contracts, evaluator rubrics, and OpenTelemetry traces/spans.
- Anthropic three-agent DAW experiment with phase durations, costs, total 3 hr 50 min / $124.70, and planner/generator/evaluator roles.

### Lecture 12 - Leave a Clean Handoff at the End of Every Session

- Source: <https://walkinglabs.github.io/learn-harness-engineering/en/lectures/lecture-12-why-every-session-must-leave-a-clean-state/>
- Deliverable: `outputs/lecture-12-notes.html`
- Status: complete.
- Navigation: Lecture 11 links forward to Lecture 12; Lecture 12 links back to Lecture 11 and has no next-lecture target.
- Verification: desktop and mobile layouts checked through the in-app browser via local static server; no horizontal overflow; no console warnings/errors; theme toggle and lecture navigation work.

Content included:

- Clean state as a required session-exit condition rather than optional housekeeping.
- Entropy growth and agent pattern-copying as the default failure mode without cleanup.
- Clean-state exit flow: build, tests, progress, artifacts, and startup path.
- Dirty-loop versus clean-loop comparison for session handoff quality.
- Core concepts: clean state, session integrity, quality document, cleanup loop, harness simplification, and idempotent cleanup.
- Dual-mode cleanup strategy: immediate per-session cleanup and periodic weekly cleanup.
- Quality-document examples for high- and low-quality modules.
- Harness simplification guidance as model capabilities improve.
- Twelve-week comparison: 68%/61%/60+ min/103 stale artifacts without cleanup versus 97%/95%/9 min/11 stale artifacts with cleanup.

## Maintenance

- Course notes are complete for Lectures 01 through 12.
- Keep generated HTML in `outputs/`; GitHub Pages publishes that directory.
- For future edits, verify affected lecture navigation, no horizontal overflow, no console warnings/errors, and theme toggle behavior before committing.
