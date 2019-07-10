## Types of positioning
- **positioned element**: an element whose computed position value is either `relative`, `absolute`, `fixed`, or `sticky`. (In other words, it's anything except `static`)
- **relatively positioned element**: position value is `relative`. Offset from its normal position.
- **absolutely positioned element**: position value is `absolute` or `fixed`. Offset from its containing block. If the element has margins, they are added to the offset.
- **stickily positioned element**: treated as relatively positioned until its containing block crosses a specified threshold (such as setting `top` to value other than auto) within its flow root (or the container it scrolls within), at which point it is treated as "stuck" until meeting the opposite edge of its containing block.

### Position values:
- `static`: The element is positioned according to the normal flow of the document. The `top`, `right`, `bottom`, `left`, and `z-index` properties have no effect.
- `relative`: Keeps its space. Creates a new **stacking context** when the value of `z-index` is not auto.
- `absolute`: Positioned relative to its **closest positioned ancestor**, if any; otherwise, it is placed relative to the **initial containing block**. Creates a new **stacking context** when the value of `z-index` is not auto.
- `fixed`: Positioned relative to the **initial containing block** established by the viewport, except when one of its ancestors has a `transform`, `perspective`, or `filter` property set to something other than none, in which case that ancestor behaves as the containing block. Creates a new stacking context.
- `sticky`: The element is positioned according to the normal flow of the document, and then offset relative to its **nearest scrolling ancestor** and **containing block** (nearest block-level ancestor), including table-related elements, based on the values of `top`, `right`, `bottom`, and `left`. 

### Containing Block:
 Percentage values that are applied to the `width`, `height`, `padding`, `margin`, and `offset` properties of an absolutely positioned element are computed from the element's containing block.

 - If the position property is `static`, `relative`, or `sticky`, the containing block is formed by the edge of the **content box** of the nearest ancestor element that is a **block container** (such as an inline-block, block, or list-item element) or which establishes a **formatting context** (such as a table container, flex container, grid container, or the block container itself).
 - If the position property is `absolute`, the containing block is formed by the edge of the padding box of the nearest ancestor element that has a position value other than static
 - If the position property is `fixed`, the containing block is established by the viewport (in the case of continuous media) or the page area (in the case of paged media).
 - If the position property is `absolute` or `fixed`, the containing block may also be formed by the edge of the **padding box** of the nearest ancestor element that has the following:
1. A `transform` or `perspective` value other than `none`
2. A `will-change` value of `transform` or `perspective`
3. A `filter` value other than `none` or a `will-change` value of `filter` (only works on Firefox).
4. A `contain` value of `paint`
- The `height`, `top`, and `bottom` properties compute percentage values from the `height` of the containing block.
- The `width`, `left`, `right`, `padding`, and `margin` properties compute percentage values from the `width` of the containing block.

### Stacking Context
The stacking context is a three-dimensional conceptualization of HTML elements along imaginary **z-axis** relative to the user, who is assumed to be facing the viewport or the webpage.
- `z-index` is used to determin the rendering order of certain elements within a stacking context.
- Stacking contexts can be contained in other stacking contexts, and together create a hierarchy of stacking contexts.
- Each stacking context is completely independent of its siblings: only descendant elements are considered when stacking is processed.
- Each stacking context is self-contained: after the element's contents are stacked, the whole element is considered in the stacking order of the parent stacking context.

### Notes:
- If both top and bottom are specified (technically, not auto), top wins.
- If both left and right are specified, left wins when direction is ltr (English, horizontal Japanese, etc.) and right wins when direction is rtl (Persian, Arabic, Hebrew, etc.).