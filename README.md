# Search-Based-Problem-Solving
Search-Based Problem-Solving

Goals
 
The goals of this assignment are to understand general Graph Search, its implementation, and how it can be applied to real problems. The task domain will be controlling 2-D motions of a robot hand, as described below.  For this world you will implement five queue-modification algorithms for use with a general Graph Search procedure :
 
1.    Breadth First Search
2.    Depth First Search
3.    Best First Search (with a heuristic you define)
4.    Best First Search (with another heuristic you define)
5.    A* Search

Definitions
 
A ’problem instance’ is defined by three things, which together provide everything needed to define what the system must solve:   (1) the board dimensions, (2) the initial state, and (3) the goal state.
 
 
The Robot Hand World
 
1. There is a rectangular grid with cells that are squares whose side is of the unit length. The width and height of the grid are whole number multiples of this unit length. There is no third dimension. The cells are indexed by 0..(length - 1) and 0..(width - 1).
 
2. Every block is a unit square. No two blocks may be in the same position. The blocks are considered distinct from one another, so if a goal state involves one block and another to its left, it matters which of the two blocks is where.
 
3. There is a single robot hand which can move around the grid. The hand may be in an open state or a closed state. If and only if the hand has no block in it and it is in an open state, it may occupy the same cell as a block. In this situation, the robot hand may do a CLOSE action and pick up the block. When the robot hand does an OPEN action, it is no longer holding the block. The hand may move left, right, forward, or backward with the same cost C whether or not it is holding a block (no atomic diagonal moves of cost C). The OPEN and CLOSE actions cost C/10.  (Note that if these had no cost, uniform cost search might favor open/close loops.) Moving right is the positive y direction, moving left is the negative y direction, moving forward is the positive x direction, and moving backward is the negative x direction. (This choice of language follows the conventional 3D axis, and the code defining this RobotWorld actually accommodates three dimensions, should you want to try out a harder domain.) 
 
4. In all problem instances, the robot hand starts in the open state and in the bottom left corner of the grid, coordinate (0,0). Each problem instance has its own initial arrangement of blocks.
 
5. Each problem instance has exactly one goal state, which consists of an arrangement of blocks. The location of the robot hand is not relevant to the goal state. Again, the blocks are considered distinct so it matters which block is where.
 
6. In the world, there is no ’time’ beyond that actions are ordered. Discrete actions punctuate a change in the world. The time the agent spends thinking is not relevant to the world, although it is relevant to you testing your work!
 
  
  
