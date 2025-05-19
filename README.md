# M301 Number Series Analyzer

## Python Self-Study Assignment: Module 3 – Mastering the Basics

**Assignment Title:**
“Number Series Analyzer: Parsing and Statistics”

**Assignment Overview:**
In this project, you will build a Python function that takes a single string of space-separated positive integers, parses it character-by-character (without using `.split()`), and computes the **sum**, **count**, **minimum**, **maximum**, and returns a comma-separated representation of the numbers entered. This reinforces string manipulation, type conversion, loops, `range`, and function design.

---

**Objectives:**
By completing this assignment, you will:

* Manually parse a space-separated string of digits using loops and indexing.
* Convert digit substrings to integers with `int()`.
* Maintain running aggregates (sum, count, min, max) in one pass.
* Build a comma-separated string of the parsed numbers.
* Encapsulate all logic in a single reusable function.

> **Note:** Do **not** use `.split()`, lists, or dictionaries—only primitive types and loops.

---

**Instructions:**

1. **Write the Function**

   * Signature:

     ```python
     def parse_and_compute(s):
         """
         Parses s character-by-character,
         extracts each positive integer, and computes:
           - total sum
           - count of numbers
           - minimum value
           - maximum value
           - a comma-separated string of the numbers entered
         Returns: total, count, minimum, maximum, numbers_str
         """
         # your implementation
     ```
   * Inside the function:

     * Accumulate digit characters into a temporary string `curr`.
     * On any non-digit (e.g., space), convert `curr` to `int`, update aggregates, append to `numbers_str`, then reset `curr`.
     * After the loop, flush any remaining `curr`.
     * Trim the trailing comma and space from `numbers_str` if any numbers were found.

2. **Edge Cases:**

   * Empty or non-digit input → function should return `(0, 0, None, None, "")`.
   * Leading/trailing/multiple spaces handled gracefully.

---

**Technical Requirements:**

* **Data Types:** Only strings and integers.
* **Loops:** Use `for` or `while` to traverse the input string.
* **Conditionals:** Use `if`/`else` to detect digits vs. non-digits.
* **Functions:** Single function `parse_and_compute(s)`.
* **String Operations:** Concatenation and slicing—no helper methods like `.split()`.

---

**Deliverables:**

* **Python Script:**

  * File name: `M301_series_analyzer.py`
  * Contains **only** the `parse_and_compute(s)` function as specified.

---

**Example of Usage:**

```python
# Suppose you call:
total, count, minimum, maximum, numbers_str = parse_and_compute(" 12 3 45  6 ")

# You would get:
# total       == 66
# count       == 4
# minimum     == 3
# maximum     == 45
# numbers_str == "12, 3, 45, 6"
```

---

**Evaluation Criteria:**

* **Correctness (50%)**

  * Accurate parsing without `.split()`.
  * Proper sum, count, min, max, and string formatting.
* **Code Quality (30%)**

  * Clear, well-commented logic.
  * Meaningful variable names.
* **Edge-Case Handling (20%)**

  * Graceful handling of empty input or extra spaces.

---

**Tip for Success:**
Sketch your parsing loop on paper first: decide when you build up `curr` and when you flush it into your aggregates. That clarity will make the code straightforward.
