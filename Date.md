# Date

## Table of Contents

1. [Properties](#properties)
2. [Operations](#operations)

## Properties

- [Day](#day)
- [Month](#month)
- [Year](#year)

### Day
- Data Type: Integer
- Constraints:
  - 1 ≤ x ≤ 31
- Programming Type: int8 (0 ≤ x ≤ 255)

### Month
- Data Type: Integer
- Constraints:
  - 1 ≤ x ≤ 12
- Programming Type: int8 (0 ≤ x ≤ 255)

### Year
- Data Type: Integer
- Constraints: /
- Programming Type: intMax (-∞ ≤ x ≤ ∞)

## Operations

### Comparison

A date is classically a compound of three fields: Day, month and year. All three fields are filled with numbers. These numbers are within respective ranges. When all three fields of a date are filled and you have two of these kind of dates comparison is trivial.

Actually, this is not always the case. Sometimes some fields have no value at all. Can you compare these, too?

| Day | Month | Year | Day | Month | Year | Comparable? | Case |
|-----|-------|------|-----|-------|------|----------------------|:------:|
| unset	| unset	| unset	| unset | unset	| unset | no        | (1) |
| unset	| unset	| unset	| unset | unset	| set   | no        | (1) |
| unset	| unset	| unset	| unset | set	  | unset | no        | (1) |
| unset	| unset	| unset	| unset | set	  | set   | no        | (1) |
| unset	| unset	| unset	| set	  | unset	| unset | no        | (1) |
| unset	| unset	| unset	| set	  | unset	| set   | no        | (1) |
| unset	| unset	| unset	| set	  | set	  | unset | no        | (1) |
| unset	| unset	| unset	| set	  | set 	| set   | no        | (1) |
| unset	| unset	| set	  | unset	| unset	| unset | no        | (1) |
| unset	| unset	| set	  | unset	| unset	| set   | partially | (2) |
| unset	| unset	| set	  | unset	| set	  | unset | no        | (1) |
| unset	| unset	| set	  | unset	| set	  | set   | partially | (2) |
| unset	| unset	| set	  | set	  | unset	| unset | no        | (1) |
| unset	| unset	| set	  | set	  | unset	| set   | partially | (2) |
| unset	| unset	| set	  | set	  | set   | unset | no        | (1) |
| unset	| unset	| set	  | set	  | set   | set   | partially | (2) |
| unset	| set	  | unset	| unset	| unset	| unset | no        | (1) |
| unset	| set	  | unset	| unset	| unset	| set   | no        | (1) |
| unset	| set	  | unset	| unset	| set	  | unset | no        | (1) |
| unset	| set	  | unset	| unset	| set	  | set   | no        | (1) |
| unset	| set	  | unset	| set	  | unset	| unset | no        | (1) |
| unset	| set	  | unset	| set	  | unset	| set   | no        | (1) |
| unset	| set	  | unset	| set	  | set	  | unset | no        | (1) |
| unset	| set	  | unset	| set	  | set	  | set   | no        | (1) |
| unset	| set	  | set	  | unset	| unset	| unset | no        | (1) |
| unset	| set	  | set	  | unset	| unset	| set   | partially | (2) |
| unset	| set	  | set	  | unset	| set	  | unset | no        | (1) |
| unset	| set	  | set	  | unset	| set	  | set   | partially | (3) |
| unset	| set	  | set	  | set	  | unset	| unset | no        | (1) |
| unset	| set	  | set	  | set	  | unset	| set   | partially | (2) |
| unset	| set	  | set	  | set	  | set	  | unset | no        | (1) |
| unset	| set	  | set	  | set	  | set	  | set   | partially | (3) |
| set	  | unset	| unset	| unset	| unset	| unset | no        | (1) |
| set	  | unset	| unset	| unset	| unset	| set   | no        | (1) |
| set	  | unset	| unset	| unset	| set	  | unset | no        | (1) |
| set	  | unset	| unset	| unset	| set	  | set   | no        | (1) |
| set	  | unset	| unset	| set	  | unset	| unset | no        | (1) |
| set	  | unset	| unset	| set	  | unset	| set   | no        | (1) |
| set	  | unset	| unset	| set	  | set	  | unset | no        | (1) |
| set	  | unset	| unset	| set	  | set	  | set   | no        | (1) |
| set	  | unset	| set	  | unset	| unset	| unset | no        | (1) |
| set	  | unset	| set	  | unset	| unset	| set   | partially | (2) |
| set	  | unset	| set	  | unset	| set	  | unset | no        | (1) |
| set	  | unset	| set	  | unset	| set	  | set   | partially | (2) |
| set	  | unset	| set	  | set	  | unset	| unset | no        | (1) |
| set	  | unset	| set	  | set	  | unset	| set   | partially | (2) |
| set	  | unset	| set	  | set	  | set	  | unset | no        | (1) |
| set	  | unset	| set	  | set	  | set	  | set   | partially | (2) |
| set	  | set	  | unset	| unset	| unset	| unset | no        | (1) |
| set	  | set	  | unset	| unset	| unset	| set   | no        | (1) |
| set	  | set	  | unset	| unset	| set	  | unset | no        | (1) |
| set	  | set	  | unset	| unset	| set	  | set   | no        | (1) |
| set	  | set	  | unset	| set	  | unset	| unset | no        | (1) |
| set	  | set	  | unset	| set	  | unset	| set   | no        | (1) |
| set	  | set	  | unset	| set	  | set	  | unset | no        | (1) |
| set	  | set	  | unset	| set	  | set	  | set   | no        | (1) |
| set	  | set	  | set	  | unset	| unset	| unset | no        | (1) |
| set	  | set	  | set	  | unset	| unset	| set   | partially | (2) |
| set	  | set	  | set	  | unset	| set	  | unset | no        | (1) |
| set	  | set	  | set	  | unset	| set	  | set   | partially | (3) |
| set	  | set	  | set	  | set	  | unset	| unset | no        | (1) |
| set	  | set	  | set	  | set	  | unset	| set   | partially | (2) |
| set	  | set	  | set	  | set	  | set 	| unset | no        | (1) |
| set	  | set	  | set	  | set	  | set 	| set   | optimal   | (4) |

#### Cases

| Case | Description | Distribution |
|:----:|-------------|--------------|
| (1) | Cannot be compared. | 48 |
| (2) | If both years are unequal, then both are comparable. Otherwise: Both cannot be compared. | 12 | 
| (3) | If both years are unequal, then both are comparable. Otherwise: If both months are unequal, then both are comparable. Otherwise: Both cannot be compared. | 3 |
| (4) | Both dates are always comparable. | 1 |
