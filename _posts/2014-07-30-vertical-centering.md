---
sourceurl: http://zerosixthree.se/vertical-align-anything-with-just-3-lines-of-css/
tags:
  - CSS
  - layout
---

Sebastian Ekström shows us three lines for vertically centering anything in CSS:

```
.element {
  position: relative;
  top: 50%;
  transform: translateY(-50%);
}
```

i'd [solve it with flexbox][flexbox] (prefixed support about the same, better unprefixed support)

[flexbox]: http://philipwalton.github.io/solved-by-flexbox/demos/vertical-centering/
