# Dart OOP Assignment: Kigali Bus Card

**Name:** Abdallah Awad Attalmnan
**Student ID:** 26496

## My numbers
D = 96
L = 6
Starting balance = 1960 RWF
Bus fare = 296 RWF
Student discount = 16%

## Output of main.dart
```text
Error: name too short
Owner: Ama | Balance: 1000 RWF
Owner: Abdallah Awad Attalmnan | Balance: 1000 RWF
Error: top-up must be 500 to 50000 RWF
Topped up 2000 RWF
Paid 296 RWF
Paid 296 RWF
Owner: Abdallah Awad Attalmnan | Balance: 2408 RWF
Student discount: 47 RWF
Paid 249 RWF
Owner: Abdallah Awad Attalmnan | Balance: 1711 RWF
Student card: 16% off
```

## Part 1: Why no setter for balance?
Because allowing direct modification of `_balance` through a public setter would break security and business rules (anyone could set their balance to any amount without paying). Instead, `_balance` should only change through controlled methods like `topUp()` (which checks the 500–50000 RWF limit) and `pay()` (which checks if there is enough balance).

## Part 2: What does ~/ do?
The `~/` operator performs **integer division** (truncating division): it divides two numbers and drops the decimal part, returning an `int` instead of a `double`.
- `print(237 * 17 / 100);` outputs `40.29` (a `double` with decimals).
- `print(237 * 17 ~/ 100);` outputs `40` (an `int` with the `.29` truncated).
This is needed because `_balance` and `fare` are `int` values in Dart.

## Part 4: Bug table

## Part 5
My prediction:

Real output:

Was I right?