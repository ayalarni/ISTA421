#C#,Chapter 19, Pages 423-438

##Norma I. Ayala-Rosa

1. What is an enumerable collection? Is a collection that implements the System.Collections.!Enumerable interface.

2. What properties and methods does the IEnumerable interface contain? It contains a single method called GetEnumerator:

IEnumerator GetEnumerator();

3. What properties and methods does the IEnumerator interface contain? It specifies the following one property and two methods:

Object Current { get;  }
Bool MoveNext();
Void Reset();

4. What values does the MoveNext() method return? Return a True or False, a Boolean.
What does it do? The enumerator points before the first element, the MoveNext method moves the pointer down to the next (first) item in the list.

5. What values does the Reset() method return? It takes it back before the first item.
What does it do? It does not return any value.

6. Are IEnumerable and IEnumerator type safe? No, they are not type safe.
Why or why not? If not, how do you implement type safety? By using generics.

7. Why don't recursive methods retain state when used with data structures like binary trees?
A new stack.

8. How do you define an enumerator? A pointer indicating answer on a list.

9. What is an iterator? It is a block of code that yields an ordered sequence of values.  

10. What does yield do? The yield keyword indicates the value that should be returned by each iteration.  It calls a temporary halt to the method, passing back a value to the caller.












