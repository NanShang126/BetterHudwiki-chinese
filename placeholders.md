# how do use the PlaceholderAPI
there are PAPI that work sync and PAPI that work with async 1 tick locks.

## sync PAPI
need to define a placeholder.

create a yml file in the placeholder folder and enter it as shown in the picture.

![](https://i.imgur.com/e6cF0P0.png)

(update is the update interval in ticks.)

can then use it in the following format: "[string:online]"

## async PAPI
don't need to configure anything, just use "[papi:name]".

ex.`papi:cmi_user_name`

## built-in PAPI
if you can, this is the most recommended method.

ex. [health] [mmocore-exp] ...

```
mmocore-mana
mmocore-max-mana
mmocore-stamina
mmocore-max-stamina
mmocore-stellium
mmocore-max-stellium
mmocore-party-member-count
mmocore-guild-member-count
mmocore-exp
mmocore-max-exp
mmocore-level
mmocore-stat-<>
mmocore-claims
mmocore-current-cooldown-slot-<>
mmocore-current-cooldown-skill-<>
mmocore-skill-bound-index-<>
mmocore-skill-level-<>
mmocore-class
mmocore-guild-id
mmocore-guild-name
mmocore-skill-name-<>
mmocore-is-casting-mode
mmocore-bounded-skill-<>
mmocore-bounded-slot-<>
mythicmobs-aura-stack-<>
mythicmobs-has-aura-<>
vault-money
worldguard-in-region-<>
health
food
armor
air
exp
```