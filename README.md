# svg.pattern.js

This is a plugin for the [svg.js](http://svgjs.com) library for adding patterns.

Svg.pattern.js is licensed under the terms of the MIT License.


## Usage

Include this plugin after including svg.js in your html document.

Patterns work very much like gradients, you only have to define the tile size:

```javascript
var pattern = draw.pattern(20, 20, function(add) {
  add.rect(10, 10).fill('#000')
  add.rect(10, 10).move(10, 0).fill({ color: '#000', opacity: 0.5 })
  add.rect(10, 10).move(0, 10).fill({ color: '#000', opacity: 0.5 })
})

var circle = draw.circle(200, 200).fill(pattern)
```

This will fill the circle with a checkered pattern. There is a lot more to patterns. Please refer to the [Patterns section](http://www.w3.org/TR/SVG/pservers.html#Patterns) of the SVG specification.