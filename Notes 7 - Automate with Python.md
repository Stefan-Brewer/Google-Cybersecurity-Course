# Course 7: Automate Cybersecurity Tasks with Python

# Module 1: Introduction to Python in Cybersecurity - Study Notes

## 1. Python and Cybersecurity

* **Programming:** Creating instructions for a computer to execute tasks. Languages like Python are converted to binary (0s and 1s) for the CPU. Python uses an **interpreter** to translate code line by line into runnable instructions.
* **Python's Role:** A general-purpose language used in web development, data analysis, and notably in cybersecurity for **automation**.
* **Automation:** Using technology to reduce manual effort for common, repetitive tasks (e.g., log analysis, malware analysis, access control list management, intrusion detection, compliance checks, network scanning). Python is good for automating short, simple tasks and combining separate tasks into a single workstream.
* **Why Python?**
    * **User-friendly:** Resembles human language, requires less code, easy to read. Follows standard guidelines (syntax) for consistency.
    * **Support:** Large online community and extensive built-in code libraries (modules) that can be imported.
    * **Cross-platform:** Works on different operating systems.

## 2. Python Basics & Environments

* **Script vs. Program:** A script contains the specific lines of code (like a play's script), while a program encompasses the whole design and execution (like a full theatre production).
* **Comments:** Notes in code explaining intent, ignored by the interpreter. Start with `#`.
* **`print()` Function:** Outputs specified objects (text, numbers, variable values) to the screen.
* **Syntax:** Rules determining correctly structured code in a language. For strings, this includes using quotation marks. Python 3 syntax is used in this course.
* **Environments:**
    * **Notebooks (e.g., Jupyter, Google Colab):** Online interfaces for writing, storing, running code, and documenting it. Use code cells (for code) and markdown cells (for text). Used in this course.
    * **Integrated Development Environments (IDEs):** Software applications with GUIs for writing code, offering editing help and error correction.
    * **Command Line Interface (CLI):** Text-based interface to interact with the computer, run Python programs, and edit files.

## 3. Data Types

A **data type** categorizes data items, affecting how they're handled.

* **String (`str`):** Ordered sequence of characters (letters, symbols, spaces, numbers) enclosed in single (`'`) or double (`"`) quotes. Numbers in strings cannot be used for calculations. An empty string is `""`.
* **Integer (`int`):** Whole numbers (positive, negative, or zero) without a decimal point (e.g., `-100`, `0`, `50`).
* **Float (`float`):** Numbers with a decimal point (e.g., `-2.2`, `0.0`, `3.14`). Division (`/`) results in a float. Floor division (`//`) rounds down to the nearest whole number (returns int if both inputs are int, float if either is float).
* **Boolean (`bool`):** Represents truth values: `True` or `False` (case-sensitive, no quotes). Used for logic and comparisons.
* **List (`list`):** Ordered, changeable collection of items in sequence, enclosed in square brackets `[]`. Items are separated by commas and can be of different data types. An empty list is `[]`.
* **Tuple (`tuple`):** Ordered, *unchangeable* collection of items, enclosed in parentheses `()`. Items separated by commas, can be different data types. More memory efficient than lists.
* **Dictionary (`dict`):** Unordered collection of key-value pairs, enclosed in curly braces `{}`. Keys map to values (`key: value`), pairs separated by commas. Useful for predictable data storage/retrieval.
* **Set (`set`):** Unordered collection of *unique* items, enclosed in curly braces `{}`. Items separated by commas, can be different types. No duplicate values allowed.

## 4. Variables

* **Variable:** A named container that stores data in memory. Its value can change (**reassignment**).
* **Assignment:** Creating a variable using `variable_name = value`. Python automatically assigns the data type based on the value.
* **Calling a Variable:** Using the variable name to access the stored value (e.g., `print(variable_name)`). Don't use quotes when calling.
* **Naming Conventions:**
    * Use only letters, numbers, underscores (`_`).
    * Case-sensitive (`time` != `Time`).
    * Don't use Python keywords (e.g., `if`, `True`).
    * Use underscores to separate words (`login_attempts`).
    * Make names descriptive, avoid unnecessary length, avoid similar names.
* **`type()` Function:** Returns the data type of a variable or value (e.g., `type(device_ID)`).
* **Type Error:** Occurs when trying an operation on incompatible data types (e.g., adding a string and an integer).

## 5. Conditional Statements

Used for decision-making and automation; they evaluate code against conditions.

* **Structure:**
    * **Header:** Starts with `if`, `elif`, or `else`, followed by a condition (for `if`/`elif`), and ends with a colon (`:`).
    * **Body:** Indented block of code executed if the header's condition is `True` (for `if`/`elif`) or if preceding conditions were `False` (for `else`).
* **Keywords:**
    * `if`: Starts the conditional. Executes body if its condition is `True`.
    * `elif` (else if): Checks a new condition only if the preceding `if` or `elif` conditions were `False`. Executes body if its condition is `True`. Can have multiple `elif`s.
    * `else`: Executes its body if *all* preceding `if` and `elif` conditions in the block were `False`. Optional, max one per block, must be last.
* **Comparison Operators:** Used in conditions: `>` (greater than), `<` (less than), `>=` (greater/equal), `<=` (less/equal), `==` (equal to), `!=` (not equal to).
* **Logical Operators:** Combine multiple conditions:
    * `and`: `True` only if *both* conditions are `True`.
    * `or`: `True` if *at least one* condition is `True`.
    * `not`: Reverses the truth value (`True` becomes `False`, `False` becomes `True`).

## 6. Iterative Statements (Loops)

Repeat a block of code multiple times. Also called **loops**.

* **Structure:**
    * **Loop Header:** Starts the loop (e.g., `for`, `while`), defines iteration criteria, ends with a colon (`:`).
    * **Loop Body:** Indented block of code executed repeatedly.
* **`for` Loops:** Iterate over a *sequence* (e.g., list, tuple, string, range).
    * Syntax: `for loop_variable in sequence:`
    * `loop_variable`: Temporarily holds the current item from the sequence for each iteration.
    * `in`: Keyword used to link the variable and the sequence.
    * `range()`: Generates a sequence of numbers.
        * `range(stop)`: 0 up to (not including) `stop`.
        * `range(start, stop)`: `start` up to (not including) `stop`.
        * `range(start, stop, step)`: `start` up to (not including) `stop`, incrementing by `step`.
* **`while` Loops:** Iterate as long as a condition remains `True`.
    * Syntax: `while condition:`
    * The condition is checked *before* each iteration.
    * Need to ensure the condition eventually becomes `False` inside the loop body (e.g., by incrementing a counter) to avoid an **infinite loop**. Stop infinite loops with `Ctrl+C` or `Ctrl+Z`.
* **Loop Control:**
    * `break`: Immediately exits the *entire* current loop.
    * `continue`: Skips the *rest of the current iteration* and proceeds to the next one.
* **Loop Variable:** A variable used to control loop iterations (e.g., `i` in `for i in range(5)` or the counter in a `while` loop).
