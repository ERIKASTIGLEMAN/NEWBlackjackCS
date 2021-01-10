# NEWBlackjackCS

PEDAC – BLACKJACK

P – Problem
We are going to play a single player(human) game of BlackJack against the house (computer), with the following requirements:

- 52 card deck
  o Cards have ranks 2, 3, 4, 5, 6, 7, 8, 9, 10, Jack, Queen, King, or Ace
  o Cards have suits "Club", "Diamond", "Heart", or "Spade"
  o Cards hold the following values
  Cards 2 3 4 5 6 7 8 9 10 Jack Queen King Ace
  Values 2 3 4 5 6 7 8 9 10 10 10 10 11

- House cards should be hidden from player until time to reveal hand
- Players cards should be visible to player
- Player should be given option to hit or stand depending on hand total
  o If player has < 21 – player can hit or stand
  o If player has = 21 – player wins, unless dealer ties. All ties, dealer wins
  o If player has > 21 – player BUST, and dealer wins
- When player stands or bust the dealer will reveal its hand
- Dealer should be given option to hit, depending on hand total
  o If dealer has < 17 – dealer can hit
  o If dealer has = 17 - 21 – dealer wins, unless dealer ties. All ties, dealer wins
  o If dealer has > 21 – dealer BUST, and player wins
- Player closer to 21 w/o going over WINS
- Aces should be considered equal to 11
- Winner should display after each game for either the player or the house
- A REPLAY option should be available at the end of each game with new deck of cards and hands

E – Examples

- If player is dealt 21 on first deal – player wins
- Player’s hand has 5hearts & 10Clubs – card total is 15
  o Player may STAND or HIT – HITS
  o Player dealt 5clubs – hand value is now 20
  o Player hand value is now 20 and STANDS
  o Dealer cards are revealed
  o Dealer hand totals 16 with a 10diamonds & 6hearts
  o Dealer must hit and next card revealed
  o Dealer is dealt a 2clubs – hand total is now 18
  o Dealer must stand and player wins

D – Data Structure

- We will need a deck of 52 cards as a string and parsed into int
  o Create ranks
  o Create suits
  o Merge ranks and suits into new card
  o Add new card to a deck
- Shuffle cards
- Create a class/method to add values to the cards using int
- Deal two hands
  o 1st dealer – keep cards hidden
  o 2nd player – reveal cards
- Assign the hands a value
- Value for hand will display either STAND, HIT, or WINNER

A – Algorithm

1. Create Cards
   a. List of ranks
   b. List of suits
   c. Merge these two list to create Newcards
   d. Add new cards a deck
2. Assign Cards a value
3. Create 2 hands
   a. 1 – player
   b. 1 – dealer
4. Deal cards into both hands
   a. Player cards shown
   b. Dealers cards hidden
5. Depending on card total
   a. Player will choose to stand
   i. Revealing dealer card
   b. Player will choose to hit
   i. Adding and showing new card to player’s hand
6. Player will bust if card value > 21 and BUSTED will display
7. Player will choose to HIT or STAND if card value is < 21
8. Player will win if card value = 21 and dealer does not tie, and WINNER will display
   c. Dealer will choose to HIT
   i. Adding and showing new card to dealers hand
9. If total card value is < 17
   a. Dealer will bust if card value > 21 and BUSTED will display
   d. Dealer will choose to STAND
   i. If total card value is > 17 Dealer will STAND
10. Dealer will win if card value >17 & <= 21 and card value exceeds players card value
11. dealer wins all ties
12. WINNER will display
    e. At end of game - display option to play again
    i. Shuffle deck
    ii. Deal two new hands

C – Code
