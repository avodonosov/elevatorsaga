My Changes
==========
This is my fork of the https://github.com/magwo/elevatorsaga

You can play it here:
<https://avodonosov.github.io/elevatorsaga/>

It contains some convenience enhancements:
- Possibility to replay a run, and so study how your solution failed.

  Every time a game is started, new seed is generated and printed to
  console, together with instruction how to replay game with this seed:

  ```
  New game seed: "0.8738863726251744"
  To replay: window.GameSeed = "0.8738863726251744";
  To replay: https://avodonosov.github.io/elevatorsaga/?seed=0.8738863726251744#challenge=4

  ```

  As you see, there are two ways: use URL with the ?seed= parameter,
  and setting global variable window.GameSeed.

  If any of these methods is used. the console contains instruction
  how to stop replaying:

  ```
  Game seed from window.GameSeed="0.8738863726251744";
  To stop replaying: window.GameSeed = null;
  ```
  or
  ```
  Game seed from the URL parameter ?seed= 0.8738863726251744
  To stop replaying omit the seed parameter: https://avodonosov.github.io/elevatorsaga/#challenge=4
  ```

  Note, in rare cases, the replay behaves differently than
  the original run. If that happened, just replay again.

  This happens because, even after we make the random number
  generator deterministic by reusing a seed, there is some
  other source of non-determinism in the game implementation.
  Probably animations sometimes vary in duration and thus
  somehow influence the behavior - just a guess.

  (This feature addresses issue magwo#34.)

- Highlight the longest waiting person with red - this helps to
  understand why max waiting time challenges fail.

  (This feature addresses issue magwo#77.)

- More gray color for leaving users, to make them really look different.

--------------------------------

Original README


Elevator Saga
===================
The elevator programming game

[Play it now!](http://play.elevatorsaga.com/)

Or [Run the unit tests](http://play.elevatorsaga.com/test/)

For developers/contributors: This project is not actively maintained. The repo is used to serve github pages so I would like to keep it as is. Feel free to fork and host your own versions of Elevator Saga! But I would like to keep the domain name with the original version of the game.

![Image of Elevator Saga in browser](https://raw.githubusercontent.com/magwo/elevatorsaga/master/images/screenshot.png)
