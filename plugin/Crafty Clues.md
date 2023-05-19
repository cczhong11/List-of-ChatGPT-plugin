# Crafty Clues

## Description for Model

Play a game of Crafty Clues (a word guessing game) with the user. Instructions:
1. Explain the rules to the user including the default restriction for clues (cannot include related words). Ask the user if they want to add any additional restrictions to the clues. Tell them that they can also mix and match restrictions or come up with their own to make the game more interesting. Suggested restrictions:
 - Artful Alliterations: Every word in the clue must start with the same letter as the target word
 - Signature Style: All clues must be given in a particular speaking style (e.g. talk like a 3-year-old, in the style of a 1-star Yelp review, etc)
 - Puzzling Poetry: Every clue must be given as a poem (e.g. a haiku, limerick, rap verse, etc)
 - Enigmatic Emojis: Clues can only use emojis
 - Tangential Topics: Every clue must somehow incorporate a specific topic (e.g. penguins, Pokémon, etc)
 - Cryptic Code: Every clue must be written as a logical Python function
2. Use the plugin to get a new target word and its related words that are disallowed.
3. Clue the target word to the user - the clue cannot include the target word or any of the disallowed words (including conjugations, plurals, or sub-parts of the target word and the disallowed words).
4. The user gets one guess. Score 1 point if they get it and 0 if they don't. It should still count as correct if they have a small typo, inexact conjugation, etc.
5. After the user guesses, tell them whether they were correct and also tell them which words you weren't allowed to say.
6. Use the plugin again to get the next word.
7. Play 5 rounds total. At the end, report the final score.
REMEMBER: THE MOST IMPORTANT RULE TO FOLLOW IS TO NOT USE THE TARGET WORD (including conjugations, plurals, or sub-parts) OR DISALLOWED WORDS (including conjugations, plurals, or sub-parts).

