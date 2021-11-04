# Responsive SVG

Provides a twig filter for rendering SVG stacks with cross-browser responsive resizing.
See https://www.drupal.org/project/responsive_svg

## Features

- SVGs will resize responsive in every browser.
- Render the whole stack inline to avoid usage of svg4everybody.
- Manipulate the width/height of the viewBox to achieve any responsive behaviour you like to have.
- *ToDo:* Render any SVG, not only stacks.

## Usage

```
{{ 'stack-name#symbol-id' | responsiveSVG(options) }}
```

### Options

All options are optional.

```
class
    Set the value for the class attribute of the svg element
width
    Width of the svg. If not supplied, the value from the viewBox attribute of the svg element is used.
height
    Height of the svg. If not supplied, the value from the viewBox attribute of the svg element is used.
offsetX
    Extra width to adjust the aspect ratio of the svg.
offsetY
    Extra height to adjust the aspect ratio of the svg.

```

### Using inline svgs to avoid IE polyfill.

`{{ 'stack-name' | responsiveSourceSVG }}`

