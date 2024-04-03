this feature is not supported for offline servers.

# how to bring your head to the hud
create a yml file in your heads folder and enter it like this.

![](https://i.imgur.com/4OA5xp8.png)
```
test_head:
  pixel: 4
```


put it on the layout.

![](https://i.imgur.com/Ric4q9Y.png)
```
outline_head:
  heads:
    0:
      name: test_head
      x: 0
      y: 0
```