


## triggers

## group
create multiple popups as a group.

default: `none`

ex. `group: skill`

![](https://i.imgur.com/jvkTS02.png)


## queue
whether to save out-of-queue popups

default: `false`

By default, when set to `move.duration: 4`, popups can only be displayed for a maximum of four,

and any further requests for popups will be ignored due to lack of space.

![](https://i.imgur.com/upXOXh9.png)

when you use `queue: true`, it works like this

for example, after sending a total of 6 popups in 1 tick increments, after 1 tick, we see the following structure

![](https://i.imgur.com/39O3Mim.png)

will still see up to four popups, but will start to see a fifth popup after the first one ends.

waiting popups will also have a reduced duration. to prevent this, the following options are used

### always-check-condition

whether popups outside of the queue should also have animated ticks.

default: `true`

`always-check-condition: false`, waiting popups will not decrease in duration.

![](https://i.imgur.com/0wdOKLs.png)

## sort

options for how you want to arrange the popups.

default: `last`

`sort: first` is performed in a stack fashion,

`sort: last` is performed using queue fashion.

![](https://i.imgur.com/BMJOFP5.png)

## duration
determine the duration of the popup.

the unit is tick and will last indefinitely if not entered.

default: `0` (infinite)

## key-mapping
mapping popups with a specific key as the unique key.

this is needed, for example, to display the health bar of an entity or another player.

default: `false`

## x,y coord
in the same way as the hud, you define where to divide the player screen into percentages.

## move
set rules for placing popups when displaying multiple popups.

### duration
maximum number of popups you want to display on the screen.

## pixel
define how it should be moved pixel by pixel in the same way as layout.

### x,y-equation

it has a very close relationship with the [operations documentation](https://github.com/toxicity188/BetterHud/wiki/operations)