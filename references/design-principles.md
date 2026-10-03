# Design principles

Use these to reason about a design, not to enforce one aesthetic.

- **Domain fit:** Organize around the work. Dispatchers need queues and exceptions; shoppers may need imagery and comparison; developers need precise data and diagnostics. A familiar dashboard shell is useful only when the task fits it.
- **Hierarchy:** Make the next decision and its supporting information easy to find. Give the main action appropriate emphasis; a page heading should identify the workspace without consuming it.
- **Proximity:** Group information that users interpret together. Spacing and labels often express relationships more clearly than another enclosing card.
- **Alignment:** Establish a few shared edges and align comparable values. Right-align numeric columns, keep units clear, and use stable action placement to support scanning.
- **Rhythm:** Reuse a spacing and typography scale. Distinguish major sections from related fields through consistent intervals rather than arbitrary gaps.
- **Density:** Match the amount of visible information to task frequency, expertise, and viewport. Dense operations screens and relaxed consumer screens can both be right; protect legibility and usable targets in either.
- **Contrast:** Use contrast to express importance, state, and interactivity. Reserve accent colors for meaningful roles; keep text and controls readable across relevant themes.
- **Affordance:** Make actions recognizable as actions. Distinguish controls from labels, primary from secondary actions, and destructive actions from routine ones. Hover cannot be the only way to discover essential functionality.
- **Progressive disclosure:** Keep frequent tasks available and defer rarely needed detail. Do not hide essential navigation, errors, or decision-making information merely to simplify the screenshot.
- **Consistency:** Extend the product's established components, tokens, and interaction language. A local improvement should not leave neighboring screens looking like different products.
- **Feedback:** Show what is happening, what changed, and how to recover. Loading indicators, validation, empty states, and errors should answer a user's immediate question rather than decorate the page.
- **Accessibility:** Preserve semantics, labels, keyboard access, visible focus, contrast, and alternatives to color. Practical density must not make targets unusable; expressive visuals must not obscure meaning. Respect reduced-motion preferences when adding motion.

Choose surface treatments after information structure. Radius, borders, shadows, typography, and color should form a coherent vocabulary tied to purpose and existing conventions. No fixed palette or geometry is required.
