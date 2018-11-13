# Problem

> On an 8x8 chess board, determine the minimum number of turns it would take for a chess piece at a given position to move to a goal position. If the goal position is unreachable, return a value representing that fact.

Your solution should work for the following pieces:
- King (can move 1 square in any direction per turn)
- Knight (can move in a 2x1 or 1x2 "L" pattern per turn)
- Bishop (can move any number of squares diagonally per turn)

# thanks for the feedback!
You're completely right, the "graph" over which the breadth-first-search operates is defined (locally) by the `move_generator`, which produces the neighbors of each node. If that part is wrong, then the algorithm is not valid!

In the original implementation, `move_generator` generates spurious moves, thus making the graph incorrect. I fixed it by having it consider only valid moves when it's generating.

Let me know (in the issues?) if there are things that are still questionable! Thanks!

# And it's open-ended!
What I chose to focus on:
- ease of understandability
- ease of extensibility
- simplicity
