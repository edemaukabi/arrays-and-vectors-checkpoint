# DS-Algo — Arrays & Nested Loops Checkpoint

Pseudocode solutions for two algorithm problems using arrays and nested loops.
All solutions are written in `.algo` pseudocode with `VAR / BEGIN / END` structure.

---

## Problem 1 — Sum of Distinct Elements (`problem1_distinct_sum.algo`)

Given two sets of elements, find the sum of all elements that appear in **exactly one** of the two sets (i.e. not shared by both).

**Example**
```
Set 1 : [3, 1, 7, 9]
Set 2 : [2, 4, 1, 9, 3]
Distinct : 7 (only in Set1), 2 and 4 (only in Set2)
Output  : 13
```

**Approach**
- Initialise `sum = 0`.
- Use a nested loop to compare every element of Set1 against all elements of Set2. Add to sum if not found.
- Repeat in reverse: compare every element of Set2 against Set1.

**Key concepts demonstrated**
- Arrays for storing sets
- Nested loops for cross-set search
- Boolean flag (`found`) to track membership

---

## Problem 2 — Dot Product & Orthogonality (`problem2_dot_product.algo`)

Calculate the dot (scalar) product of two vectors and determine whether they are orthogonal. Two vectors are orthogonal when their dot product equals zero.

**Procedure variant** — result stored in an output parameter passed **by reference** (`VAR ps`).

**Function variant** — result returned directly; `size` is passed **by value**.

**Example**
```
v1 = [1, 0]   v2 = [0, 1]   dot product = 0  -> ORTHOGONAL
v1 = [1, 2]   v2 = [3, 4]   dot product = 11 -> NOT orthogonal
```

**Key concepts demonstrated**
- Arrays for representing vectors
- Nested loop structure (outer loop over n pairs, inner loop inside dot_product)
- Two types of parameter passing: by reference (procedure) vs by value / return (function)

---

## File Structure

```
ds-algo/
├── problem1_distinct_sum.algo   # Sum of distinct elements
├── problem2_dot_product.algo    # Dot product + orthogonality check
└── README.md
```

---

## Checkpoint Criteria

| Criterion | Covered in |
|---|---|
| Use of an array | Both problems — sets and vectors stored as arrays |
| Use of nested loops | Problem 1 (search loop) · Problem 2 (pairs × dimensions) |
| Code commented & clear | Inline comments + trace in each `.algo` file |
| Different parameter passing types | Problem 2 — by reference (procedure) vs by value (function) |
