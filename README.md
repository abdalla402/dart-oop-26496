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

| Bug | The line | Why it is wrong (your words) | Your fix |
| :--- | :--- | :--- | :--- |
| 1 | `String _brand;` and `int _battery;` | Non-nullable fields must be given an initial value when declared. | Changed to `String _brand = '';` and `int _battery = 0;` |
| 2 | `SmartPhone (String brand, int battery, String system) {` | The child constructor did not call the parent constructor to initialize `_brand` and `_battery`. | Added `: super(brand, battery)` |
| 3 | `String system = '';` (used as `_system`) | The field was declared without an underscore (`system`), while the constructor and `restart()` used `_system`. | Renamed the field to `String _system = '';` |
| 4 | `@override` above `void restart()` | `@override` can only be used if the parent class (`Phone`) already has a `restart()` method. | Removed `@override` |
| 5 | `p.battery = 100;` and `print(p.battery());` | `battery` had no setter to assign `100`, and `battery` is a getter so it should not be called with `()`. | Added a `battery` setter (accepting `0` to `100`) and changed `p.battery()` to `p.battery` |
| Not a bug | `Phone p = new Phone ('Tecno', 50);` | Why is this line fine? Using the `new` keyword is optional in Dart; it looks unusual in modern Dart, but it is valid syntax. | (none) |

## Part 5
My prediction:

Real output:

Was I right?