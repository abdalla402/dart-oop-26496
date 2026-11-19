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
(will be pasted after Part 3)

## Part 1: Why no setter for balance?
Because allowing direct modification of `_balance` through a public setter would break security and business rules (anyone could set their balance to any amount without paying). Instead, `_balance` should only change through controlled methods like `topUp()` (which checks the 500–50000 RWF limit) and `pay()` (which checks if there is enough balance).

## Part 2: What does ~/ do?

## Part 4: Bug table

## Part 5
My prediction:

Real output:

Was I right?