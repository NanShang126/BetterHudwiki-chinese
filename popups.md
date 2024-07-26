- [triggers](https://github.com/toxicity188/BetterHud/wiki/popups#triggers)
  - [papi](https://github.com/toxicity188/BetterHud/wiki/popups#papi)
- [group](https://github.com/toxicity188/BetterHud/wiki/popups#group)
- [unique](https://github.com/toxicity188/BetterHud/wiki/popups#unique)
- [queue](https://github.com/toxicity188/BetterHud/wiki/popups#queue)
  - [always-check-condition](https://github.com/toxicity188/BetterHud/wiki/popups#always-check-condition)
- [sort](https://github.com/toxicity188/BetterHud/wiki/popups#sort)
- [duration](https://github.com/toxicity188/BetterHud/wiki/popups#duration)
- [key-mapping](https://github.com/toxicity188/BetterHud/wiki/popups#key-mapping)
- [x,y coord](https://github.com/toxicity188/BetterHud/wiki/popups#xy-coord)
- [move](https://github.com/toxicity188/BetterHud/wiki/popups#move)
  - [duration](https://github.com/toxicity188/BetterHud/wiki/popups#duration-1)
  - [pixel](https://github.com/toxicity188/BetterHud/wiki/popups#pixel)

popups are extremely extensible.

it's not a lie to say that almost every deep functionality you can think of comes from popups.

buff icon, skill hud, etc.

```
monster_health:
  triggers:
    1:
      class: entity_attack
  group: mob_group
  unique: true # default: false
  queue: true # default: false
  always-check-condition: false # default: true
  sort: first # types: last/first , default: last
  duration: 60 #tick
  key-mapping: true #default: false
  x: 10
  y: 35
  move:
    duration: 3
    pixel:
      x-equation: 0
      y-equation: 20t
  layouts:
    1:
      name: monster_health
```

There are several ways to run a popup.
1. run it as a command
2. register it in config.yml as a default-popup to display the popup when a condition is met. (in this case, you should not set a duration.)
3. can use a trigger

# triggers
```
monster_health:
  triggers:
    1:
      class: entity_attack
```
trigger is a feature that fires a popup when a specific action is triggered.

list of triggers is as follows and provides its own PAPI.

***

entity_attack : when player attacks an entity.

entity_damage : when player is damaged by an entity.

entity_kill : when player killed the entity

entity_dead : when player dies

## papi
trigger-only papi

```
entity_max_health
entity_health
entity_name
entity_custom_name
entity_type
entity_dead
```

# group
create multiple popups as a group.

default: `none`

ex. `group: skill`

![](https://i.imgur.com/jvkTS02.png)

# unique
Avoid duplicate popups.

default: `false`

# queue
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

## always-check-condition

whether popups outside of the queue should also have animated ticks.

default: `true`

`always-check-condition: false`, waiting popups will not decrease in duration.

![](https://i.imgur.com/0wdOKLs.png)

# sort

options for how you want to arrange the popups.

default: `last`

`sort: first` is performed in a stack fashion,

`sort: last` is performed using queue fashion.

![](https://i.imgur.com/BMJOFP5.png)

# duration
determine the duration of the popup.

the unit is tick and will last indefinitely if not entered.

default: `0` (infinite)

# key-mapping
mapping popups with a specific key as the unique key.

this is needed, for example, to display the health bar of an entity or another player.

default: `false`

# x,y coord
in the same way as the hud, you define where to divide the player screen into percentages.

# move
set rules for placing popups when displaying multiple popups.

```
  move:
    duration: 3
    pixel:
      x-equation: 0
      y-equation: 20t
```

## duration
maximum number of popups you want to display on the screen.

## pixel
define how it should be moved pixel by pixel in the same way as layout.

it has a very close relationship with the [operations documentation](https://github.com/toxicity188/BetterHud/wiki/operations)

for example, if you simply want to offset to the right by 20 pixels, you can do something like `x-equation: 20t`

![](https://github.com/toxicity188/BetterHud/assets/114675706/3bef5f14-9d94-498d-95f2-c484e5cc6ef1)

To do something like this photo 
```
buff_absorption:
  group: buff
  unique: true
  layouts:
    1:
      name: buff_absorption
      x: 90
      y: 10
  conditions:
    1:
      first: potion_effect_duration:absorption
      second: 0
      operation: ">"
  move:
    duration: 33
    pixel:
      x-equation: -floor((t - 1) / 8) * 40
      y-equation: (((t - 1) % 8) + 1) * 40
 ```
in this way, some math knowledge is required.