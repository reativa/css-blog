---
date: "2020-01-04"
description: ''
title: CSS como usar o Drop cap
tags: visual,beginner
---

Makes the first letter in the first paragraph bigger than the rest of the text - often used to signify the beginning of a new section.

```html
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam commodo ligula quis tincidunt cursus. Integer consectetur tempor ex eget hendrerit. Cras facilisis sodales odio nec maximus. Pellentesque lacinia convallis libero, rhoncus tincidunt ante dictum at. Nullam facilisis lectus tellus, sit amet congue erat sodales commodo.</p>
<p>Donec magna erat, imperdiet non odio sed, sodales tempus magna. Integer vitae orci lectus. Nullam consectetur orci at pellentesque efficitur.</p>
```

```css
p:first-child::first-letter {
  color: #5f79ff;
  float: left;
  margin: 0 8px 0 4px;
  font-size: 3rem;
  font-weight: bold;
  line-height: 1;
}
```

#### Explanation

- Use the `::first-letter` pseudo-element to style the first element of the paragraph, use the `:first-child` selector to select only the first paragraph.

#### Browser support

- https://caniuse.com/#feat=first-letter

[Acesse a Referência original](http://github.com/30-seconds/)
