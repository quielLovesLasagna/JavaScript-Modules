<h1>Modules Overview</h1>

A module is a reusable piece of code that encapsulates implementation details of a certain part of our project (sounds like a function or even a class) but the difference is usually a standalong file. This is not always the case but normally when we think of a module we think of a separate file.

![Module]()

A module always contains some code but it can also have ```imports``` and ```exports```.
- ```exports```, as the name says, we can export values out of a module. For example, simple values or even entire functions. Whatever we export from a module is called the ```PUBLIC API```. This is just like classes where we can also expose a public API for other codes to consume. In the case of modules, this public API is actually consumed by ```importing``` values into a module. 

- Just like we can ```export``` values, we can also ```import``` values from other modules. These other modules from which we import are called ```dependencies``` of the importing modules because the code that is in the module, that is importing cannot work without the code that it is importing from the external module. 

This entire logic is true for all modules in all programming languages. 

We can write code without modules. However, when a code base grows bigger and bigger, there start to be many advantages of using modules:

1) Modules make it really easy to compose software. We can think of modules as small building blocks then we can then put together in order to build really complex applications
