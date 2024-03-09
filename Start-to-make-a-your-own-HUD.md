![녹화_2024_03_09_12_25_07_25](https://github.com/toxicity188/BetterHud/assets/114675706/d82bab8b-c18c-402c-be0e-22734fdfa973)  
If you first install this plugin, As you can see, this HUD will be automatically generated.  

![Capture](https://github.com/toxicity188/BetterHud/assets/114675706/9cd4a09d-f246-4e1c-ac1f-d48be7d48fe6)  
I will make this HUD to show you what this plugin can. Thanks dreamcatcher!

![1](https://github.com/toxicity188/BetterHud/assets/114675706/dca822d2-9c3a-44ff-8650-2d29726173ef)  
First, you have to put the images you want to use.

``` yaml
empty_bar: #image name.
  type: single #image type.
  file: Empty_Bar.png #file location.

health_bar:
  type: listener #listener type
  file: Health_Bar.png
  split: 25
  split-type: left
  setting:
    listener:
      class: health
food_bar:
  type: listener
  file: Food_Bar.png
  split: 25
  split-type: left
  setting:
    listener:
      class: food
mana_bar:
  type: listener
  file: Mana_Bar.png
  split: 25
  split-type: left
  setting:
    listener:
      class: mmocore_mana
stamina_bar:
  type: listener
  file: Stamina_Bar.png
  split: 25
  split-type: left
  setting:
    listener:
      class: mmocore_stamina
```
Second, define your **image** in images folder.  

``` yaml
health_bar:
  images:
    1:
      name: empty_bar
    2:
      name: health_bar
      x: 6 #6 to pixel right
      y: 4 #4 to pixel down

food_bar:
  y: 15 #15 to pixel down
  images:
    1:
      name: empty_bar
    2:
      name: food_bar
      x: 6 #6 to pixel right
      y: 4 #4 to pixel down

mana_bar:
  y: 30 #15 to pixel down
  images:
    1:
      name: empty_bar
    2:
      name: mana_bar
      x: 6 #6 to pixel right
      y: 4 #4 to pixel down

stamina_bar:
  y: 45 #15 to pixel down
  images:
    1:
      name: empty_bar
    2:
      name: stamina_bar
      x: 6 #6 to pixel right
      y: 4 #4 to pixel down
```
Third, make a **image layout** to group your image.  
``` yaml
default_hud:
  conditions:
    1:
      first: dead #whether to player is dead
      second: false
      operation: "=="
    2:
      first: gamemode #player's gamemode
      second: "'CREATIVE'" #'<string' = String format
      operation: "!="
  layouts:
    1:
      name: health_bar
      x: 15 #15% right to gui
      y: 20 #20% down to gui
    2:
      name: food_bar
      x: 15 #15% right to gui
      y: 20 #20% down to gui
    3:
      name: mana_bar
      x: 15 #15% right to gui
      y: 20 #20% down to gui
    4:
      name: stamina_bar
      x: 15 #15% right to gui
      y: 20 #20% down to gui
```
Fourth, define a **HUD** to group your image layout.  
``` yaml
info: "<gold><b>[!]</gold> "
warn: "<red><b>[!]</red> "

number-format: "#,###.#"

default-hud:
  - default_hud

default-popup: []
```
Last, define your HUD to default HUD to write your HUD mane in default-hud.  
![녹화_2024_03_09_12_57_43_528](https://github.com/toxicity188/BetterHud/assets/114675706/e58d38fa-d2bc-4208-a484-4eaa904c3662)  
Success!
