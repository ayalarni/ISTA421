# C# Chapter 21, Pages 469-492

## Norma I. Ayala-Rosa

1. What is the difference in the purposes of SQL and LINQ? SQL provides a high-level description of the data that can be retrieve but does not indicate exactly how the database management system should retrieve it.
In other words, why do we need two different query languages?
LINQ Language-Integrated Query queries data from an application code itself.
Does LINQ replace SQL? No.
Does SQL make LINQ unnecesary? No.

2. What is the one essential requirement for the datastructures used with LINQ? It requires the data to be stored in a data structure that implements the IEnumerable or IEnumerable<T> interface. 
Why is this requirement important? Because the enumeration, it allows you to process a lot of data from one item to the next.

3. Were does the LINQ Select() method live? Is an extension method of the Enumerable class.

4. (Select) Explain, token by token, each token in this line of code:
IEnumerable<string> customerFirstNames = customers.Select(cust => cust.FirstName);
Interface generic type / variable name / Object / Method / Lambda expression / Object / Property of object

5. (Filter) Explain, token by token, each token in this line of code:
IEnumerable<string> usCompanies = addresses.Where(addr =>
String.Equals(addr.Country, "United States")).Select(usComp => usComp.CompanyName);
Interface generic type / data structures / addr is every record in turn / String is a class / Equals is a method / Country is a property/
usComp is a name / resultin the name of each company is US

6. (OrderBy) Explain, token by token, each token in this line of code:
IEnumerable<string> companyNames = addresses.OrderBy(addr =>
addr.CompanyName).Select(comp => comp.CompanyName);
companyNames is variable / OrderBy is a method / addr is every record / 

7. (Group) Explain, token by token, each token in this line of code:
var companiesGroupedByCountry = addresses.GroupBy(addrs => addrs.Country);
var is unspecified variable type / variable / addresses is Object / addrs is every record in turn / 

8. (Distinct) Explain, token by token, each token in this line of code:
int numberOfCountries = addresses.Select(addr => addr.Country).Distinct().Count();
int is a data type integer / variable / Distintc eliminates duplicates

9. (Join) Explain, token by token, each token in this line of code:
var companiesAndCustomers =
customers.Select(c =>
new { c.FirstName, c.LastName, c.CompanyName }).Join(addresses, custs =>
custs.CompanyName, addrs => addrs.CompanyName, (custs, addrs) =>
new {custs.FirstName, custs.LastName, addrs.Country });

var is any type / customers is data structure / 

10. Explain the difference between a deferred collection and a static, cached collection.
A cached collection is

