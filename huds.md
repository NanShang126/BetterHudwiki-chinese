hud can be thought of as a way to bundle and manage layouts.

```
example_hud:
  layouts:
    1:
      name: layout_name_1
      x: 35
      y: 90
    2:
      name: layout_name_2
      x: 65
      y: 90
    3:
      name: layout_name_3
      x: 40
      y: 90
    ...
```
slight difference from the layout is that the coordinates in the hud are given as a percentage of the player's screen.

this is why the position of the hud sometimes changes depending on the GUI scale.

# position of the hud changes with gui scale
![](https://i.imgur.com/Fu63YuN.png)![](https://i.imgur.com/EWKyXDN.png)

this issue is caused by the hud not scaling proportionally when changing the GUI scale.
therefore, if you want to place them in direct proportion to the GUI scale, you should use the coordinates of the HUD as 0,50,100 to reference only the end and center positions.
recommend that you then adjust the coordinates in your layout.
![](https://i.imgur.com/QSfciQJ.jpeg)

here is the file modified using the built-in hud.
default-hud.yml
```
test_hud:
  layouts:
    1:
      name: health
      x: 50
      y: 100
    2:
      name: hunger
      x: 50
      y: 100
```

default-layout.yml
```
health:
  images:
    1:
      name: health_empty
      x: -62
      y: -24
    2:
      name: health_bar
      x: -47
      y: -20
    3:
      name: armor_empty
      x: -62
      y: -9
    4:
      name: armor_bar
      x: -47
      y: -5
  animations:
    duration: 60
    x-equation: 0
    y-equation: 3cos(t/30 * pi)

hunger:
  images:
    1:
      name: hunger_empty
      x: 63
      y: -24
    2:
      name: hunger_bar
      x: 65
      y: -20
    3:
      name: air_empty
      x: 63
      y: -9
    4:
      name: air_bar
      x: 65
      y: -5
  animations:
    duration: 60
    x-equation: 0
    y-equation: 3cos(t/30 * pi)
```

![](https://i.imgur.com/GlNo8Mh.png)