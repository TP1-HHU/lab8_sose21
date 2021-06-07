# Lab 8

Write a class `Fraction` that allows to represent fractions of integer numbers, i.e. *n/d*, where *n, d* are integer numbers.
Use `const` wherever possible.
The things you have to implement as member functions of the class are:


- A standard constructor that accepts two integers, nominator and denominator.
- The function `decimal()` that returns the decimal (floating point) value of the fraction as a `double` value.
- The function `invert()` that inverts the fraction.
- The overloaded `operator+=()`, `operator*=()` and `operator/=()` functions.
  - `void operator+=(const Fraction& f)`
  - `void operator*=(const Fraction& f)`
  - `void operator/=(const Fraction& f)`
- The function `print()` that prints the string `n/d` (and nothing else) to the console.
- Implement a private member function (used by the public functions) ```normalize``` that normalizes the fraction after every manipulation. For this you will have to implement a second private member function ```gcd()``` that determines the greatest common divisor of nominator and denominator.
- Implement the binary operators
  - ```Fraction operator+(const Fraction& a, const Fraction& b)```,
  - and ```Fraction operator*(const Fraction& a, const Fraction& b)```
as _friends_ of the class.
- Implement an overloaded << operator to simplify the output of the fraction into any kind out stream (e.g. using ```cout``` or an ```fstream```object).
For this you have to add ```#include <ostream>```.
The stream operator << is added as a friend to the class. Its interface is
```std::ostream& operator<<(std::ostream& stream, const Fraction& f)```. The ```stream``` object can then be used like any stream object inside the operator function (i.e. like ```cout```).
