# how do use the PlaceholderAPI
there are PAPI that work sync and PAPI that work with async 1 tick locks.

this method can cause memory leaks depending on how the plugin providing the PAPI handles it.

## sync PAPI
need to define a placeholder.

create a yml file in the placeholder folder and enter it as shown in the picture.

```
test:
  variable: online
  placeholder: "%server_online%"
  update: 20
```

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
mmocore_mana
mmocore_max_mana
mmocore_stamina
mmocore_max_stamina
mmocore_stellium
mmocore_max_stellium
mmocore_party_member_count
mmocore_guild_member_count
mmocore_exp
mmocore_max_exp
mmocore_level
mmocore_stat:name
mmocore_claims
mmocore_current_cooldown_slot:number
mmocore_current_cooldown_skill:name
mmocore_skill_bound_index:name
mmocore_skill_level:name
mmocore_class
mmocore_guild_id
mmocore_guild_name
mmocore_skill_name:name
mmocore_is_casting_mode
mmocore_bounded_skill:name
mmocore_bounded_slot:number
mmocore_required_mana_skill:name
mmocore_required_stamina_skill:name
mmocore_casting_slot:name
[skript_variable:%{test::%uuid of hud player%}%]
mythicmobs_aura_stack:name
mythicmobs_has_aura:name
vault_money
worldguard_in_region:name
health
food
armor
air
exp
hotbar_slot
```