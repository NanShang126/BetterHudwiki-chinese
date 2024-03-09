![2](https://github.com/toxicity188/BetterHud/assets/114675706/cfbd1c5d-bdd9-4b47-b910-c9a36175366a)  
Before starting, it would be helpful if you have your ttf file ready. Put it in your **fonts** folder.  

``` yaml
itim:
  file: itim.ttf #Optional. defines your ttf location.
  scale: 16 #Rendering scale. The greater that value, The bigger resource pack size.
```
First, you have to define your text in your texts folder.

``` yaml
health_bar:
  images:
    1:
      name: empty_bar
    2:
      name: health_bar
      x: 6 #6 to pixel right
      y: 4 #4 to pixel down
  texts:
    1:
      name: itim
      pattern: "[health] // [max_health]" #[value] -> Placeholder
      number-format: "#,###" #number format
      outline: true #whether to outline
      layer: 1 #layer number
      color: green #text color
      scale: 0.5
      x: 10
      align: left

food_bar:
  y: 15 #15 to pixel down
  images:
    1:
      name: empty_bar
    2:
      name: food_bar
      x: 6 #6 to pixel right
      y: 4 #4 to pixel down
  texts:
    1:
      name: itim
      pattern: "[food] // 20"
      number-format: "#,###"
      outline: true
      layer: 1
      color: green
      scale: 0.5
      x: 10
      align: left

mana_bar:
  y: 30 #15 to pixel down
  images:
    1:
      name: empty_bar
    2:
      name: mana_bar
      x: 6 #6 to pixel right
      y: 4 #4 to pixel down
  texts:
    1:
      name: itim
      pattern: "[mmocore_mana] // [mmocore_max_mana]"
      number-format: "#,###"
      outline: true
      layer: 1
      color: green
      scale: 0.5
      x: 10
      align: left

stamina_bar:
  y: 45 #15 to pixel down
  images:
    1:
      name: empty_bar
    2:
      name: stamina_bar
      x: 6 #6 to pixel right
      y: 4 #4 to pixel down
  texts:
    1:
      name: itim
      pattern: "[mmocore_stamina] // [mmocore_max_stamina]"
      number-format: "#,###"
      outline: true
      layer: 1
      color: green
      scale: 0.5
      x: 10
      align: left
```
Second, marge the text in your layout by following this.  
![녹화_2024_03_09_13_22_08_73](https://github.com/toxicity188/BetterHud/assets/114675706/03e2da4a-6b11-428b-93bf-0e59ea75c6e4)  
Success!

