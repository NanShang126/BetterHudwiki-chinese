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
      x: 65
      y: 90
    ...
```
slight difference from the layout is that the coordinates in the hud are given as a percentage of the player's screen.

this is why the position of the hud sometimes changes depending on the gui scale.

# position of the hud changes with gui scale
![](https://i.imgur.com/EWKyXDN.png)![](https://i.imgur.com/Fu63YuN.png)
