# Unorganized Notes

## Chapter 3: Working Code Isn’t Enough (Strategic vs. Tactical Programming)

Many organizations encourage tactical programming - getting features working as quickly as possible. However, good design requires a more strategic approach with better designs. Strategic programming focuses on the long term and is usually cheaper over time.

### 3.1 Tactical programming

- Tactical programming is an approach where the main focus is to get something working, such as a new feature or bug.
  - The trade-off with tactical programming is the lack of time spent and consideration of good system design.

### 3.2 Strategic programming

- The first step to becoming a good software designer is to realize taht working code isn't enough. It's not acceptable to introduce unnecessary complexities in order to finish your current task faster.
  - The most important thing is the long-term structure of the system.

### 3.3 How much to invest?

- A huge up-front investment, such as trying to design the entire system, won't be effective.
  - This is the Waterfall method.
- The best approach is to make a lot of small investments on a continual basis. The suggested amount is 10-20% of your total development time on these investments.

### 3.4 Startups and investment

- Many startups take a tactical approach, spending little effort on design and even less on cleanup when problems pop up.
  - They rationalize this with the thought that, if they are successful, they'll hav eenough money to hire extra engineers to clean things up.
    - However, if you're a company leaning in this direction, you should realize that once a code base turns to spaghetti, it is nearly impossible to fix. You will pay for high development cost for the life of the product.

### 3.5 Conclusion

- It's crucial to be consistent in applying the strategic approach and to think of investment as something to do today, not tomorrow.

## Chapter 4: The Nature of Complexity

### Modules Should Be Deep

- One of the most important techniques for managing software complexity is to design systems so that developers only need to face a small fraction of the overall complexity at any given time.
- This approach is called _modular design_, and this chapter presents its basic principles.

### 4.1 Modular design

- In modular design, a software system is decomposed into a collection of _modules_ that are relatively independent.
  - A module is any unit of code that has an _interface_ and an _implementation_.
    - e.g., A module can be a class in an object-oriented programming. Methods within a class or functions in a non object-oriented languages can also be thought of as modules. Higher-level subsystems and services, such as kernel calls or HTTP requests, are also modules.
  - There will always be _dependencies_ between modules.
- In order to identify and manage dependencies, we think of each module in two parts: _interface_ and an _implementation_.
  - The interface consists of everything tha developer working in a different module mustk now in order to use the given module.
    - The interface describes _what_ the module does but not _how_ it does it.
    - The implementation consists of the code that carries out the promises made by the interface.
- The best modules are those whose interfaces are much simpler than their implementations.

### 4.2 What's in an interface

- The interface to a module contains two kinds of information: _formal_ and _informal_.
  - The formal parts of an interface are specified explicitly in the code, and some of these can be checked for correctness by the programming language.
  - The informal parts of an interface include its high-level behaviour. For example, a function deletes the file named by one of its arguments.
    - If there are constraints on the usage of a class (perhaps one method must be called before another), these are also part of the class's interface.
    - Informal elements are not specified in a way that can be understood or enforced by the programming language.
    - In general, if a developer needs to know a particular piece of information in order to use a module, then that information is part of the module's interface.
      - The information aspects of an interface can only be described using comments, and the programming language cannot ensure that the description is complete or accurate.
      - For most interfaces, the informal aspects are larger and more complex than the formal aspects.

### 4.3 Abstractions

- The term _abstraction_ is closely related to the idea of modular design.
- An abstraction is a simplified view of an entity, which omits unimportant details.
- In modular programming, each module provides an abstraction in the form of its interface. The interface presents a simplified view of the module's functionality.
- In the definition of abstraction, the word "unimportant" is crucial. An abstraction can go wrong if it includes details that are not reall important and when it omits details that really are important (i.e., _false abstraction_).

### 4.4 Deep modules

- The best modules are those that provide powerful functionality, yet have simple interfaces.
  - The term _deep_ is used to desribe such modules.
  - TBA
