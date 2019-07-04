## Specificity
- When multiple declarations have equal specificity, the **last** declaration found in the CSS is applied to the element
- Level 1: Type selectors (e.g., `h1`) and pseudo-elements (e.g., `::before`)
- Level 2: Class selectors (e.g., `.example`), attributes selectors (e.g., `[type="radio"]`) and pseudo-classes (e.g., `:hover`)
- Level 3: ID selectors (e.g., `#example`)
- Level 4: `Inline styles` always overwrite any styles in external stylesheets
- Level 5 : `!important`

### !important

---
Reference: [Specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity)