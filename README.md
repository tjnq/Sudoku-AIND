# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: Constraint propogation techniques usually coincide with searching in order to solve a problem, or make it simpler to solve. The naked twins problem is 
   solved by constraining each unit in the Sudoku, and searching through the boxes of that unit in order to find pairs of boxes that contain the same two 
   values, hence the name 'naked twins'. The values of these two boxes are then eliminated from each of the other boxes that are within the same unit. This
   is done because no other boxes can possibly contain any of the two values within the naked twins, because the solution to the naked twins can only be 
   one value, or the other. I have implemented the naked_twins() method in the reduce_puzzle() method in order to, perhaps, solve the sudoku faster, or at
   least make the Sudoku simpler to solve. This is also a constraint propogation technique in order to solve the entire Sudoku.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: The diagonal Sudoku problem takes the constraints of the main diagonals into consideration, so that the numbers 1-9 also appear in each diagonal only 
   once. The boxes for each diagonal were grouped into 2 units, and these units were then added to the list of units, unitlist. This was all that needed 
   to be done in order to solve the diagonal problem. The eliminate(), only_choice(), and naked_twins() methods would run the same way as they would when
   solving a normal Sudoku. Since the diagonal units were added into unitlist, these methods still run through unitlist, units, and peers the same way.
   The addition of the diagonal units is what adds a constraint on the Sudoku itself when finding a solution. 

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.