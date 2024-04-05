


## triggers

## group
create multiple popups as a group.

default: `none`

ex. `group: skill`

![](https://i.imgur.com/jvkTS02.png)


## queue
By default, when set to `move.duration: 4`, popups can only be displayed for a maximum of four,

and any further requests for popups will be ignored due to lack of space.

![](https://i.imgur.com/upXOXh9.png)

when you use `queue: true`, it works like this

for example, after sending a total of 6 popups in 1 tick increments, after 1 tick, we see the following structure

![](https://i.imgur.com/39O3Mim.png)

will still see up to four popups, but will start to see a fifth popup after the first one ends.

waiting popups will also have a reduced duration. to prevent this, the following options are used

### always-check-condition

`always-check-condition: true`, waiting popups will not decrease in duration.

![](https://i.imgur.com/0wdOKLs.png)

## sort

## duration

## key-mapping

## x,y coord

## move

### duration

## pixel

### x,y-equation