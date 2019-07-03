## Main Drive
Provide a more efficient way to lay out, align and distribute space among items in a container, even when their size is unknown and/or dynamic (thus the word "flex").

### Flex Container Properties
- `flex-direction`: row | row-reverse | column | column-reverse
- `flex-wrap`: nowrap (default) | wrap | wrap-reverse
- `flex-flow`: `flex-direction` || `flex-wrap` (default: row nowrap)
- `justify-content`: flex-start | flex-end | center | space-between | space-around | space-evenly; (alignment along the **main** axis)
- `align-items`: stretch | flex-start | flex-end | center | baseline; (alignment along the **cross** axis on the **current** line, `justify-content` version for the cross-axis)
- `align-content`: flex-start | flex-end | center | space-between | space-around | stretch; (this property has **no** effect when there is only one line of flex items)

### Flex Items Properties
- `order`: 1 | 2 | 3 | ...
- `flex-grow`: 0 (default) | `positive number`
- `flex-shrink`: 1 (default) | 0 | `positive number`
- `flex-basis`: auto (default) | `length` (e.g. 20%, 5rem, etc.)
- `flex`: none | `flex-grow` `flex-shrink` `flex-basis` (default: 0 1 auto)
- `align-self`: auto | flex-start | flex-end | center | baseline | stretch (override `align-items` for individual flex items)

### Other Notes
Note that `float`, `clear` and `vertical-align` have no effect on a flex item.

---
Reference: [A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)