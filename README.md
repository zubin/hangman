# Hangman

Implement [Hangman] as a programming exercise!

## Synopsis

The game is to be played in a shell, like this:

```
$ bin/hangman

===================
Welcome to Hangman!
===================

Please choose an option:

[1] How to play
[2] Start game
[3] Exit

Enter your choice: 1

-----------
How to play
-----------

The goal of the game is to correctly guess a word by suggesting letters. The
word to guess is represented by a row of dashes which represent each letter of
the word.

You need to suggest letters which occur in the word. It gets written into all
its correct positions. If the suggested letter does not occur in the word, one
element of a hanged man stick figure is drawn as a tally mark. You must guess
each letter to make up the whole word before the hangman is fully drawn!

Please choose an option:

[1] How to play
[2] Start game
[3] Exit

Enter your choice: 2

----------
Start game
----------
    ___________
    |         |
    |
    |
    |
    |
    |

Word:   _______  <-- in this example, the word is "hangman"
Misses:          <-- wrong letters are listed here (lowercase, comma-separated)
Guess: A         <-- player suggests a letter here

    ___________
    |         |
    |
    |
    |
    |
    |

Word:   _a___a_
Misses:
Guess: B

    ___________
    |         |
    |         0
    |
    |
    |
    |

Word:   _a___a_
Misses: b
Guess:  C

    ___________
    |         |
    |         0
    |         |
    |
    |
    |

Word:   _a___a_
Misses: b, c
Guess:  D

    ___________
    |         |
    |         0
    |        /|
    |
    |
    |

Word:   _a___a_
Misses: b, c, d
Guess:  E

    ___________
    |         |
    |         0
    |        /|\
    |
    |
    |

Word:   _a___a_
Misses: b, c, d, e
Guess:  F

    ___________
    |         |
    |         0
    |        /|\
    |        /
    |
    |

Word:   _a___a_
Misses: b, c, d, e, f
Guess:  G

    ___________
    |         |
    |         0
    |        /|\
    |        /
    |
    |

Word:   _a_g_a_
Misses: b, c, d, e, f
Guess:  H

    ___________
    |         |
    |         0
    |        /|\
    |        /
    |
    |

Word:   ha_g_a_
Misses: b, c, d, e, f
Guess:  N

    ___________
    |         |
    |         0
    |        /|\
    |        /
    |
    |

----------------------------------------
Scenario 1: Player wins

Word:   hang_an
Misses: b, c, d, e, f
Guess:  M

    ___________
    |         |
    |         0
    |        /|\
    |        /
    |
    |

Word:   hangman
Misses: b, c, d, e, f

--------
You win!
--------

Please choose an option:

[1] How to play
[2] Start game
[3] Exit

Enter your choice: 3
Bye!

$

----------------------------------------
Scenario 2: Player loses

Word:   hang_an
Misses: b, c, d, e, f
Guess:  T

    ___________
    |         |
    |         0
    |        /|\
    |        / \
    |
    |

Word:   hang_an
Misses: b, c, d, e, f, t

---------
You lose!
---------

The correct word was: hangman

Please choose an option:

[1] How to play
[2] Start game
[3] Exit

Enter your choice: 3

Bye!

$
```

## Instructions

1. Create a subdirectory for your implementation in `implementations` (eg `implementations/java`).
1. Write your implementation to comply with the [Synopsis](#synopsis) above (BDD FTW!).
1. Ensure that `bin/hangman` invokes your implementation.

[Hangman]: https://en.wikipedia.org/wiki/Hangman_(game)
