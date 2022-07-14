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

# css units

- [resource 1](https://www.raresportan.com/css-units/)
- [resource 2](https://every-layout.dev/rudiments/units/)

# flexbox

```css
.container {
  display: flex;

  /* flex-direction: row column row-reverse column-reverse; */
  flex-direction: row;

  /* wrap: wrap no-wrap; */
  flex-wrap: wrap;

  /* HORIZONTAL X-AXIS justify-content: space-around space-between flex-start flex-end center; */
  justify-content: flex-start;

  /* VERTICAL Y-AXIS align-items: space-around space-between stretch flex-start flex-end center baseline; */
  align-items: space-around;
}

.item {
  /* order: 0; */
  order: 1;

  /* flex: grow shrink basis; */
  flex: 1 1 100px;

  /* align-self: ...; OVERRIDES PARENT */
  align-self: flex-start;
}
```

# css grid

```css
.container {
  display: grid;

  /* 3 columns */
  grid-template-columns: auto auto auto;

  /* 2 rows */
  grid-template-rows: auto auto;

  /* start, end, space-around, space-evenly */
  justify-content: start;

  /* space-between, space-evenly, end, start */
  align-content: ;

  grid-column-gap: ;

  grid-row-gap: ;

  grid-gap: column row;
}

/* line is the core-concept of grid */
.item {
  /* grid-column: start / end; */
  grid-column: 1 / 3;
  grid-column: 1 / span 2;

  /* grid-row: start / end; */
  grid-row: 1 / 3; /* start at rwo 1 to 3 */
  grid-row: 1 / span 2; /* start at row 1 and span 2 rows */

  /* short-hand */
  grid-area: row-start / col-start / row-end / col-end;
  grid-area: 1 / 2 / span 2 / span 3;
}
```

# transition property

```css
selector {
  ...: ...;

  /* transition: elements duration style delay; */
  transition: all 300ms ease 0.3s;

  /* browser support - chrome, safari - webkit */
  -webkit-transition: ...;
  /* moz firefox */
  -moz-transition: ...;
  /* opera */
  -o-transition: ...;
}

selector:hover {
  ...: ...;
}
```

# transformation function

```css
selector {
  ...: ...;

  transform: ...;
}
```

# animation

```css
@keyframes some-animation-name {
  from {
  }

  to {
  }

  0% {
  }

  50% {
  }

  100% {
  }
}

selector {
  animation-name: some-animation-name;
  animation-duration: 4s;
  animation-timing-function: linear;
  animation-delay: 2s;
  animation-iteration-count: infinite;
  animation-direction: normal;

  /* shorthand */
  animation: some-animation-name 4s linear 2s infinite normal;

  /* cross browser */
  -webkit-animation: some-animation-name 4s linear 2s infinite normal;
  -moz-animation: some-animation-name 4s linear 2s infinite normal;
  -ms-animation: some-animation-name 4s linear 2s infinite normal;
  -o-animation: some-animation-name 4s linear 2s infinite normal;
}
```
