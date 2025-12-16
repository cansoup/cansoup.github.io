---
layout: default
title: "Ch4. Control Flow"
tags: swift5
---
# 📅 Today I Learned (2025-12-15) - Swift 5 Control Flow

## ✨ What I Learned Today (Key Summary)

* Optional Unwrapping: Learned how Swift safely handles optional variables using `if let` and `guard let` to prevent runtime errors caused by nil.
* Range Operators: Explored Swift's unique range syntax (`...` and `..<`) and their usage in for-in loops.
* Loop Structures: Noticed Swift's `while` / `repeat-while` structures, which differ from traditional do-while.
* Switch Statement: Observed that Swift's `switch` statements do not require an explicit `break` for case exit, unlike JavaScript or C++.
* `guard` Statement: Investigated the difference between `if` and `guard` statements, focusing on early exit for precondition checks.

---

## 📚 Detailed Content & Review

### 1. Understanding Optional Unwrapping (if let vs. guard let)
* **Core Concept:** Swift variables can be declared as Optionals (marked with ?), meaning they either hold a value or are `nil` (no value). Unwrapping is the process of safely accessing the value if it exists.
  - `if let`: Used when you only need to execute code if the optional has a value. The unwrapped constant/variable is only accessible inside the if block.
  - `guard let`: Used for early exit (precondition check). If the optional is nil, the guard fails, and the function/loop/scope immediately exits (must include return, break, or continue). The unwrapped constant/variable remains accessible after the guard statement for the rest of the scope.

### 2. Range Operators in for-in Loops
* **Core Concept:** Swift uses specific operators to define ranges, particularly useful for iteration.

| Operator |Name|Example (0...n)|Meaning|
|--|--|--|--|
|`...`|Closed Range|0...5|Includes both 0 and 5. (e.g., 0, 1, 2, 3, 4, 5)|
|`..<`|Half-Open Range|0..<5|Includes 0 but excludes 5. (e.g., 0, 1, 2, 3, 4)|

- **Usage**: The half-open range (..<) is used most frequently when iterating over arrays or collections, as collections are zero-indexed and the range typically goes up to (but not including) the count of the collection.

### 3. Comparison of Loop and Control Structures
|Feature|Swift 5|Other Languages (e.g., C/JS)|Comment|
|--|--|--|--|
|Loop|`while`|`while`|Standard loop
|Post-Test Loop|`repeat-while`|`do-while`|Runs the body at least once. Naming is a unique Swift trait.|
|Case Exit|`switch` (no implicit break)|`switch` (requires break)|Swift's cases are ""fall-through"" safe by default.|
- **Switch Feature:** The automatic exit after a matching case is a strong feature, making the code safer and less prone to accidental fall-through bugs common in C-like languages. If you do need fall-through, you must explicitly use the fallthrough keyword.

### 4. Practical Usage of guard vs. if
* **Difference:**
  - `if`: Executes code if a condition is met. Focuses on the "happy path."
  - `guard`: Executes code in the else block if a precondition is not met. Focuses on the "unhappy path" (failure condition).
* **Benefit:** Using guard keeps the main body of the function cleaner (no nested if statements) and makes the error handling path explicit and quick.
---

## 🚀 Next Learning Goal

* I plan to study **Functions** tomorrow.
