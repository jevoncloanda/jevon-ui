# Behavioral evaluation cases

Use for conceptual review or forward-testing when maintaining the skill. Evaluate decisions and observable outcomes, not exact wording. A metadata validator cannot prove automatic discovery or good design judgment.

## Product and preference cases

1. **Operations dashboard:** "Build a shipment management dashboard."
   Expect activation, a product preflight, useful density, queue/table-first reasoning, meaningful statuses, restrained decoration, and optional Impeccable shaping/general guidance. Fail if decorative KPI cards displace the primary work or invented widgets fill space.
2. **Existing enterprise interface:** "Add an exception filter to this established shipment screen."
   Expect inspection and reuse of existing components/tokens and preservation of identity, navigation, and behavior. Fail if a missing DESIGN.md triggers a new visual language or unrelated rewrite.
3. **Consumer application:** "Create a touch-first music discovery screen."
   Expect room for expression, imagery, and browsing. Fail if enterprise density is treated as universal.
4. **Marketing/portfolio:** "Build my portfolio homepage with strong art direction."
   Expect brand/marketing classification and expressive storytelling. Fail if it becomes an admin dashboard.
5. **Scoped screenshot references:** "Redesign this shipment table: A for navigation, B for table density, C for typography."
   Expect strong activation, inspection and a reference mapping, faithful scoped adaptation, and rendered comparison. Fail if references are blindly merged or branding/copy copied without purpose. Mark inaccessible references and unproven interactions.
6. **Generic AI dashboard:** "Make an operations dashboard with a premium feel."
   Expect product-specific task reasoning and scrutiny of automatic card/pill soup, large headings, ornamental charts, and excessive whitespace. Fail if a stock shell is assumed or these patterns become absolute bans.
7. **Explicit aesthetic:** "Use expressive gradients and rounded cards for this music app."
   Expect user intent to win, with coherent treatment and accessibility. Fail if either skill rejects gradients by default.
8. **Mixed-purpose enterprise home:** "Improve an ERP home page where Quick Navigation instructions and interactive Favorites occupy equal-width, equal-height cards."
   Expect content-role reasoning, a prominent usable Favorites section, accessible compact navigation actions, proportional guidance, and preservation of product identity. On mobile, keep hints compact and functional content prominent. Fail if the result merely stacks oversized cards, adds fake metrics/activity, or wraps every item in another surface.
9. **Justified equal treatment:** "Arrange comparable interactive project summaries in a balanced two-column card grid using the existing product design."
   Expect equal treatment when content and purpose warrant it, with responsive usability and intentional whitespace. Fail if the skill forces asymmetry or bans equal-width/nested cards without a concrete hierarchy or usability problem.
10. **Expandable supporting aggregate table:** "Let users compare this monthly chart with its exact aggregate values; the small dataset is already available and the table belongs beneath the chart."
    Expect a recommended supporting table collapsed by default within the chart component, with chart and table visible together when expanded, a contextual integrated disclosure row, synchronized filters/values, and no redundant request. Check semantic keyboard operation, visible focus and expanded state, logical order without unnecessary focus movement, table headers, and no whole-page horizontal overflow. Fail if a toggle or overlay replaces it merely for appearance, a generic blue link is repeated, or record-level detail is assumed.
11. **Contextual investigation:** "Let users inspect a selected category's records and continue into a large filtered investigation using existing record navigation."
    Expect a context-specific accessible entry point, a bounded drawer only if useful, and sufficient workspace for extensive investigation. Check focus, back/close, filters and selection on return, relevant data states, and smaller-screen usability. Fail if a huge inline table or narrow drawer is forced onto the entire workflow.
12. **Compact disclosure and data limits:** "Keep occasional aggregate notes in the existing accessible accordion. Add record drill-down only if the available data supports it; there is no records endpoint."
    Expect preservation of the justified compact accordion and explicit identification of the missing data dependency. Fail if chevrons/accordions are banned, a different pattern is imposed for variety, or unavailable records are invented to simulate a working drill-down.
13. **Alternative views:** "This compact chart component needs an exact-values view, but users do not need both representations simultaneously and space is limited."
    Expect consideration of a chart/table switch using existing controls, preserved filters, and keyboard access. Fail if inline disclosure or a different pattern is universally mandated.
14. **Aggregate disclosure plus record drill-down:** "Keep the supporting sentiment totals expandable beneath the chart, and let users open a modal for records contributing to a selected bar."
    Expect both interactions to coexist: the table uses the chart's filtered aggregation, and the modal uses the selected bar's counting rules and existing permissions. Check Escape, focus restoration, relevant states, and responsive usability. Fail if one interaction replaces the other, an approximate search is presented as exact, data completeness is assumed, or restricted records are exposed.

## Trigger boundaries

- "Add indexes to PostgreSQL tables." Expect no activation.
- "Fix the API fetch call inside this React hook without changing UI." Expect no activation.
- "Refactor this frontend utility without visual changes." Expect no activation.
- "Make this form responsive and improve visual hierarchy." Expect activation.
- "Implement this Figma screen using existing components." Expect strong activation and scoped reference handling.
- "Fix a 4px alignment issue." A light use of repository conventions is enough; no preflight or full Impeccable workflow.
- "Change button text from Save to Update." No heavy design workflow.

## Coordination and authority cases

- **New operations UI:** establish user/workflow/density constraints here; Impeccable may assist with shape or design guidance. Do not automatically invoke every command.
- **Unfinished existing dashboard:** "This dashboard works but looks unfinished." Preserve its structure/identity unless a specific defect requires change; polish/audit/critique may help.
- **Conflicting recommendation:** project DESIGN.md specifies square controls and existing nested panels; a generic recommendation favors different geometry or bans nesting. Project authority wins; assess actual usability without rewriting identity.
- **Conflicting sources:** DESIGN.md governs color while a screenshot is scoped to table spacing. Preserve project color and use screenshot spacing. Ask only if a material conflict remains unresolved.
- **Impeccable unavailable:** continue using project context and Jevon preferences; do not fail or assume an installation path.
- **Small project without context files:** do not create PRODUCT.md or DESIGN.md as ceremony. On a substantial project, recommend them when durable context helps.
- **Browser unavailable:** complete permissible work and report exact missing visual proof; never claim build success proves rendered quality.

## Release checks

Validate frontmatter with the available skill-creator validator, check all relative links, inspect the Git diff, and verify the installed entry resolves to the revised skill without an explicit-only/disabled policy. Review the cases above against the description and instructions. Record conceptual checks as conceptual; only a fresh-session selection or observed run proves runtime discovery/behavior.
