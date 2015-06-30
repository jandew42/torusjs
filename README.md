*See example [here](http://jandew.ersoft.org/torusjs/example.html).*

The Game
========

Torus is a board game similar in design to Go,
but instead is simplified to have rapid local victory
while complication arises from orthogonal methods
of capture and win.

Specifically, the rules are:

1. The board is a 9x9 grid on a toroid.
   (This can be thought of as a normal 9x9 board,
   but to the left of the left side is the right side and vice-versa,
   and above the top side is the bottom and vice-versa.)
2. A win is triggered by Go capture conditions on exactly one opponent piece.
   (That is, to have your pieces occupying each of the four spots
   immediately above, below, left of, and right of an opponent piece.)
3. A capture is triggered by a diagonal chain of opponent's pieces being
   ended by your pieces on either side.
   (This requires having two pieces placed.)
   The captured stones are removed but not replaced, as in go.
4. Suicides are not allowed.
   (No piece can be placed where a capture/win would be triggered against it.)
5. Superko is in effect.
   (No move can bring the board to a state that has already occurred.)

The order of operations is related to the listing above:

1. (N/A)
2. Wins made by a move are parsed, and occur.
3. Captures made by a move are parsed.
4. Suicide is checked and can reverse a non-winning move.
5. Superko is checked and can reverse a non-winning move.

The Client, and Plans
=====================

This client is built off of eidogo as a base.
I am currently modifying the rules code to match Torus.
After that, I intend to create a vector-based display system,
and add in more features,
following the footsteps of the java client a friend has made.
The hope is to have a javascript client to use for a Torus server someday.

