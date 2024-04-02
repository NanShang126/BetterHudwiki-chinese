depends on whether the image is a single or listener.

single is used to simply place an image and is universal.

listener is used to create a variable bar, such as health.


## single

```
image_id:
  type: single
  file: "example.png"
```
you can load the example.png folder in the assets folder with the id named image_id.

## listener
```
health_bar:
  type: listener
  file: "example.png"
  split: 10
  split-type: up
  setting:
    listener:
      class: health```
