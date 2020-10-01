Sunfish.lua
===========

 Sunfish is a simple, but strong chess engine, written in Python, mostly for teaching purposes. Without tables and its simple interface, it takes up just 111 lines of code! Yet it plays at rating 1800-1900 at Lichess. It’s simple open source chess engine under the GPL written by Thomas Dybdahl Ahle in Python for didactic purposes, inspired by Harm Geert Muller's Micro- Max. Sunfish supports the Chess Engine Communication protocol to play with a graphical interface like XBoard or PyChess. 
 The program uses Unicode glyphs to display the pieces within the terminal,making it look a little more chess- like than GNU chess. Moves are inputted by specifying the starting and ending co-ordinates,so the aggressive opening which moves the king's pawn to e4 would be inputted e2e4.Note that this can be slightly longer than the more common algebraic notation(in which the previous move would be written e4),but makes it much easier for computation. In this engine Lower case letters represent black pieces (p,r,n,b,k,q), and upper case letters represent white pieces (P,R,N,B,K,Q).Black-White-Empty matrix(BWE) is solely a listing of strings which represent each square on the board. This matrix is compared with an internally stored matrix within the Chess Engine.This suggests the Chess Engine can understand : 
 
i)where the piece moved from 
 
ii)where it moved to and construct a chess command from it. Moving pawn piece A2 to A4 at the beginning of the game would require command ‘a2a4’.         
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
