# Conceptual before/after patterns

These illustrate decisions, not a component library or mandatory layout.

## Shipment operations
**Before:** Four decorative KPI cards consume half the viewport above a shipment table.

**Better:** A compact operational summary shows delayed and unassigned shipments above filters and the queue. Keep a metric card only when its trend or comparison informs an action.

**Reason:** Dispatchers need to identify and resolve exceptions quickly.

## Record metadata
**Before:** Every date, owner, identifier, and state is a colored pill.

**Better:** Use plain text for metadata, align comparable fields, and reserve status badges for meaningful states. Use removable chips for active multi-select filters when appropriate.

**Reason:** The important state becomes visible when ordinary metadata stops competing with it.

## Complex editing
**Before:** A multi-section edit form sits inside a small scrolling modal.

**Better:** Use a dedicated edit page or suitable side panel with grouped fields and reachable actions. Retain a dialog for a bounded confirmation or short contextual edit.

**Reason:** The workflow needs space, validation context, and predictable navigation.

## Developer monitoring
**Before:** A gradient welcome header, decorative usage chart, and large rounded panels dominate the screen.

**Better:** Prioritize failing runs, a compact filter bar, precise timestamps, error details, and logs. Add a chart only if a trend helps diagnosis.

**Reason:** Diagnosis needs exact information and visible failures.

## Consumer discovery
**Before:** Apply a dense enterprise table because density is considered universally preferable.

**Better:** Use accessible imagery, readable descriptions, clear comparison, and enough space for touch interaction when customers browse products.

**Reason:** Domain fit matters more than a global preference for minimalism or density.

## Responsive records
**Before:** Convert every wide table row into a large mobile card, repeating all labels.

**Better:** Prioritize key columns and offer deliberate horizontal scrolling or a detail view. Use cards when records are independent and comparison is unimportant.

**Reason:** Preserve the user's task rather than mechanically changing the container.

## Scoped references
**Before:** Mix Reference A's navigation, B's colors, and C's hero effects despite a request to use B only for table styling and C only for typography.

**Better:** Apply A to navigation, B to table treatment, and C to type hierarchy, adapting each to the existing tokens.

**Reason:** Explicit scopes prevent incoherent combinations and unnecessary rebranding.

## Explicit visual direction
**Before:** Remove requested gradients and rounded cards solely because they appear on an anti-pattern list.

**Better:** Honor the requested treatments, assign them consistent roles, keep contrast readable, and preserve useful information density. Explain a material usability conflict if one remains.

**Reason:** The skill guides judgment; it does not override explicit user intent.
