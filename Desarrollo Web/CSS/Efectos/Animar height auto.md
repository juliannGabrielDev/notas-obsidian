---
tags:
  - css
  - efectos
---
```css
article {
    height: 150px;
    overflow: hidden;
    transition: height .5s;
    interpolate-size: allow-keywords;
}

article:hover {
    height: auto;
}
```