You can implement various things using the popup system.  
I will create a skill system using popups.  
![스크린샷 2024-03-09 180712](https://github.com/toxicity188/BetterHud/assets/114675706/f6da96db-15f0-4115-91af-1de3b1fe4419)  
As we learned earlier, please prepare the desired images and font files.
``` yaml
brutal_strike_layer:
  y: -8
  x: 2
  images:
    1:
      name: skill_icon_brutal_strike
      scale: 0.6
    2:
      name: skill_cooldown_brutal_strike
      scale: 0.6
  texts:
    1:
      name: itim_skill
      pattern: "[mmocore_skill_level:BRUTAL_STRIKE]"
      layer: 1
      color: yellow
      outline: true
      x: 16
      y: 10
      align: center
    2:
      name: itim
      scale: 0.5
      pattern: "[mmocore_current_cooldown_skill:BRUTAL_STRIKE]"
      layer: 1
      color: yellow
      number-format: "#,###"
      outline: true
      x: 9
      align: center
      conditions:
        1:
          first: "mmocore_current_cooldown_skill:BRUTAL_STRIKE"
          second: 1
          operation: ">"
    3:
      name: itim
      scale: 0.5
      pattern: "[mmocore_current_cooldown_skill:BRUTAL_STRIKE]"
      layer: 1
      color: yellow
      outline: true
      x: 9
      align: center
      conditions:
        1:
          first: "mmocore_current_cooldown_skill:BRUTAL_STRIKE"
          second: 1
          operation: "<="
        2:
          first: "mmocore_current_cooldown_skill:BRUTAL_STRIKE"
          second: 0
          operation: ">"
```
Please create layouts corresponding to each skill.
``` yaml
brutal_strike_popup: #popup name
  unique: true
  group: skill #popup group
  x: 50 #gui location
  y: 100
  index: "mmocore_skill_bound_index:BRUTAL_STRIKE@t - 2"
  layouts:
    1: 
      name: brutal_strike_layer
  move:
    duration: 6 #maximum popup index
    gui: 
      x-equation: 0
      y-equation: 0
    pixel:
      x-equation: -60 + 24(t - 1) #a location that each popup will locate.
      y-equation: 0
  conditions:
    0:
      first: mmocore_is_casting_mode
      second: true
      operation: "=="
    1:
      first: "mmocore_bounded_skill:BRUTAL_STRIKE"
      second: true
      operation: "=="
charge_popup:
  unique: true
  group: skill #sets the same group to join popup..
  x: 50
  y: 100
  index: "mmocore_skill_bound_index:CHARGE@t - 2"
  layouts:
    1: 
      name: charge_layer
  move:
    duration: 6
    pixel:
      x-equation: -60 + 24(t - 1)
      y-equation: 0
  conditions:
    0:
      first: mmocore_is_casting_mode
      second: true
      operation: "=="
    1:
      first: "mmocore_bounded_skill:CHARGE"
      second: true
      operation: "=="
```
Then, you should make a popup like this.
```
default-popup: 
  - brutal_strike_popup
  - charge_popup
  - shield_barrier_popup
  - judgement_popup
  - rampage_popup
  - chain_hook_popup
```
Finally, make this popup to default.  
![녹화_2024_03_09_17_33_45_816](https://github.com/toxicity188/BetterHud/assets/114675706/5f6c5403-947f-4244-8a00-2ab9383c5761)  
Success!