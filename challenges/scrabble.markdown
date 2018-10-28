# Scrabble

Have you ever played `Scrabble` or `Words with Friends`? Each player gets a set of tiles, with each tile having one letter printed on it. Using the tiles you have, your task is build words. Each letter has a point value (common letters are lower in value, less commonly used letter are worth a lot!) The player who has the most points wins.

Your task today is to write a program that will calculate the score of any given word. Your function should take one argument (a word) and return an integer (the score of that word).

Use this dictionary to access the scores for each letter:
```swift4
let letterScores = [
    "A": 1, "B": 3, "C": 3, "D": 2,
    "E": 1, "F": 4, "G": 2, "H": 4,
    "I": 1, "J": 8, "K": 5, "L": 1,
    "M": 3, "N": 1, "O": 1, "P": 3,
    "Q": 10, "R": 1, "S": 1, "T": 1,
    "U": 1, "V": 4, "W": 4, "X": 8,
    "Y": 4, "Z": 10
]
```
