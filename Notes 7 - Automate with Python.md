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

# Module 2: Write Effective Python Code - Study Notes

## Introduction to Functions

* **Definition:** A function is a reusable block of code designed to perform a specific task. Think of it like a dishwasher automating the repetitive task of washing dishes.
* **Purpose:** Functions improve efficiency and code organization by allowing you to write a set of instructions once and call it multiple times from different parts of your program. This makes code easier to manage and update; changes made within the function are reflected everywhere it's used.
* **Types:**
    * **Built-in Functions:** Pre-defined functions available in Python by default (e.g., `print()`, `type()`).
    * **User-defined Functions:** Functions created by the programmer for specific needs.

## Creating and Using User-Defined Functions

* **Defining:** Use the `def` keyword, followed by the function name, parentheses `()`, and a colon `:`. The code block that the function will execute (its body) must be indented below the definition line.
    ```python
    # Define the function
    def greet_user():
        print("Welcome!")
    ```
* **Calling:** To execute the function, simply write its name followed by parentheses.
    ```python
    # Call the function
    greet_user()
    ```
* **Parameters and Arguments:**
    * **Parameters:** Variables listed inside the parentheses in the function definition. They act as placeholders for data the function needs to receive.
    * **Arguments:** The actual data values passed into the function when it is called. These values are assigned to the corresponding parameters.
    ```python
    # Function with a parameter
    def personalized_greeting(name):
        print("Hello, " + name + "!")

    # Calling the function with an argument
    personalized_greeting("Alex") # "Alex" is the argument

    # Function with multiple parameters
    def add_numbers(x, y):
        print(x + y)

    # Calling with multiple arguments
    add_numbers(5, 3) # 5 and 3 are arguments
    ```
* **Return Statements:** Use the `return` keyword inside a function to send a value back to the part of the program that called the function. This allows the function's result to be stored in a variable or used in further computations. Python exits the function as soon as it hits a `return` statement.
    ```python
    def calculate_area(length, width):
        area = length * width
        return area # Sends the calculated area back

    # Store the returned value
    room_area = calculate_area(10, 5)
    print(room_area) # Output: 50
    ```

## Variable Scope

* **Local Variables:** Variables defined *inside* a function (including parameters). They only exist while the function is executing and cannot be accessed from outside the function.
* **Global Variables:** Variables defined *outside* any function. They are accessible from anywhere in the program, including inside functions.
* **Best Practice:** While functions *can* access global variables, it's generally better to pass data into functions using parameters and get results back using `return`. Avoid using the same names for global and local variables to prevent confusion; if a variable is assigned *within* a function, Python treats it as a new local variable, even if a global variable with the same name exists.

## Built-in Functions Exploration

* **Review:** `print()` outputs objects to the screen, `type()` returns the data type of an object.
* **Combining Functions:** You can use the output of one function as the input (argument) for another. The inner function is executed first.
    ```python
    print(type(123)) # type() executes first, its output (e.g., <class 'int'>) is passed to print()
    ```
* **Key Functions:**
    * `max(iterable)` / `max(arg1, arg2, ...)`: Returns the largest item from an iterable (like a list) or the largest of several arguments.
    * `min(iterable)` / `min(arg1, arg2, ...)`: Returns the smallest item.
    * `sorted(iterable)`: Returns a *new* list containing all items from the iterable in ascending order (numerically or alphabetically). The original iterable remains unchanged. Requires items in the iterable to be of comparable data types (e.g., all numbers or all strings).
    ```python
    numbers = [5, 1, 9, 3]
    print(max(numbers))      # Output: 9
    print(min(numbers))      # Output: 1
    print(sorted(numbers))   # Output: [1, 3, 5, 9]
    print(numbers)           # Output: [5, 1, 9, 3] (original list is unchanged)
    ```

## Modules and Libraries

* **Module:** A Python file (`.py`) containing Python definitions and statements (functions, variables, classes). Modules allow you to logically organize your Python code.
* **Library:** A collection of related modules.
* **Python Standard Library:** An extensive library of modules included with Python installations (e.g., `statistics`, `re`, `csv`, `os`, `datetime`). Provides ready-to-use code for common tasks.
* **External Libraries:** Collections of modules developed by third parties (e.g., `NumPy`, `Beautiful Soup`). They often need to be installed before use (e.g., using `pip install library_name`).
* **Importing:** To use code from a module, you must import it:
    * `import module_name`: Imports the entire module. Access its contents using `module_name.function_name()`.
    * `from module_name import function_name`: Imports only a specific function (or variable/class). Access it directly using `function_name()`.
    * `from module_name import func1, func2`: Imports multiple specific items.
    ```python
    # Import the whole 'statistics' module
    import statistics
    data = [1, 2, 2, 3, 5]
    mean_value = statistics.mean(data) # Use module name prefix

    # Import only the 'median' function from 'statistics'
    from statistics import median
    median_value = median(data) # Use function name directly
    ```

## Code Readability and Style (PEP 8)

* **Importance:** Code is read far more often than it is written. Readable code is easier to understand, debug, and maintain, especially when working in teams.
* **PEP 8:** Python's official style guide, providing conventions for writing clean, consistent Python code. Following it is highly recommended.
* **Key Elements:**
    * **Comments:** Explain the "why" behind your code, not just the "what". Use `#` for single-line comments. Use triple quotes `"""Docstring goes here"""` (docstrings) or multiple `#` lines for multi-line comments/documentation. Keep comments concise and up-to-date.
    * **Indentation:** Crucial for Python's syntax. Use 4 spaces per indentation level (recommended by PEP 8) to define code blocks (within functions, loops, conditionals). Consistent indentation improves readability significantly.
    * **Naming Conventions:** Use descriptive names for variables and functions (e.g., `failed_login_attempts` instead of `fla`).
    * **Whitespace:** Use spaces appropriately around operators and commas to improve clarity.
    * **Line Length:** Keep lines under 79 characters (PEP 8 guideline) for better readability.
* **Syntax:** Pay attention to details: use quotes for strings (`"hello"`), no quotes for numbers (`123`) or Booleans (`True`/`False`), use brackets `[]` for lists, and ensure headers for `if`, `for`, `while`, `def` end with a colon `:`.

## Collaboration

* Writing readable, well-commented, and consistently styled code (following PEP 8) is vital when working on a team.
* It allows others to understand, use, and modify your code efficiently.
* Sharing code snippets and seeking/giving feedback improves code quality and team productivity.
