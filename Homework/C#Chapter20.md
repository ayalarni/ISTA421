#C#Chapter20,Pages439-466

##Norma I. Ayala-Rosa

1. What is a delegate? Explain delegates in terms of pointers and reference types.
A delegate is a reference to a method.  A delegate is an object that refers to a method.  A delegate is similar to a function pointer.
One can assign a reference to a method to a delegate in much the same way that you can assign an int value to an int variable.
A pointer is type safe and is NOT a reference type.

2. How do you declare a delegate? Include a discussion of types, return values, names, and parameters.
Start of with the word "delegate", then the data type delegate, next a name.
delegate void stopMachineryDelegate(); // the delegate type
private stopMachineDelegate stopMachinery; // an instance of the delegate

3. How do you create instances of delegates and assign values to the instance? delegate void stopMachineryDelegate(); // the delegate type
What are the values? A method.

4. How do you invoke a method that has been added to a delegate?
Use same syntax to invoke a delegate. 

5. What is an event? It can be used to define and trap significant actions and arrange for a delegate to be called to handle the situation. 
Why do we have events? An event source is usually a class that monitors its environment and raises an event when something significant happens.

6. How do you declare events?  Similarly to how you declare a field.  However, because events are intended to be used with delegates, the type of an event must be a delegate, and you must prefix the declaration with the event keyword. 
event delegatetype name

7. How do delegates recognize event subscriptions?  Use a lambda expression i.e. (() => { folder.StopFolding(0); });
How do you unsubscribe an event from a delegate? += 

8. How do you raise an event? Upon a significant event happens, call it like a method.
How do you declare code that raises an event? 

9. Explain with specificity what happens when an event fires and that event has been attached to a delegate.
When an occurence happens, notify delegates and the code executes.