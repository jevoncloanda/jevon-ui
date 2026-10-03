# Interface review checklist

Apply relevant items. Record concrete issues and their impact, not a score based on taste.

## Product fit
- Does the screen support the user's main task, decisions, and exceptions?
- Does it follow the requested direction, design specification, and scoped references?
- Are displayed metrics, copy, and controls meaningful rather than invented filler?

## Visual hierarchy
- Are the current context, important information, next action, and exceptional states obvious?
- Are primary and secondary actions distinguishable without overwhelming the workspace?

## Layout
- Do grouping, alignment, navigation, and content width fit the task?
- Do containers express real boundaries without unnecessary nesting?
- Is information density useful and readable for the audience?

## Typography
- Are existing type conventions preserved, with readable sizes and clear roles?
- Are numbers, units, code, and long labels easy to scan and compare?

## Spacing
- Is spacing consistent, with tighter related groups and clearer section separation?
- Do controls remain usable without oversized gaps consuming the screen?

## Components
- Are existing components and tokens reused appropriately?
- Are tables aligned, widths sensible, and row actions discoverable?
- Are form labels, grouping, control types, widths, and validation useful?
- Are dialogs suited to the task and navigation important enough to remain visible?

## Interaction
- Do changed actions work, with predictable focus, selection, and dismissal?
- Do disabled and destructive controls explain their state or consequence where needed?
- Are keyboard paths and existing interaction behavior preserved?

## States
- Are relevant loading, empty, error, success, and selection states clear?
- Can users recover from errors, and do empty states offer a useful next step?
- Does loading avoid disruptive layout shifts or misleading stale data?

## Responsive behavior
- Were desktop and small-laptop widths inspected, plus tablet/mobile where relevant?
- Are wrapping, overflow, clipping, navigation, dialogs, and form actions usable?
- Do table adaptations preserve necessary information and comparison?

## Accessibility
- Are semantics, labels, focus order, visible focus, and keyboard access correct?
- Are text/control contrast and target sizes appropriate, with meaning beyond color?
- Are status updates available to assistive technology where needed, and motion preferences respected?

## Generic AI pattern check
- Does each conspicuous card, pill, icon, gradient, shadow, chart, and large heading serve a purpose?
- Does the screen feel specific to this product rather than a reusable decorative dashboard?
- Consult [anti-patterns](anti-patterns.md) for questionable treatments and legitimate exceptions.

## Visual verification
- Was the relevant rendered screen inspected and the changed flow exercised?
- Were available non-happy-path states and relevant viewports checked after fixes?
- Were supplied references compared within their intended scope?
- Are repository-required checks complete and unavailable visual proof stated accurately?
