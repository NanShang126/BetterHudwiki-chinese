operator uses the exp4j library.

# operator wiki
see the links below for the default operators

https://redmine.riddler.com.ar/projects/exp4j/wiki/Built_in_Operators

for math operators, see the links below.

https://redmine.riddler.com.ar/projects/exp4j/wiki/Built_in_Functions

https://redmine.riddler.com.ar/projects/exp4j/wiki/Extra_Functions_and_Operators


# example
use 't' as a parameter.

It is primarily used by [PAPI](https://github.com/toxicity188/BetterHud/wiki/placeholders), and examples of how it is used include

ex. `[player_health@t * 2]`

The value of player_health is defined as t, which in this example would be 40 if the original health was 20.

when used as a PAPI variable, it is of type string, so it needs to be defined as type number.

ex. `[(number)papi:player_x@t * 2]`

## exception
when working within a pattern in a text layout,

the divide ('/') operator uses '//'. This will change to '\' in the future.