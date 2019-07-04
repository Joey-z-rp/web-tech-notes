## Normal Flow

#### Block element:
- 100% of the width of its parent element
- as tall as its content
- laid out in the block flow direction, based on the parent's `writing-mode`
- appear on a new line below the last one

#### Inline element:
- as tall as their content
- as wide as their content
- can't set width or height
-  If you want to control the size of an inline element in this manner, you need to set it to behave like a block level element with `display: block`; (or even, `display: inline-block`; which mixes characteristics from both.)
- don't appear on new lines
- sit on the same line as one another and any adjacent (or wrapped) text content, as long as there is space for them to do so inside the width of the parent block level element
- If there isn't space, then the overflowing text or elements will move down to a new line

#### Margin Collapsing
If two adjacent elements both have the margin set on them and the two margins touch, the larger of the two remains, and the smaller one disappears.

---
Reference: [Normal Flow](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Normal_Flow)