Start by importing and defining all my files

I used a large dictionary to create a word bank with three different categories and three different difficulties
I defined how many lives and hints the player gets depending on their chosen difficulty

Then I saved and made sure the word bank existed along with saving each highscore from each player

I set up a class that sets up a non-resizable Tk window titled “Hangman”. Which loads data and initializes the game's logical state (word bank, highscores, selected category/difficulty, current secret word variables, guessed letters, lives).
It also defines how many drawing stages exist.

I implemented the game’s end-of-round logic, a highscore viewer, and the base drawing for the hangman canvas. _on_win computes a numeric score from remaining lives and the unique letters in the secret word, prompts the player for a name, saves the highscore, shows a win message, and resets the round. 
Then _on_loss shows a losing message and resets the secret word.

I managed drawing the hangman figure on the Tkinter canvas. The _draw_base() function draws the base/poles, while _draw_hangman() determines how many body parts to draw based on the number of wrong guesses. It keeps a list of body-part-drawing functions in order and calls each one depending on the player’s mistakes, after clearing any previous drawings.
