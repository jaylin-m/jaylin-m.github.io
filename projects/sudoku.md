---
layout: project
type: project
image: img/Sudoku.jpg
title: "Sudoku"
date: 2023
published: true
labels:
  - Java
  - Eclipse IDE
summary: "I implemented a Sudoku solver application capable of finding solutions to Sudoku puzzles, written in Java."
---

  <img width="300px" class="img-fluid" src="../img/Sudoku1.png"> <img width="300px" class="img-fluid" src="../img/Sudoku2.png">
  <img width="300px" class="img-fluid" src="../img/Sudoku3.png">

This Sudoku solver application is a solo project I completed in my Introduction to Computer Science II course (ICS 211) at the University of Hawaiʻi at Mānoa. The goal for each method was outlined, and I worked on implementing the code for each method on my own. I developed the application in Java on the Eclipse IDE. The application checks if the puzzle obeys all Sudoku rules and validates the puzzle's correctness. It systematically fills in blank cells and ensure compliance with Sudoku constraints. I also created a user-friendly output format for displaying the Sudoku puzzles and solutions to enhance readability.

Through this project, I learned how to problem-solve when implementing recursive algorithms and nested for loops to work with multidimensional arrays. I learned how to implement the toString method in Java to display the Sudoku grid in a readable format. I also learned how to test the application's solver functionality using different test Sudoku boards and automate the testing process using the SudokuTest class, which checks if the program's solution matches a given expected solution.

Here is the code for the fillSudoku method, which finds an assignment of values to the Sudoku cells that makes the puzzle valid:

```cpp
public static boolean fillSudoku (int [] [] sudoku)
  {
    boolean allFilled = true;
    int row = -1;
    int col = -1;
    for (int i = 0; i < 9; i++) {
    	for (int j = 0; j < 9; j++) {
    		if (sudoku[i][j] == 0) {
    			row = i;
    			col = j;
    			allFilled = false;
    			break;
    		}
    	}
    	if (!allFilled) {
			break;
		}
    }
    
    if (allFilled == true) return true;
    
    for (int num = 1; num <= 9; num++) {
    	sudoku[row][col] = num;
    	if (checkSudoku(sudoku, false)) {
    		if (fillSudoku(sudoku)) {
    			return true;
    		}
    	}
    }
    sudoku[row][col] = 0;
    return false;
  }
```

To see the code for the Sudoku application, click <a href="https://github.com/jaylin-m/ICS-211/blob/main/Sudoku.java">here</a>. To see the test code for the Sudoku application, click <a href="https://github.com/jaylin-m/ICS-211/blob/main/SudokuTest.java">here</a>.
