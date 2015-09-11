Sunfish.lua
===========

- tiny and basic chess engine for lua.
- Port of https://github.com/thomasahle/sunfish
- Pretty decent AI
- Game state readily available as a string
- inputs taken as a string
- Code is easily modifiable to plug into Torch to make a neural net play against it.
  - Simply remove main function, and plug the board into your own scripts: https://github.com/soumith/sunfish.lua/blob/master/sunfish.lua#L541-L591

##Usage

```bash
$ lua sunfish.lua



   r  n  b  q  k  b  n  r
   p  p  p  p  p  p  p  p
   .  .  .  .  .  .  .  .
   .  .  .  .  .  .  .  .
   .  .  .  .  .  .  .  .
   .  .  .  .  .  .  .  .
   P  P  P  P  P  P  P  P
   R  N  B  Q  K  B  N  R


Your move: 
e2e4


   r  n  b  q  k  b  n  r
   p  p  p  p  p  p  p  p
   .  .  .  .  .  .  .  .
   .  .  .  .  .  .  .  .
   .  .  .  .  P  .  .  .
   .  .  .  .  .  .  .  .
   P  P  P  P  .  P  P  P
   R  N  B  Q  K  B  N  R


My move:        g8f6


   r  n  b  q  k  b  .  r
   p  p  p  p  p  p  p  p
   .  .  .  .  .  n  .  .
   .  .  .  .  .  .  .  .
   .  .  .  .  P  .  .  .
   .  .  .  .  .  .  .  .
   P  P  P  P  .  P  P  P
   R  N  B  Q  K  B  N  R


Your move:

```
