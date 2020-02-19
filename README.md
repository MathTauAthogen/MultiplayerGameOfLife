# MultiplayerGameOfLife
Wanted to do this for a while, it's basically my spin on a game to replace Total War because I was sad when that came down.

#The RUUUUUUUUULES are simple!
We begin with normal Game of Life rules and make some modifications.

Each realm is given a color. We use red and blue here. There is one additional realm that is grey, which is civilian.

The goal of the game is to produce a setup that will end in the highest chain at the end.

## Starting position

Each player begins by placing up to 15 soldiers within a 13 tile radius of their corner, with one of two hues (i.e. light and dark).
Civilians start at random points in the grid.

## Play

Each turn, any tile with 2 adjacent soldiers of the same color but of different hues will produce a soldier, randomly one hue or the other. Any soldier that has no neighboring soldier of the opposite hue, however, will die of lonliness. Additionally, any soldier without a direct link to their corner will also die of hunger.

Colors cannot interbreed, except that civilians will breed with any color, but not two different colors at the same time.

Any two adjacent soldiers of different colors follow the following rules:

- Each color in a conflict has a "total strength". This is the sum of the strengths of each soldier of that color adjacent to the soldiers in conflict, as well as the soldiers themselves.
- Each light soldier has strength 7/4, and each dark soldier has strength 2.
- Whichever total strength is greater causes the other soldier to lose a hue. This means that a dark soldier becomes light and a light soldier dies.
- In case of ties both lose a hue.
- Battles are resolved before breeding.
- Soldiers can be parts of multiple conflicts. In this case they are resolved simultaneously.

## Win condition

The winner is the person first with the most living soldiers, then with the largest total strength, then the person with the longest chain from the center. If there is still a tie, the furthest distance from the corner is taken and finally if it still isn't resolved a die is rolled.

## Ranking points

To be implemented
