## try "/hud reload" does not move the y coordinate.

will also need to reapply the resourcepack.

## hud doesn't appear

![](https://i.imgur.com/5F0IrKW.png)

no resourcepack were applied.

if using itemsadder, do this

https://github.com/toxicity188/BetterHud/wiki/How-to-install

## don't see any bossbars, don't see any hud, it's clean.

if you're using itemsadder, will need to set text-effect to false.

https://github.com/toxicity188/BetterHud/wiki/Caution

## if the bossbar for enderdragon or wither pops up, the hud is out of alignment.

config.yml `merge-boss-bar: false`

this is a specialized bossbar and cannot be resolved.

## Optimize resourcepack

1. config.yml(if dont't use shader.yml hotbar.disable: true)

`load-minecraft-default-textures: false`

2. font.yml (if don't use default font) `scale: 1`

3. minimize font usage types