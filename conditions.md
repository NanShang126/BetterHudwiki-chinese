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
          gate: or
```
can use it almost anywhere: images, layouts (text layout, image layout), popups, huds, etc.

displayed when the condition is met.

# operation
types: '>', '>=', '<', '<=', '==', '!='

only '==', '!=' are available for string types.

comparison works like this `first >= second`

# gate
types: and , or
`default: and`

sets the method of the condition.

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

(vice versa)

## PAPI format
```
      conditions:
        1:
          first: "[papi:player_x]"
          second: "'1'"
          operation: '=='
```
don't use [] when using PAPI in conditions.