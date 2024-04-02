ability to use multiple custom fonts.

see the layouts documentation for instructions on how to use it.

#how to add fonts
1. put files with extensions like ttf and otf in the fonts folder.
![](https://i.imgur.com/C2NbdUf.png)

2. create a yml file in the texts folder with a name of your choice.
![](https://i.imgur.com/r9TLnQR.png)

3. enter the following
```
example_font:
  file: example.ttf
  scale: 16
```

# how to change the first bossbar font
1. font.yml `merge-default-bitmap: false`

2. place the font file in the betterhud plugin folder and modify the font name in config.yml.
![](https://i.imgur.com/6BzNqrc.png)
