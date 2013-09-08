##Sudoku

This is a solver for a Sudoku puzzle built as class exercise at Makers Academy.

For those of you that do not know Sudoku is a puzzle that consists of a 9X9 master grid that contains 81 cells and nine 3X3 inner grids.

The aim of the puzzle is to place a number between 1-9 in each cell, so that every row, column and inner grid contains **all** the numbers from 1-9 without any duplicates.

A game would typically start with a partially completed board for you to complete.

~~~
                        -----------------
                       |  3 |  2  | 6   |
                       | 9  | 3 5 |   1 |
                       |  1 | 8 6 | 4   |
                        -----------------
                       |  8 | 1 2 | 9   |
                       |7   |     |   8 |
                       |  6 | 7 8 | 2   |
                        -----------------
                       |  2 | 6 9 | 5   |
                       |8   | 2 3 |   9 |
                       |  5 |  1  | 3   |
                        -----------------
~~~



In our program the starting board is represented as a 81 character string, where every 9 characters in the string represents a row, the zeros blank spaces and the numbers their respected cell numbers on the board.

~~~ruby
 puzzle = Sudoku::Puzzle.new '003020600900305001001806400008102900700000008006708200002609500800203009005010300'
~~~


It's then up to the program to solve the puzzle !!


~~~
                        -----------------
                        |483| 921 | 657 |
                        |967| 345 | 821 |
                        |251| 876 | 493 |
                        -----------------
                        |548| 132 | 976 |
                        |729| 564 | 138 |
                        |136| 798 | 245 |
                        -----------------
                        |372| 689 | 514 |
                        |814| 253 | 769 |
                        |695| 417 | 382 |
                        -----------------
~~~

###Note**
Currently the solver uses bruteforce to solve the puzzle but this might not work for for more difficult puzzles, as is the case in some of our experiments.