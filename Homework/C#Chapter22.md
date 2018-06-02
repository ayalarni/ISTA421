# C#Chapter22#Pages493-514

## Norma I. Ayala-Rosa

1. Explain the difference between the concepts of associativity and precedence.
Each operator has an associativity defining whether the operator evaluates from left to right or from right to left.  The = operator is right-associative, it evaluates from right to left, so a=b=c is the same as a=(b=c).

Precedence- * operator has a higher precedence than the + operator, a + b * c is the same as a + (b * c).

2. Explain the difference between the concepts of binary and unary operators.
A binary operator is an operator with two operands; the multiplication operator (*) is a binary operator.

A unary operator is an operator that has just one operand, i.e. the increment operator (++) is a unary operator.

3. List four constraints imposed by C# with respect to operator overloading.
 a. cannot change the precedence and associativity of an operator
 b. cannot change the multiplicity
 c. cannot invent new operator symbols
 d. cannot change the meaning of operators
 
4. What is the syntax for overloading operators? Discuss access, scope, return value types, and parameter
types and multiplicity.
syntax - Hour Example(Hour a, Hour b)
{
   return a + b;
}

5. What are symmetric overloaded binary operators and how do they differ from non-symmetric over-
loaded binary operators?
A symmetric overloaded binary operators one must declare a binary + operator whose first parameter is an Hour and whose second parameter is an int.  They come in pairs.

6. Can you overload compound assignment operators? If so, please state how you do so. If not, explain why not.
No, because it is automatically done.

7. What is the difference between overloading increment and decrement operators for value types and reference types?
The rules apply:
 a. the operator is public, all operators must be public.
 b. the operator is static; never polymorphic and cannot use the virtual, abstract, override, or sealed modifiers.
 c. a binary operator has two explicit arguments, and a unary operator has one explicit argument.

The return type of the increment and decrement operators must be the same as the parameter type.

8. Why do we overload some operators in pairs?
C# compiler enforces this very reasonable expectation by insisting that if one define either operator == or !=, one must define them both.

9. What is the difference between widening conversion and narrowing conversion?
Widening conversion changes a value to a data type.
Narrowing changes a value to a data type that may not be able to hold a data value.

10. What is the difference between explicit conversion and implicit conversion?
Explicit conversion the complier does it automatically and the implicit must be programed.
 