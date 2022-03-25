# Cellular Automata

Cellular automata is used in different branches of science to model complexity for
example in organisms. An example of 2 dimensional cellular automata is a 2d grid of cells with each
cell having one of two states on or off, black or white with each cell having limited local knowledge.
In a series of cycles, each cell decides its next state based on the current states of its surrounding cells
(from Matt Pearson, Generative art: a practical guide using processing, Manning publications, 2011).

- Implement the Game of life CA using the following rules
    * If a live cell has two or three live neighbours, it continues to live. Otherwise it dies either of lonliness or overcrowding.
    * If a dead cell has exactly three live neighbours, a miracle occurs; it comes back to life.

- Modify the CA in (a) using a neighbouhood of radius 2.

- The stepping stone cellular automata has the following rule: "Choose a number between 0 and 1; this will be the update probability for all cells. For each cell in the array, generate a random number between 0 and 1 at every time step. If the random number generated for the given cell is higher than the update probability, the color of the cell changes to that of one of its neighbours selected uniformly at random. (Neighbour is defined as the four orthogonally adjacent cells: north, east, south, west)."
    * What is the evolutionary behaviour of this CA?
    * What happens when we begin with a grid of random colors?
    * What if we extend the definition of neighbour to include the north-east, north-west, south-east, south-west?
    * Now take a picture as the initial grid and discuss what happens in time.

- Another CA type is Vichniac Vote. In this CA evolution, each cell is susceptible to peer pressure. It looks to its neighbours to observe the current state. If it's state is in the majority, it remains unchanged. It it is in the minority, it changes. The cell uses its own state as a tie breaker.

- Brian's brain is a three-state cellular automata. The states mimic the behaviour of brain neurons. The states are off, fire, rest. The rules are
    * If the state is firing, the next state is resting.
    * If the state is resting, the next state is off.
    * If the state is off and exactly two states are firing, the state becomes firing.

- Waves (averaging) is an example of CA with continuous behaviour. The state can vary across a range of values. The rules are as follows:
    * If the average of the neighbouring states is 255, the state becomes 0
    * If the average of the neighbouring states is zero, the state becomes 255.
    * Otherwise,
        new state = current state + neighbourhood average 􀀀 previous state value
    * If the new state goes over 255, clip to 255. If the new state goes under 0, clip to 0.