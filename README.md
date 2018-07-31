# 10k_statistical_inferences
First project on GitHub - analyzing games of chance.

A while back my mom taught me a fun dice game called 10,000 (10k). The rules are laid out clearly here. https://www.wikihow.com/Play-10000
I will add that this is considered a 'folk' game with a lot of variations and house rules. I have coded this simulate our house rules.


# Rationale
From playing a few games with my mom, it wasn't clear to me what the optimal strategy was, but because there's a cost tied to continued rolling, there's likely an optimal threshold to lock in your winnings. In my experience, I fell prey to the 'hot hand' fallacy, where I figured the good rolls would keep coming. I dominated a few games but overall lost more frequently than I won. My mom, based on observing many games, thinks that 350 is a safe threshold once you're on the board. 

So let's test it! 

Enter statistical inference. I've been taking courses on DataCamp recently and learned some neat strategies for simulating and analyzing data, visualizing those results and drawing conclusions from them. And I'm going to apply them here. One as good practice in coding up games and logic, and 2 for flexing my stats and plotting skills.


# The Rules
In a game of 10000, players roll 6 dice. They score based on a combination of 1s, 5s, or groups of at least three of a kind. If a player scores, they can choose to keep their score or roll the non-scoring die to try to improve their score. However, if at any point a player rolls a non-scoring combination, their turn is over and they lose all of the points scored during the turn. The game continues until a player rolls 10,000 or more points. 

Roll six dice. If the roll has no scoring combinations, 1's or 5's, the player's turn ends. 

If the roll has scoring dice, the player may choose to roll all six again or keep any of his/her scoring dice and roll the others to create lucrative scoring combinations. 

A player MUST roll an aggregate score of 1000 points in one series of rolls to begin recording his or her score. 

Check to see if any rolled dice create winning combinations. Various combinations of numbers score points in 10,000. 

Possible scoring combinations:
Any die that shows '1' is worth 100 points
Any die that shows '5' is worth 50 points
A Three-of-a-Kind is worth a hundred times the number on the dice, with the exception of three '1's, which is worth 1000 points.
Any additional matching numbers past three of a kind double the point worth (i.e. 4+4+4=400 while 4+4+4+4=800).
Three pairs is worth 1000 points.
A straight (1+2+3+4+5+6) is worth 1000 points.
A six-of-a-kind of 1's = 10000 points, instant win

"Lock" any dice you want, provided they in a scoring combination. After your first six-dice roll, if you wish, you can roll smaller numbers of dice to continue scoring points. When you decide to stop rolling, record the points you've made during your turn on a score table.

Note: Any dice set aside cannot be used to make a combination with any rolled dice, i.e., setting aside two '5's and then rolling another '5' only gains you 50 points, not 500.

Rolling a non-scoring combination causes you to lose all points gained in your turn ('BUST'). If, at any point during your turn (including your first roll), a roll doesn't contain any scoring dice, your turn ends and you make no points. This is what makes continued rolling risky - the possibility of making more points must be weighed with the risk of losing everything you've earned so far during your turn.

The game ends when one player reaches 10000 points.


