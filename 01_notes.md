# 01_notes.md

## Chapter 2: The Nature of Complexity

### 2.1 Complexity defined

- Complexity is anything related to the structure of a software system that makes it hard to understand and modify the system.
- The overall complexity of a system is determined by the complexity of each part weighted by the fraction of time developers spend working on that part.
  - Isolating the complexity in a place where it will never be seen is almost as good as eliminating the complexity entirely.

### 2.2 Symptoms of complexity

- Complexity manifests itself in three general ways: - Change amplification - Cognitive load - Unknown unknowns

### 2.3 Causes of complexity

- Complexity is caused by two things: dependencies and obscurity.
  - Dependency is a given piece of code that cannot be understood and modified in isolation.
    - e.g., A web page uses the same banner across multiple pages, where the background colour must be the same across all pages. As such, if the background colour is changed for one page, then it must be changed for all of them.
- Obscurity is when important information is not obvious.
  - e.g., A variable name that is so generic that it doesn’t carry much useful information (e.g., time). Or, the documentation for the variable doesn’t specify its unit when applicable (e.g., time in seconds or milliseconds?)

### 2.4 Complexity is incremental

- Complexity usually isn’t caused by a single catastrophic error; it accumulates through hundreds or thousands of small dependencies and obscurities over time.
  - In order to slow the growth of complexity, a “zero tolerance” philosophy must be adopted (further discussed in Chapter 3).

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
