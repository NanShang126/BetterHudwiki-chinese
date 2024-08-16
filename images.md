depends on whether the image is a single or listener.

single is used to simply place an image and is universal.

listener is used to create a variable bar, such as health.


- [type: single](https://github.com/toxicity188/BetterHud/wiki/images#type-single)
- [type: listener](https://github.com/toxicity188/BetterHud/wiki/images#type-listener)
  - [split](https://github.com/toxicity188/BetterHud/wiki/images#split)
  - [split-type](https://github.com/toxicity188/BetterHud/wiki/images#split-type)
  - [class (default)](https://github.com/toxicity188/BetterHud/wiki/images#class-default)
  - [class (compatible)](https://github.com/toxicity188/BetterHud/wiki/images#class-compatible)
- [type: sequence](https://github.com/toxicity188/BetterHud/wiki/images#type-sequence)

# type: single

```
image_id:
  type: single
  file: "example.png"
```
you can load the example.png file with the id named 'image_id' in the assets folder.
![](https://i.imgur.com/WZUoAZR.png)

# type: listener
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

more you split, the more detail you can display, but it also increases the resourcepack capacity.

`split: 10`, a total of 10 resources will be created, as shown in the photo below.

![12](https://i.imgur.com/RCK4jbq.png)

## split-type

types: up, down, left, right, circle, reverse_circle

they decrease in the direction shown in the photo below.

![](https://i.imgur.com/PhjFBKa.png)


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

you can also just enter a number. ```max: 1000```

more details are covered in the [placeholder documentation](https://github.com/toxicity188/BetterHud/wiki/placeholders)

# type: sequence
an animated image.

works with 1 tick per photo.
```
test_gif:
  type: sequence
  files:
    - test/test_00000.png
    - test/test_00001.png
    - test/test_00002.png
    - test/test_00003.png
    - test/test_00004.png
    - test/test_00005.png
    - test/test_00006.png
    - test/test_00007.png
    - test/test_00008.png
    - test/test_00009.png
    - test/test_00010.png
```