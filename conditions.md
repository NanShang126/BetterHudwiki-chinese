```
layout:
  images:
    1:
      name: example
      conditions:
        1:
          first: (number)papi:player_x
          second: 1
          operation: '>='
```
can use it almost anywhere: images, layouts (text layout, image layout), popups, huds, etc.

displayed when the condition is met.

# operation
types: '>', '>=', '<', '<=', '==', '!='

only '==', '!=' are available for string types.

comparison works like this `first >= second`

# caution
## number text
```
      conditions:
        1:
          first: "papi:player_x"
          second: "'1'"
          operation: '=='
```
to compare numeric text when it's a string, you need to use something like "'1'".

in this case, the papi in first is not prefixed with (number), so it is a string type,

and if you put `second: 1`, it will be recognized as a number, so you will get an error.



## PAPI format
```
      conditions:
        1:
          first: "[papi:player_x]"
          second: "'1'"
          operation: '=='
```
don't use [] in conditions.