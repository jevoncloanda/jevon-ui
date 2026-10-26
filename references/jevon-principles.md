# Jevon's design preferences

These preferences apply after the design authority in [SKILL.md](../SKILL.md). They guide choices where the project leaves room; they are not a universal palette, geometry, or layout.

## Match the work

- **Operations/logistics:** make queues, tables, actionable statuses, and exceptions central. Operational software should not sacrifice workspace density merely to look premium.
- **Enterprise/ERP/admin/dashboards:** favor useful information density for frequent tasks, without reducing legibility, accessibility, or usable targets. Keep frequent actions and functional shortcuts accessible; limit repeated onboarding and decorative feature explanations on frequently visited pages.
- **Developer tools/monitoring:** prioritize precise data, logs, errors, timestamps, and visible status. Do not turn technical content into a decorative costume.
- **Finance:** preserve trustworthy data presentation, units, comparisons, and clear action consequences.
- **Consumer:** allow expression, imagery, simpler navigation, and breathing room when they fit browsing or touch use. Enterprise density is not the default.
- **Brand/marketing/portfolio:** give identity, storytelling, and art direction room to lead. Do not force a task workspace onto a campaign or showcase.

These are starting points. The surface's audience and workflow determine the direction, not its category name alone.

## Preserve the product

Extend existing components, tokens, utilities, layout conventions, and interaction patterns. Consistency across neighboring screens usually matters more than an isolated supposedly better component. Preserve intentional typography, spacing, border/radius rules, navigation, and responsive behavior unless changing them is in scope.

For focused work, do not redesign unrelated screens, replace libraries unnecessarily, rewrite the design system to improve one feature, or add dependencies without concrete need. Put a fix at the layer that owns it; a shared defect may justify a shared correction, not a broader aesthetic rewrite.

## Question defaults, not treatments

Cards, pills, gradients, shadows, charts, icons, and large headings need a product or design reason. Do not default to repeated three- or four-column KPI-style layouts without actual KPIs, ornamental charts, or generous empty space when users need a working queue. Do not invent statistics, activity data, filters, tabs, copy, or widgets merely to fill the composition.

These are not bans. An expressive music app may legitimately use gradients; a portfolio may need large typography; independent records may fit cards. Respect explicit intent and established identity. When a treatment obstructs the task, describe that concrete impact rather than rejecting its style by name.

Use Impeccable for broader theory and detailed anti-pattern analysis when useful; keep the final judgment grounded in this product.

## Compose around content and purpose

Design around the user's actual task and the content's importance, not a predetermined number of equally sized cards. Before choosing a grid or container, distinguish primary and secondary functional content, informational guidance, navigation shortcuts, status messages, supporting metadata, and decorative or optional content. Let these roles determine emphasis, placement, width, and height; multiple sections alone do not justify a symmetrical dashboard.

- Give primary work the space its data and interactions require: a table or operational workflow may need the main workspace, while an interactive Favorites collection deserves a meaningful functional section.
- Keep supporting content proportional: a keyboard shortcut can be a compact hint, a status message an inline notice, and a short explanation unboxed text rather than a full-width panel. Navigation shortcuts can form a compact grid without large enclosing cards.
- Prefer purposeful asymmetry when needs differ: a main area with a smaller utility sidebar, variable-width columns, or a full-width functional section followed by a compact hint. Do not give unrelated functions equal dimensions or visual weight by default.
- Size containers to useful content. Question oversized cards with one or two lines, equal-height stretching that creates accidental empty space, and repeated surfaces added to fill a page. Preserve whitespace when it supports focus, legibility, or the product's intended rhythm.
- Use fewer, meaningful surfaces. Reserve cards for distinct semantic groups or interaction boundaries; use spacing, dividers, typography, and subtle backgrounds when they communicate grouping more clearly. Nest cards only when the additional boundary helps users understand or act on the content, rather than boxing every label, instruction, shortcut, or item.

**Before:** Quick Navigation instructions and an interactive Favorites collection occupy equal-width, equal-height cards, leaving the instructions mostly empty. **After:** Favorites leads as a functional section; navigation actions form compact shortcuts and the keyboard instruction becomes a small adjacent or following hint. Use the product's existing visual language.

On smaller screens, adapt roles rather than merely stacking desktop boxes: keep a utility hint compact, let a functional grid become one or two columns as space permits, and preserve primary-task prominence. Reconsider fixed heights and placement so secondary guidance does not consume the first screen ahead of useful work.

These are judgment guidelines, not bans on two columns, equal-width cards, nested cards, symmetry, or generous whitespace. Balanced peer content may warrant equal treatment; asymmetry should follow content needs rather than become another template. A purpose-built enterprise interface should reflect its real workflow and identity, rather than defaulting to a generic SaaS analytics dashboard.

## Reveal data in context

Choose how additional data is revealed based on the user's task and information hierarchy, not to avoid a particular UI pattern. First distinguish precise values for the chart's existing aggregation from deeper investigation of a selected element. Ask whether simultaneous chart and table visibility helps, whether the data naturally belongs beneath the chart, whether it remains manageable inline, and how much workspace and retained context users need. Consider access frequency and alternatives without automatically favoring toggles, overlays, or navigation. If straightforward presentation is sufficient, do not add an interaction or extra state.

Choose using the task and available data, reusing existing application controls and navigation:

| Pattern | Fits when | Keep in mind |
| --- | --- | --- |
| Chart + expandable supporting table | The chart shows patterns and the table supplies precise aggregate values; seeing both helps and the data fits inline. | Recommended for analytical dashboards with time series, grouped comparisons, or category counts when these needs apply. Keep the chart visible with its supporting table beneath it in the same component/card. |
| Chart/table toggle | The views are alternatives with little benefit from seeing both, or simultaneous presentation is impractical in the available space. | Put a small view switch near the title or controls; do not switch solely for a cleaner appearance or replace a useful expandable table by default. |
| Contextual drill-down, including a modal | Users investigate deeper information for a selected point, segment, category, period, or record group. | Make the relevant visual element an entry point where practical, provide a keyboard-accessible alternative, and scope details to the selection. A bounded drill-down modal can coexist with a supporting aggregate table. |
| Detail drawer | Supporting information or record details must retain dashboard context. | Keep the scope bounded; large datasets and complicated workflows need more room than a narrow drawer. |
| Dedicated detail view | Investigation needs extensive tables, filters, sorting, pagination, exports, or several steps. | Use a workspace suited to the task rather than expanding an enormous table below a chart. |
| Inline tabs or segmented views | A component has a few distinct perspectives, such as Overview, Breakdown, and Records. | Do not hide content behind tabs when a simpler presentation works. |
| Popover | A brief definition, explanation, or lightweight comparison helps in place. | Keep large datasets and primary interactions out of popovers. |
| Accordion/disclosure | Secondary, compact content naturally belongs beneath its parent. | Use a meaningful label and accessible open/close behavior; avoid repeating vague blue-chevron links by default. |
| Modal dialog | A bounded inspection or focused task benefits from temporarily isolating attention. | Preserve a clear return to the originating context and follow established dialog conventions. |

For an expandable supporting table, keep it collapsed by default unless the workflow warrants otherwise. Expand beneath the visualization, preserving both views. Reuse the same underlying dataset and active filters without another backend request when the aggregates are already available. Use contained scrolling or pagination for longer tables that remain suitable inline; choose a dedicated workspace when the investigation outgrows the component. Aggregate disclosure provides precise numbers; a chart-click drill-down reveals deeper information, such as records contributing to a sentiment bar. They serve different purposes and can coexist.

Integrate the supporting-data control as a natural continuation of the chart component. A quiet full-width row with a light separator, a compact footer action, a secondary toolbar control, or a restrained text-and-icon section header can fit. Choose according to the existing layout, importance, access frequency, horizontal space, and other chart controls. Use contextual labels such as "Monthly sentiment breakdown", "Topic counts by period", or "View monthly figures"; a short description, table icon, or trailing expand indicator is optional. These are examples, not a naming formula or mandatory appearance.

Avoid repeating a bright blue "View aggregate data" chevron link as the only treatment, oversized accordion headers, heavy nested cards, excessive borders, and decorative chevrons without semantic purpose. Place other actions near the relevant title, selected value, or toolbar; labels such as "View records" or "Inspect details" should describe their actual outcome and distinguish ambiguous targets. Follow consistent product conventions without forcing every chart's controls into identical positions or structures. Avoid disorienting page expansion, but preserve useful inline disclosure; do not introduce visual differences merely for variety.

Apply the skill's accessibility and state-completeness requirements to each disclosure: prefer native semantic disclosure controls or an accessible equivalent, support keyboard operation and visible focus, announce expanded/collapsed or selected state, and associate controls with their content. Keep inline content in logical document order and avoid moving focus unnecessarily on expansion. Use screen-reader-friendly tables with meaningful headers. Dialogs need Escape dismissal and focus restoration; provide predictable back/close behavior for the chosen pattern. Preserve relevant filters and selection on return, support smaller screens without horizontal overflow of the whole page, and handle loading, empty, and error states. Respect reduced-motion preferences when animating; do not add unnecessary animation or complex state management.

Keep chart and supporting table values synchronized to the same filtered aggregation. A selected-element drill-down must follow that point's counting rules; an approximate search is not an exact drill-down. Distinguish aggregate tables from record-level tables when sizing the workspace, and do not assume data completeness or that every chart needs record-level detail. Reuse existing data structures, permissions, and navigation; never invent underlying records, breakdowns, or metadata, expose restricted records through new endpoints, or add APIs merely to reproduce available aggregates. If an interaction requires an unavailable endpoint or additional data, identify the dependency rather than simulating working functionality.

Expandable data sections, accordions, chevrons, inline tables, toggles, modals, drawers, dedicated pages, and reusable disclosure components remain legitimate choices. The issue is unintentional repetition of generic treatments, not familiar functionality. Preserve a functional expandable table when it fits the task; prefer the simplest interaction that supports understanding and investigation.
