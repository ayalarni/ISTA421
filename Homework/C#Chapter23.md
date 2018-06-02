# C#Chapter23#Pages517-558

## Norma I. Ayala-Rosa

1. List two reasons for multitasking, and explain the rationale for them.
 a. to improve responsiveness - performing tasks not requiring processor time, such as reading from or writing to a local disk or sending and receiving data across a network.  

 b. to improve scalability - a powerful CPU capable of supporting true multitasking, and operating systems parallizing tasks easily.

2. Explain Moore's law. A number of transistors that can be placed inexpensively on an integrated circuit will increase exponentially, doubling approx. every two years.  "cramming more components onto integrated circuits", 1965, Gordon E. Moore  What does Moore's law have to do with multitasking? The ability to pack transistors together led to the ability to pass data between them more quickly.

3. In UWP, what namespace is used as the container for the multitasking methods?
System.Threading.

4. What is the difference between tasks and threads? Explain.
A Task class is unity of work that needs to be done.
A Thread is a context frame on a processor that executes.

5. What is the ThreadPool?
It implements a number of optimazition on the CPU, units of work change.
A queuing mechanism distributing the workload (threads), when unit of work comes in, it assigns it.

6. What parameters does the Task() constructor take?
A Task constructor is overloaded

7. How do you start a thread?
Start.Thread()

8. What is the difference between the Start() and Run() methods?
Start method is used as a start object.
Run method runs as soon as is created.

9. What is the difference between creating independent tasks with Tasks and parallelization with Parallel?
Using Tasks the programmer decides how to divide the work.
On parallel, the program decides how to divide the work.

10. Explain how manual cancellation works using a cancellation token.
Create a token and every execution creates a token.
