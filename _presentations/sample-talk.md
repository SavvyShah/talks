---
title: Sample Presentation
theme: black
---


# Welcome to Reveal.js

This is a slide.

---

## Multiple Slides

Use `---` to separate slides.

--- 

## Robust Separators

The new separator logic supports trailing spaces like `--- `.

---

## Features

- **Markdown** support
- Vertical slides
- Code highlighting

---

## Create textual Venn diagrams


<div class="venn" style="background: white;">
[ 
  {"sets": ["A"], "size": 25}, 
  {"sets": ["B"], "size": 12},
  {"sets": ["A", "B"], "size": 2}
]
</div>

---

## Supports mermaid JS

<div class="mermaid" style="background: white">
sankey
  'Agricultural waste',Bio-conversion,124.729
  Bio-conversion,Liquid,0.597
  Bio-conversion,Losses,26.862
  Bio-conversion,Solid,280.322
</div>

---

## Vertical Slide

This is a nested slide.
(Separated by vertical delimiter `--`)

--

## Sub-Slide

I am nested below the previous one!

---

## Code Example

```javascript
Reveal.initialize({
  hash: true,
  plugins: [ RevealMarkdown ]
});
```

---

## Line number focus

```js [1-2|3|4]
  let a = 1;
  let b = 2;
  let c = x => 1 + 2 + x;
  c(3);
```

---

## Use SVG

Incase your needs cannot be represented using diagrams, use https://tldraw.com and make an SVG diagram


![alt text](/talks/assets/img/dice-5.svg)

--

Because it's easy to change textual representation incase of simple changes

![alt text](/talks/assets/img/blue-dice.svg)

--

![alt text](/talks/assets/img/dice-5.svg)

--

![alt text](/talks/assets/img/dice-4.svg)