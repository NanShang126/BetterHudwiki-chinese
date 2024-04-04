- [Common Options](https://github.com/toxicity188/BetterHud/wiki/layouts#common-options)
  - [scale](https://github.com/toxicity188/BetterHud/wiki/layouts#scale)
  - [layer](https://github.com/toxicity188/BetterHud/wiki/layouts#layer)
  - [x,y coordinates](https://github.com/toxicity188/BetterHud/wiki/layouts#xy-coordinates)
- [images layout](https://github.com/toxicity188/BetterHud/wiki/layouts#images-layout)
- [texts layout](https://github.com/toxicity188/BetterHud/wiki/layouts#texts-layout)
  - [name](https://github.com/toxicity188/BetterHud/wiki/layouts#name)
  - [number-format](https://github.com/toxicity188/BetterHud/wiki/layouts#number-format)
  - [pattern](https://github.com/toxicity188/BetterHud/wiki/layouts#pattern)
  - [align](https://github.com/toxicity188/BetterHud/wiki/layouts#align)
  - [outline](https://github.com/toxicity188/BetterHud/wiki/layouts#outline)
- [heads layout](https://github.com/toxicity188/BetterHud/wiki/layouts#heads-layout)
- [animations](https://github.com/toxicity188/BetterHud/wiki/layouts#animations)

layout is a grouping of text and images.

it can be used in a hud or popup and has three different layouts.

here's a rough idea of the structure.

![](https://i.imgur.com/Uttt8Ad.png)

(can put conditions on almost any element.)

# Common Options
```
layout:
  y: -5
  x: 5
  images:
    1:
      name: example
      x: 10
      y: -10
      scale: 0.5
      layer: 1
```
## scale
applies to images and text.

you can increase and decrease the size.

default : 1

ex. `scale: 0.5`

## layer
priority to display when overlapping.

higher the number, the higher the priority.

default : 0

ex. `layer: 1`

## x,y coordinates
coordinates of the layout can be moved in pixels.
you can move the entire layout or customize it individually.

default : 0

ex.

`x: 10`

`y: -10`

# images layout

```
image_layout:
  images:
    1:
      name: image_id
      scale: 0.5
      x: 5
      y: 10
    2:
    ...
```
load the images you set in the [images](https://github.com/toxicity188/BetterHud/wiki/images#type-single) folder.

only common options exist.

# texts layout
```
text_layout:
  texts:
    1:
      name: example_font
      number-format: "#,###.#"
      pattern: "Lv. [mmocore_level]"
      align: center
      x: 10
      y: -10
      scale: 0.5
      outline: true
```
## name
specifies the [font](https://github.com/toxicity188/BetterHud/wiki/fonts) to use.

font is named `example_font` if you follow the documentation.

if not specified, the default font is used.

ex. `name: example_font`

## number-format
set the number format.

DecimalFormat, see the wiki for more information.

https://docs.oracle.com/javase/8/docs/api/java/text/DecimalFormat.html

default : config.yml - `number-format: "#,###.#"`

## pattern
define the text to display.

[PAPI](https://github.com/toxicity188/BetterHud/wiki/placeholders) can be used, and can be mixed with plain text.

ex. `pattern: "Lv. [mmocore_level]"`

and you can add color and text formatting.

color type : `<#hex>, <black>, <gold>, <gray>, <blue>, <green>, <aqua>, <red>, <yellow>, <white>`

format type : `bold <b>, obfuscated <obf>`

![](https://i.imgur.com/rBn9ONM.png)

![](https://i.imgur.com/SEFS5XA.png)

## align
this refers to how the text should be aligned.

types: left, center, right

ex. `align: center`

![](https://i.imgur.com/SJZ1sBv.png)

## outline
whether or not to put a drop shadow on the text.

if text is on top of an image, you can't show a drop shadow.

ex. `outline: true`

![](https://i.imgur.com/z2YJjyX.png)

# heads layout
[heads](https://github.com/toxicity188/BetterHud/wiki/heads)

# animations
animations can basically be organized by math formulas and use the exp4j library.

see the links below for more math formula wikis.

https://redmine.riddler.com.ar/projects/exp4j/wiki

use 't' as a parameter.

this example is an animation that moves up and down.
```
example_layout:
  images:
    1:
      name: image_id
  animations:
    duration: 60
    x-equation: 0
    y-equation: 3cos(t/30 * pi)
```