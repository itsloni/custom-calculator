# Custom Recursive Command-Line Calculator

A pure-Python arithmetic parsing engine built entirely from scratch without using dangerous shortcuts like `eval()` or standard mathematical libraries. 

This project explores lower-level string parsing, list mutation algorithms, and recursion.

##  Features

- **Nested Parentheses Handling:** Evaluates complex nested expressions using an inside-out lookback algorithm.
- **Strict Operator Priority (PEMDAS/BODMAS):** Correctly prioritizes brackets, custom `of` operations, multiplication, division, and left-to-right evaluation for addition and subtraction.
- **Dynamic List Mutation:** Tokenizes user inputs via spaces, processes operations, and handles array shrinking cleanly without off-by-one errors.

##  Core Engineering Challenges Overcome

1. **The Exclusive Slicing Rule:** Navigated Python's default behavior where a stop slice index `[start:stop]` excludes the boundary element, safely expanding slices to avoid leaving lingering array values.
2. **Inside-Out Bracket Resolution:** Solved the classic matching parenthesis problem by scanning left-to-right for the first closing bracket `)`, then running a lookback pointer loop to capture its exact matching open bracket `(`. This handles nested equations without breaking side-by-side bracket expressions.
3. **Data Type Preservation:** Prevented list parsing errors during recursive function callbacks by tracking list mutation and converting mathematical floats securely back to string objects before re-joining arrays.

##  How To Run

1. Clone this repository.
2. Open your terminal and run:
   ```bash
   python "CALCULATOR 2.0 practice.py"
   ```
3. Enter equations separating every number and operator with a space:
   * Example: `2 * ( 3 + 4 ) of ( 10 - 8 )`
