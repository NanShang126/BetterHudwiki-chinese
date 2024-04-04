```
layout:
  images:
    1:
      name: example
      conditions:
        1:
          first: mmocore_current_cooldown_skill:DEADLY_SQUASH
          second: 1
          operation: '>='
```
can use it almost anywhere: images, layouts (text layout, image layout), popups, huds, etc.

# operation
types: '>', '>=', '<', '<=', '==', '!='

only '==', '!=' are available for string types.

comparison works like this `first >= second`
