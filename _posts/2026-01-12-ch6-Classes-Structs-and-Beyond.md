---
layout: default
title: "Ch6. Classes Structs and Beyond"
tags: swift5
---
# 📅 Today I Learned (2026-01-12) - Swift Class, Structure, and Chaining optionals

## ✨ What I Learned Today (Key Summary)
* Value vs Reference Types: Deepened understanding of how Swift manages memory for different types (Struct/Enum vs Class/Function/Closure).
* Access Control: Learned about `public`, `internal`(default), `fileprivate`, and `private` keywords to manage code visibility.
* Type Properties: Differentiated between `static` and `class` keywords for properties and methods regarding inheritance.
* Struct Mutating: Understood why `mutating` is required to modify properties within a value type.
* Optional Chaining: Explored the concise syntax for accessing properties and methods on optional instances.

---

## 📚 Detailed Content & Review
### 1. Value Types vs Reference Types
* **Core Concept:** Swift categorises types into Value types (copied when assigned) and Reference types (shared via pointer).
* Review/Summary:
  * Value Types: `struct`, `enum`, and all basic types(`Int`, `String`, `Array`, etc.). Each instance keeps a unique copy of its data.
  * Reference Types: `class`, `function`, `closure`. Multiple variables can point to the same instance in memory.
* Self-Reflection: While common in many languages, explaining the "Copy-on-Write" behavior and memory management in Swift is crucial for performance optimisation.

### 2. Access Control in Swift
* Review/Summary: Swift provides levels of access to hide implementation details.
  * `public`: Accessible from any module, but cannot be subclassed/overridden outside the defining module.
  * `internal` (Default): Accessible within any source file from their defining module.
  * `fileprivate`: Restricts the use to the defining source file.
  * `private`: Restricts the use to the enclosing declaration (scope).

### 3. Static vs Class Properties/Methods
* **Core Concept:** Both define properties/methods on the type itself rather than an instance.
* Key Difference:
  * `static`: Final by default. Cannot be overridden by subclasses.
  * `class`: Allowed to be overridden in subclasses, specifically for class types.

### 4. Structs and the `mutating` Keyword
* **Core Concept:** Structs are value types, and their properties are immutable by default when the struct instance is a constant.
* Review/Summary: To modify a property within a struct's method, the method must be marked with `mutating`. This explicitly tells the compiler that this method will modify the value of the instance, effectively replacing the old value with a new one.
* When to use: Use them by default for data containers and simple models. Switch to Class only when inheritance or reference sharing is specifically required.

### 5. Initialisation in Subclasses
* **Core Concept:** A process for querying and calling properties, methods, and subscripts on an optional that might currently be `nil`.
* Review/Summary: Similar to Javascript's `?.`, if the optional contains a value, the call succeeds; if the optional is `nil`, the call returns `nil`. This prevents runtime crashes and avoids nested `if-let` statements.

---
## 🚀 Next Learning Goal
* 
