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
      name: example
      scale: 0.5
      x: 5
      y: 10
```


# texts layout

# heads layout