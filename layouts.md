layout is a grouping of text and images.

it can be used in a hud or popup and has three different layouts.

here's a rough idea of the structure.

![](https://i.imgur.com/ajoZlxb.png)

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

## pattern
define the text to display.

[PAPI](https://github.com/toxicity188/BetterHud/wiki/placeholders) can be used, and can be mixed with plain text.

ex. `pattern: "Lv. [mmocore_level]"`

## align
this refers to how the text should be aligned.

types: left, center, right

ex. `align: center`

![](https://i.imgur.com/SJZ1sBv.png)

## outline
whether or not to put a drop shadow on the text.

ex. `outline: true`

![](https://i.imgur.com/z2YJjyX.png)

# heads layout
[heads](https://github.com/toxicity188/BetterHud/wiki/heads)