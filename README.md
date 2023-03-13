# Taxi Reinforcement Learning

    ### Map: D -> destination, R -> origin
        +---+
        |D: |
        | :R|
        +---+

        +---+
        |0:1|
        |2:3|
        +---+

    ### taxi:
        #   -> taxi
        #<$ -> passenger in (taxi)
        #>$ -> passenger out (of taxi)

    ### Actions
        There are 6 discrete deterministic actions:
        - 0: move south
        - 1: move north
        - 2: move east
        - 3: move west
        - 4: pickup passenger
        - 5: drop off passenger

     ### Observations
        There are 12 discrete states since there are 4 taxi positions, 3 possible
        locations of the passenger (including the case when the passenger is in the
        taxi), and 1 destination locations.

    ### Rewards
        - -1 per step unless other reward is triggered.
        - -10  executing "pickup" and "drop-off" actions illegally.
        - +200 delivering passenger.
        - +10  executing "pickup" legally.

    ### ternimate
        True when the passenger is in destination and not in taxi


<img src="https://github.com/arashebra/Taxi-Reinforcement-Learning/blob/main/AllStates.jpg">