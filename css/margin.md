### Margin Collapsing
- The margins of adjacent siblings are collapsed (except when the latter sibling needs to be cleared past floats)
- If there is no `border`, `padding`, `inline part`, `block formatting context` created, or `clearance` to separate the `margin-top` of a block from the `margin-top` of its first child block; or no `border`, `padding`, `inline content`, `height`, `min-height`, or `max-height` to separate the `margin-bottom` of a block from the `margin-bottom` of its last child, then those margins collapse. The collapsed margin ends up **outside** the parent.
- If there is no `border`, `padding`, `inline content`, `height`, or `min-height` to separate a block's `margin-top` from its `margin-bottom`, then its top and bottom margins collapse.
