# learn css

A playground for random and usefull css experiments.

- [CSS Crash Course](https://www.youtube.com/watch?v=1Rs2ND1ryYc)

# selectors

```css
/*
    - Element selector (here -> body)
    - 1 point
*/
body {
  background: red;
}

/*
    - Class selector
    - 10 points
*/
.classname {
  xyz: abc;
}

/*
    - ID selector
    - 100 points
*/
#someID {
  xyz: abc;
}

/* 
    - evaluating to higher point is prefered by the browser "CSS Specificity"
    - Element < Class < ID < Inline Style
*/
```

# psuedoselectors

```css
selector:hover {
}

selector:active {
}

selector:focus {
}

selector:first-child {
}

selector:last-child {
}

selector:nth-child(n) {
}

selector:only-child {
}

selector:link {
}

selector:visited {
}
```

# advanced selectors

```css
/* adjacent selector */
selector + selector {
}

/* general sibling selector */
selector ~ selector {
}

/* child selector */
selector > selector {
}

/* descendant selector */
selector selector {
}
```

# attribute selectors

```css
selector[attribute="value"] {
}

/* value starts with "..." */
selector[attribute^="value"] {
}

/* value ends with "..." */
selector[attribute$="value"] {
}

/* if contains value in attribute */
selector[attribute*="value"] {
}

/* similar to *; but specific */
selector[attribute~="value"] {
}

/* unclear */
selector[attribute|="value"] {
}
```

# properties

```css
selector {
  property: value;
  ...;
}
```

# type of colors

```css
/* hex code */
selector {
  property: #0f0f0f;
  /* #RRGGBB */
}

/* decimal code */
selector {
  property: rgb(0, 125, 255);
}

/* rgb alpha, alpha -> opacity [0-1] */
selector {
  property: rgba(0, 0, 0, 0.4);
}

/* gradient */
selector {
  /* linear-gradient(direction, ...colors); */
  property: linear-gradient(to right, red, green, blue);

  /* radial-gradient(shape, ...colors) */
  property: radial-gradient(circle, red 20%, green, blue);
}
```
