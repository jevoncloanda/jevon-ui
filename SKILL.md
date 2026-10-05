---
name: jevon-ui
description: >-
  Apply Jevon's personal UI judgment and project fit to meaningful visual frontend work:
  pages/components, dashboards, forms, data tables, redesign, responsive layouts,
  design review, and screenshot/Figma/live-site implementation. Preserve product
  conventions and interpret references; coordinate with Impeccable when useful.
  Exclude backend, database, infrastructure, API-only, nonvisual frontend refactors,
  and tiny implementation changes without visual impact.
---

# Jevon UI

Own personal design judgment, product/domain fit, repository preservation, reference interpretation, and the decision to use Impeccable. Do not become a design textbook or impose one aesthetic across products.

## Design authority

Respect system and repository instructions. Within design guidance, resolve conflicts in this order:

1. Explicit user requirements.
2. Existing project design specification.
3. User-provided visual references, within their stated scope.
4. Existing repository/product conventions.
5. Project domain and user workflow.
6. Jevon UI preferences.
7. Impeccable generic recommendations.

Project-specific authority wins over either skill, including generic stylistic bans. Honor explicit aesthetics; if they create a material usability or accessibility problem, explain it and resolve that problem without silently substituting your taste. Ask only when a material conflict cannot be resolved from context.

## Establish context before substantial work

Inspect current screens, components, tokens, typography, spacing, borders/radii, responsive behavior, and interaction patterns before editing an established interface. Missing design documentation does not make it greenfield. Reuse the visual language unless redesign is explicitly requested; even then preserve product truth, behavior, and constraints outside the requested change.

Classify the requested **surface**, not the whole company:

- **Product:** prioritize task completion, information hierarchy, state clarity, efficient navigation, useful density, and predictable interactions.
- **Brand/marketing:** allow stronger identity, storytelling, art direction, expression, and visual impact. Portfolios and campaigns should not inherit dashboard restraint.

For substantial work, record a concise internal or user-visible preflight as appropriate:

```text
Surface: Product / Brand
Primary user:
Primary task:
Existing design:
Provided references and scope:
Required density:
Main hierarchy:
Patterns to preserve:
Patterns to avoid:
Impeccable use: shape / audit / critique / polish / general guidance / none
```

Infer settled facts from available evidence; ask about material gaps only. Skip preflight for trivial visual fixes. Read [Jevon principles](references/jevon-principles.md) for domain/density decisions and [project context](references/project-context.md) when durable project guidance would help.

## Use Impeccable selectively

Impeccable is an optional, separately installed broad design toolkit. Discover it by skill name/capability through the available skill catalog; never assume a machine path or vendor its documentation.

- **Tiny alignment fix or copy change:** use existing repository conventions; no full design workflow.
- **Substantial new UI:** establish product constraints here, then use Impeccable design reasoning or shaping if it helps resolve open decisions.
- **Working UI feels unfinished:** preserve structure and identity; use polish for finish, audit for technical quality, or critique for design judgment when warranted.
- **Screenshot/Figma/live-site work:** establish reference scope here; add Impeccable reasoning only where beneficial.

General guidance is not an implicit request to run every Impeccable command. If selecting a workflow, read the installed skill and relevant playbook and follow its applicable requirements, subject to higher-priority instructions and the design authority above. Do not treat its breadth as permission for unrelated redesigns, dependency changes, or mandatory project documents. Jevon UI remains responsible for checking the result against the actual product and repository.

If Impeccable is unavailable, continue using project context, these preferences, existing components, and normal frontend expertise. Report missing capability only when it materially limits the requested outcome.

## Interpret references

For screenshots, Figma, live sites, or multiple references, read [reference workflow](references/reference-workflow.md). Inspect supplied references and identify what each governs before implementation. Adapt their relevant characteristics to the current product rather than combining every feature or importing an unrelated identity.

## Verify and finish

For meaningful visual changes, run the app with available browser tooling, inspect relevant rendered screens and viewport(s), exercise changed interactions and relevant states, and compare with project conventions and scoped references. Fix visible issues and reinspect in a bounded confirmation pass. Use Impeccable/browser capabilities where useful; do not require a particular tool or install dependencies solely for this skill.

Preserve accessibility and complete relevant loading, empty, error, disabled, success, and selection behavior. For dense tables, keep critical comparison and actions available on smaller screens rather than mechanically converting every row into a card.

Run repository-required checks, but lint/typecheck/build success is not rendered-screen proof. State exactly which screens, states, or viewports remain unverified if execution is unavailable. Use the [review checklist](references/review-checklist.md) for product-fit acceptance, and [eval cases](evals/cases.md) when maintaining this skill.

Finish with material decisions, verification, and limitations. Stop when the requested scope works, fits its context, and has sufficient proof.
