---
name: jevon-ui
description: Apply Jevon's frontend design judgment when creating or materially changing user-facing interfaces, including pages/components, UI redesign, visual polish, responsive layouts, product interface review, and design-reference implementation. Favor domain fit, clear hierarchy, useful density, existing product conventions, and intentional styling over generic AI/SaaS aesthetics. Do not use for backend, database, CLI, infrastructure, API-only work, or frontend changes with no visual impact.
---

# Jevon UI

Create interfaces that feel like usable products in their own domain. This skill supplies design judgment, not a universal palette, layout, density, radius, or imitation of another product.

## Establish the direction

Respect higher-priority system and repository instructions. Within design guidance, use this order: explicit user request, project design specification (such as `docs/DESIGN.md`), provided visual references, existing product conventions, then this skill's defaults. Resolve material conflicts instead of blending incompatible directions.

Before editing an existing UI, inspect the relevant screen and its components, CSS, tokens, typography, spacing, borders, colors, interaction states, and responsive rules. Reuse its visual language unless redesign is requested. Avoid unrelated changes and new component libraries when existing tools suffice.

Identify the user's main task, important information, decisions, and exceptions. Let these determine hierarchy, navigation, grouping, and density. For a new interface without established conventions, choose a small coherent set of typography, spacing, radius, borders, shadows, colors, and content-width decisions appropriate to the domain; do not invent a global Jevon brand.

If a generated brief defaults to four KPI cards, purple gradients, rounded containers, pills, and generous whitespace, examine what those choices serve. Replace unsupported decoration with a task-focused workspace. If the user explicitly requires those treatments, respect that direction and make them coherent and usable; explain material tradeoffs without silently overriding the request.

## Use references deliberately

Inspect all supplied references before implementation. Establish what each governs: navigation, table treatment, typography, hierarchy, density, or interaction. Extract those characteristics and adapt them to the product rather than combining every visual feature. Preserve explicit reference scopes. Avoid unnecessary reproduction of third-party branding or proprietary assets; use supplied or authorized assets appropriately. Compare the rendered result with the intended direction afterward.

## Choose useful structure

- **Operations/admin:** Consider compact navigation, a utility bar, contextual actions, filters, tables or queues, details, and visible exceptions. Use practical density without sacrificing readability.
- **Developer tools:** Favor precise navigation, logs/traces/code/data views, and visible status or errors. Use monospace for semantically useful content, not every label.
- **Finance:** Prioritize trustworthy data presentation, units, numeric alignment, and clear consequences of actions.
- **Consumer:** Allow imagery, more whitespace, expressive typography, and simpler navigation when they support the experience.
- **Marketing:** Allow distinctive composition and expressive type. Build around real value and content rather than a stock hero/features/testimonials formula.

These are starting points, not mandatory shells. Use meaningful grouping, typography, alignment, and separators before adding cards. Reserve pills, icons, gradients, shadows, charts, and large headings for a clear purpose. Use concise domain-specific copy and real functionality; do not invent metrics, tabs, filters, or widgets for visual fullness.

## Implement complete interactions

Use existing framework patterns, components, tokens, utilities, and accessibility behavior. Keep primary and secondary actions distinguishable. Preserve keyboard usability, visible focus, semantic structure, contrast, and status meaning beyond color.

Tables need scan-friendly columns, aligned numbers, sensible widths and actions, and clear hover/selection states. Forms need labels, logical grouping, appropriate controls and widths, predictable tab order, and explicit validation. Use dialogs to maintain context for bounded tasks; use a page or suitable panel for spacious workflows. Keep important navigation discoverable. Represent status with text and restrained supporting color or icons.

Implement relevant loading, empty, error, disabled, success, and selection states with useful feedback and recovery. Do not treat a populated happy-path mockup as a finished interface.

## Verify the rendered result

For meaningful visual changes, use available browser tooling to run the application, open the relevant screen, inspect the actual rendering, exercise the changed interaction and relevant states, fix issues, and reinspect. Use available Playwright or screenshot capabilities when appropriate; do not require a particular tool or install dependencies solely for this skill.

Check desktop and small-laptop widths; include tablet and mobile where relevant to the product. Examine spacing, alignment, hierarchy, overflow, clipping, text wrapping, tables, forms, dialogs, and responsive behavior. For complex tables, choose deliberate scrolling, reduced columns, or responsive details when these work better than row-to-card conversion. Retain access to critical information and actions.

Capture screenshots when they aid comparison or proof. Run repository-required checks, but do not equate lint, typecheck, or build success with visual verification. If browser execution or particular states are unavailable, report exactly what remains unverified. Do not force browser testing for a nonvisual change.

## Supporting material

Read only what the task needs:

- [Design principles](references/design-principles.md): when choosing or explaining hierarchy, density, grouping, and visual treatment.
- [Anti-patterns](references/anti-patterns.md): when auditing generic generated styling or deciding whether a familiar pattern is justified.
- [Review checklist](references/review-checklist.md): when reviewing an interface or checking a completed visual change. Apply relevant items only.
- [Conceptual examples](examples/patterns.md): when comparing alternative approaches without prescribing exact CSS.

Finish with a brief account of material design decisions, verification performed, and remaining limitations. Stop when the requested interface works, fits its context, and has sufficient visual proof.
