Hangman - an online word game. The player is given a secret word to guess by using the letters of the alphabet and the ability to make a limited number of mistakes.

As hints, the category to which the secret word belongs is provided, along with the number of letters in the word represented by asterisks (***). Each incorrect guess adds a part to the "hangman". The maximum number of mistakes allowed is 9.

The program consists of several modules:

**bot_viselnica**

This module contains information about the bot itself and the primary commands:
-   `/hello` - greets the player
-   `/topic` - suggests the category to which the secret word belongs
-   `/game` - displays the number of asterisks (***), corresponding to the number of letters in the secret word, and prompts the player to enter a letter
-   `/again` - restarts the game
-   `/help` - provides help

**game**

One of the main modules, consisting of three parts:

-   `hidden_word_topic` - randomly selects the category to which the secret word belongs
-   `word_choice` - randomly chooses a word from the suggested category and replaces the letters of the word with asterisks (***)
-   `game` - replaces an asterisk (*) with a letter if the player's input is correct. In case of an incorrect guess, it displays an image adding a hangman part. After losing, it prompts to play again.

**guess_word**

Creates a string for displaying intermediate results after guessing letters:

***, **g, *og, dog
