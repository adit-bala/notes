# Search Problem
    - state space: list of possible ways for world to be configured
    - successor function: how to get to future states from current state
    - start state and goal test: goal test tells whether we are done based on state
**Solution**: sequence of actions that transforms start to goal state

## Search State

**Definition**: keeps only details needed for planning

Pathing
    - location `(x,y)` 
    - Actions: NSEW 
    - Successor () -> updates location only
    - Goal test () -> is (x,y) == END

## State Space Sizes?
World State:
    - Agent Positions: 120
    - Food count: 30
    - Ghost positions: 12
    - Agent facing: NSEW

World States (How Many)?

120 (any starting position)
2^30 (Food Count)
12^2 (Ghost positions)
4 (# of ghosts)

States for pathing (How Many)?

120

States for eat-all-dots?
120
2^30

# Safe Passage

**Problem**: eat all dots while keeping ghosts perma scared
**State specifications**:
    - Scared timer (how long ghosts are scared)
    - food booleans (whether we have eaten a food
    - Pacman location 
    - Ghost locations

# State Space Graphs
**Definition**: A mathematical representation of a search problem
    - Nodes (abstracted world configurations)
    - Arrows represent successors (action results)
    - Goal test, set of goal nodes (maybe only one)

Each state occurs only once!

Can rarely build this full graph in memory

[Add state space graph]

# Search Trees
    - A "what if" tree of plans and their outcomes
    - The start state is the root node
    - Children correspond to successors
    - Nodes show states, but correspond to PLANS that achieve those states
    - Plan: is how we get to state
    - Lots of repeated structure

    s 
        -> a
            -> b
                -> a
                -> g
            -> g
        -> b
            -> a
            -> g

**Goal**: Build tree and stop once reached solution

#### Search Tree Algorithm
    - Expand out potential plans (tree nodes)
    - Maintain a **fringe/frontier** of partial plans under considerations
        - plans in search tree to expand 
    - Try to expand as few tree nodes as possible

[insert algorithm]

##### Tree information
- `b` is branching factor
   - 1st layer: 1 node
   - 2nd layer: b nodes
   - 4th layer: b^2 nodes
- `m` is max depth

##### DFS
    - Strategy: expand a deepest node first
    - Fringe: LIFO stack
    - Properties
        - solutions at various depths
        - Number of nodes in tree
            - `1 + b + ... + b^m = O(b^m)`
        - Complete?
            - not complete if cycle exists
        - Optimal?
            - No, finds "leftmost" solution
        - Time Complexity
            - worst -> bottom right
            - O(b^m)
        - Space Complexity
            - How much space does the fringe take?
                - leaving `b` nodes at every `m` layer -> `O(bm)`

###### BFS
    - Strategy: expand a shallowest nodes first
    - Properties:
        - Time: O(b^s)
        - Space: Has roughly the last tier, `O(b^s)`
        - Complete?
            - solution exists if `s` is finite
        - Optimal?
            - only if costs are all 1

### DFS vs BFS
    - BFS > DFS
        - when solutions are shallow
    - DFS < BFS
        - when solutions are all deep
