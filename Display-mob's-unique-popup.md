``` yaml
monster_health:
  images:
    1:
      name: monster_empty
    2:
      name: monster_health
      x: 10
      y: 2
  texts:
    1:
      name: test_font
      pattern: "HP [entity_health] // [entity_max_health]"
      align: left
      x: 10
      y: 2
      scale: 0.5
      color: "green"
      outline: true
```
First, create a layout that represents monster's info.
``` yaml
monster_health:
  triggers:
    - attack
  duration: 60
  key-mapping: true
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
Second, create a popup that enable key mapping.  
![녹화_2024_03_09_20_34_37_639](https://github.com/toxicity188/BetterHud/assets/114675706/7798e63d-9a30-4ce8-a290-7946172d999f)  
Success!
