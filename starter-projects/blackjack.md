# BlackJack - Starter Project

## Specification

You may choose to do this whatever way you are confident in doing

1. Should be able to play at least 1 round of blackjack (rules defined here)
   - Deck consists of four suits: Hearts (H), Diamonds (D), Clubs (C), Spades (S)
   - All numbered cards represent their value. Jack, Queen & King have the value 10, Ace has 11
2. One round of blackjack should consist of (in order)
   1. Player (user) is given 2 cards to start, with the card values shown. The deal
   2. Player turn:
    - If the player has 21 for 2 cards then they automatically win with "Blackjack".
   3. If the player has under 21 then they can be repeatedly asked to "stick" or twist while the total hand value is less than 21.
    - stick: the current value is 
   4. If the player goes over 21 then the dealer wins.

Round over messages:

- If player has blackjack: "Blackjack! You win!"
- If the player busts: "Bust! Bad Luck!"
- If the dealer busts: "Dealer Bust! You win!"
- If the player ends the round with a higher value than the dealer: "High Value! You win!"
- If the player ends the round with the same score as the dealer: "Draw!"
- If the player ends the round with a lower score than the dealer: "Dealer wins! Bad Luck!"

### Example Console Game
This is an example of how this might work in a command line program version of this exercise.
```
Welcome to Blackjack!
Round 1
Your cards: 3D, 7C (10)
Dealer cards: 9J, **
Stick (s) or Twist (t)? t
Your cards: 3D, 7C, KH (20)
Stick (s) or Twist (t)? s
Dealer's Turn
Dealer cards: 9J, 2H (11)
Dealer Draws... 8H
Dealer cards: 9J, 2H, 8H (19)
Dealer Sticks.
HIGH VALUE! YOU WIN! 🎉

Play Again?
```
