Snap!
============

Description
----
##### Based on the lessons in Chapter 14 from The Well Grounded Rubyist
Implementing a networked and threaded two-player version of the card game 'snap!'.

Rules/Instructions
---
Two players connect to the server, enter their names, and start a new game. A deck of cards gets shuffled and distributed between the two players and each player takes it in turn to draw out a card one by one.  If, at any moment, two consecutively drawn cards match (example: two kings, two sixes, two aces, etc..), the first player to shout ```snap!``` claims all drawn cards and adds it to their own hand. The player who ends up with the entire deck of cards in his hand is crowned the winner.

How to run it
----

First tab:

```sh
git clone git@github.com:sroop/threaded_snap.git
cd threaded_snap
ruby lib/snapserver.rb
```

Second tab (connect at player 1):

```sh
telnet localhost 3939
```

Third tab (connect as player 2):

```sh
telnet localhost 3939
```

Keywords
----

```shuffle``` Starts a new game and deals out a newly shuffled deck of cards between the two players
```draw``` Draws a card from the player's hand
```snap!``` First player to shout this wins all drawn cards and adds it to their hand
