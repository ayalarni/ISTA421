# C#,Chapter24,Pages575-600

## Norma I. Ayala-Rosa

1. What are the two scenarios in which you can use PLINQ to speed up operations?
PLINQ is ideal for scenarios that involve data sets with large numbers of elements, or
if the criteria specified for matching data involve complex, computationally expensive operations.

Why does using PLINQ in these scenarios speed up processing?
PLINQ works by dividing a data set into partitions and then using tasks to retrieve the data that matches the criteria specified by the query for each partition in parallel.

2. How does AsParallel qualify as an extension method?
AsParallel extension method coverts a LINQ query into a PLINQ query.

First, explain what an extension method is.


How you define extension methods, and then explain why AsParallel qualifies as an extension method.

3. How do you cancel a PLINQ query before it finishes?
Specify a CancellationToken object from a CancellationTokenSource and use the WithCancellation extension method of the ParallelQuery. Specify WithCancellation only once in a query.  Cancellation applies to all sources in the query.  If the CancellationTokenSource object used to generate the CancellationToken is canceled, the query stops with an OperationCanceledException exception.

Be specific with respect to the variables and methods used for the cancellation operation, and how the variables and methods are used.

4. Why is it important to synchronize concurrent access to a server?
One can end up with applications that exhibit unpredictable (and erroneous) behavior.

Give an example of a specific condition that will cause an error in your application if concurrent access is not synchronized.
If two tasks attempt to access and modify the same data

5. What does the lock statement do?
It attempts to obtain a mutual-exclusion lock over the specified object or reference type, and it blocks if this same object is currently locked by another thread.

6. This is not in the book. Define mutex, define semaphore, and explain the difference between them.

7. What does it mean to say that some collection classes are not thread safe? Explain how not being thread safe may lead one of these collection classes to produce a malfunction in the program.

8. Explain how thread safe collection classes are made thread safe.

9. Why are thread safe classes slower than non-thread safe classes? Be specific.
 