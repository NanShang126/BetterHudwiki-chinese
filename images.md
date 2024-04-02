depends on whether the image is a single or listener.

single is used to simply place an image and is universal.

listener is used to create a variable bar, such as health.


# single

```
image_id:
  type: single
  file: "example.png"
```
you can load the example.png folder in the assets folder with the id named image_id.


# listener
```
health_bar:
  type: listener
  file: "example.png"
  split: 10
  split-type: up
  setting:
    listener:
      class: health
```

## split

more you split, the more detail you can display, but it also increases the resource pack capacity.

split: 10, a total of 10 resources will be created, as shown in the photo below.

![12](https://i.imgur.com/RCK4jbq.png)

## split-type

types: up, down, left, right

they decrease in the direction shown in the photo below.

![](https://i.imgur.com/y0pyDB6.png)

## class (default)
built-in listeners
```
health
food
armor
air
exp
absorption
placeholder (details below)
```

## class (compatible)
compatible plugins listeners
```
mmocore_mana
mmocore_stamina
mmocore_stellium
mmocore_experience
```


## placeholder listener
if you don't find what you're looking for, you can still create custom listeners using the PAPI.
```
health_bar:
  type: listener
  file: "example.png"
  split: 10
  split-type: up
  setting:
    listener:
      class: placeholder
      value: "(number)papi:mmocore_health"
      max: "(number)papi:mmocore_max_health"
```
1. class as a placeholder
2. value is current value
3. max is maximum value

PAPI is a string by default, so you need to prefix it with (number)

You can also just enter a number. ```max: 1000```

more details are covered in the placeholder documentation.