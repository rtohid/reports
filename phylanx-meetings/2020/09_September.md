## 
What are you trying to do?

Develop a performance analysis API for HPX&Phylanx for both single and multiple
runs:

1. **Profiling** measuring execution time of each task(s) and efficiency of

   resources they run on.

2. **Tracing** studying performance efficiency of the system.

3. **code structure** data type, data dependencies, number of operations, ...

---
---

## How is it done today, and what are the limits of current practice?

I don't know of a single package supporting all three. In the case of Phylanx
with HPX+APEX+Traveler there's support for single runs both in terms visualizing
performance metrics as well as execution trees. However, it might be easier for
users if some APIs developed to remove the scaling
(performance and execution time )

---
---

## What is new in your approach and why do you think it will be successful?

The greatest obstacle here is getting many independent tools and libraries to
work together within a pipeline. This is more obvious in the case of many common
distributed applications which rely and separate libraries to express
parallelism. Meanwhile, Phylanx built on top of HPX and APEX enables us to
easily collect such information at a couple of levels of abstraction. In
addition as AST, PhySL expression tree, and perhaps CFG are built through
execution of PhySL code, the new set of profiling and visualization may provide
better understanding of code characteristics for adaptivity and analysis.

---
---

## Who cares? If you are successful, what difference will it make?

There are a few benefits:

* Automating performance measurement, reporting and to some extent analysis.
* Provides more comprehensive picture of the computation and even maybe
  resources.
* long long term: maybe a start for providing a gui for code analysis. For
  example generating the graph representation of tasks and allow user to pick a
  set of optimization for a task node or a set of them as subtree of expression
  tree.

---
---

## What are the risks?
The risk here is we are relying on automatic transcompilation of Python to PhySL
which may get expensive to track globally specially if all the performance 

---
---

## How much will it cost?                                                                 
A few developers.

---
---
                                                                                                                                                                                     

## How long will it take?

3-6 months for mid-term, 6-12 months for final results. 

## What are the mid-term and final “exams” to check for success?
- **Midterm** Generating plots and graphs for local runs
- **Final** performance analysis of the whole system: Distributed + GPU that may
  also run remotely.