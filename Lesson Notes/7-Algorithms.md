# Hangman using Node.js

First, we need to define the method that we will use to solve the problem:

```
WORD = "CAT"
GUESSES = []

STATE = UPDATE_STATE(WORD, GUESSES)

WHILE (STATE == NUETRAL):
    GUESS   =  ASK_GUESS()
    GUESSES += GUESS
    STATE   =  UPDATE_STATE(WORD, GUESSES)
```

Additionally, the method used to update the visual state needs the valid states to be defined, we know that the game state must be one of the following when displayed

```
VALUD GAME_STATES:
    NUETRAL
    WIN
    LOSE


VALID GAME_DISPLAY:
    0. ________     1. ________     2. ________     3. ________
       |      |        |      |        |      |        |      |
       |               |      O        |      O        |      O
       |               |               |      |        |     /|
       |               |               |               |
    ___|___         ___|___         ___|___         ___|___

    4. ________     5. ________     6. ________
       |      |        |      |        |      |
       |      O        |      O        |      O
       |     /|\       |     /|\       |     /|\
       |               |     /         |     / \
    ___|___         ___|___         ___|___
```

Next we can define a function to update the display as well as return the new game state

```
FUNCTION UPDATES_STATE(WORD, GUESSES):
    UNIQUE_LETTERS         = GET_UNIQUE_LETTERS(WORD)
    UNIQUE_CORRECT_GUESSES = GET_UNIQUE_CORRECT(WORD, GUESSES)
    INCORRECT_GUESSES      = GET_INCORRECT(WORD, GUESSES)

    NEW_DISPLAY            = GAME_DISPLAY[INCORRECT.LENGTH]
    SHOW_DISPLAY(NEW_DISPLAY)

    NEW_STATE              = GET_NEW_STATE(UNIQUE_LETTERS, UNIQUE_CORRECT_GUESSES, INCORRECT_GUESSES)

    SHOW_LETTERS(WORD, UNIQUE_CORRECT_GUESSES, NEW_STATE)

    RETURN NEW_STATE
```

As well as functions to help us get the new state and print out the letters as needed

```
FUNCTION GET_NEW_STATE(UNIQUE_LETTERS, UNIQUE_CORRECT_GUESSES, INCORRECT_GUESES):
    IF(INCORRECT_GUESSES.LENGTH >= 6):
        RETURN GAME_STATE.LOSE
    ELSE IF(UNIQUE_LETTERS == UNIQUE_CORRECT_GUESSES):
        RETURN GAME_STATE.WIN
    ELSE:
        RETURN GAME_STATE.NEUTRAL

FUNCTION SHOW_LETTERS(WORD, UNIQUE_CORRECT_GUESSES, NEW_STATE)
    IF (NEW_STATE == LOSE):
        SHOW_ALL_LETTERS(WORD, UNIQUE_CORRECT_GUESSES)
    ELSE:
        SHOW_CURRENT_LETTERS(WORD, UNIQUE_CORRECT_GUESSES)
```
