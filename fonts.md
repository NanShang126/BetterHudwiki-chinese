ability to use multiple custom fonts.

see the layouts documentation for instructions on how to use it.

# how to add fonts
1. put files with extensions like ttf and otf in the fonts folder.

![](https://i.imgur.com/C2NbdUf.png)

2. create a yml file in the texts folder with a name of your choice.

![](https://i.imgur.com/r9TLnQR.png)

3. enter the following
``` yaml
example_font:
  file: example.ttf
  scale: 16
```

## use minecraft font
Note: this mimics the Minecraft default font and does not use the default font, so you cannot use image fonts such as glyphs added by plugins like itemsadder.
``` yaml
default_font:
  scale: 16
  merge-default-bitmap: true
```

## how to add a glyph
``` yaml
example_font:
  file: example.ttf
  scale: 16
  images:
    star:
      name: "star.png"
      x: 0
      y: 0
      scale: 2.0
```
can add an image with this feel and then use it in the same way as `<image:star>` in a text layout pattern.

# how to change the first bossbar font
1. font.yml `merge-default-bitmap: false`

2. place the font file in the betterhud plugin folder and modify the font name in config.yml.
![](https://i.imgur.com/6BzNqrc.png)

## Use minecraft unifont
``` yaml
font:
  file: some_name
  use-unifont: true
```
you can use minecraft default unifont by using this configuration.

## Exclude other languages
``` yaml
scale: 16
height: 8
ascent: 7
merge-default-bitmap: true
use-unifont: true
include:
- korean
```
if you want to reduce your resource pack size, you can nominate some language by using "include" configuration.
Latin alphabet always be included, and there are other language like this:

- korean
- japan
- china
- russia
- bengal
- thailand
- greece
- hindi
- arab
- hebrew
