# ********** 08/26/2020 **********

## Performance
Studied what needs to bo done in terms of performance data collection, visualization and analysis

### Measurements
- execution time
- number of computation
- idle rate, ...

#### Memory

* **How many**

   + instructions are executed, floating point
   + level 1 and 2 data cache 

      - misses
      - hits
      - branches taken

* **When and where**

   + memory allocated/de-allocated
   + memory leaks

* **What are the I/O characteristics**

   + the peak read and write bandwidth of

      - individual calls, total volume?

* **How much computation time**
  + each application routine
  + outer loops
  + each statement within loops

### Analysis

* **How much overhead time** 

   + waiting for collectives
   + I/O operations
   + initialization
   + I/O phases

* **Scalability**

  + efficiency
  + time breakdown of performance per unit (core, node, ...)

**more info** on [APEX/TAU](http://stellar.cct.lsu.edu/files/hpx_sc15/APEX_and_TAU_slides.pdf)

## Visualization

### Code Execution
* Trace data
* Performance in terms of:
  + computation efficiency (throughput)
  + execution time
  + I/O 
  + memory efficiency
  + scalability

### Code structure
- expression-tree (PhySL)
- data-flow
- control flow

## Resource Allocation Algorithm

### Input

* set _**A**_ of variable _arrays_
* set _**C**_ of _computations_ on one or more elements of  **A**
* expression-tree _**E**_ where

   - **nodes** represent computations (an element of **C**), and
   - **edges** represent data dependency between two computations.
: NOTE: collapsing the expression tree nodes

### Goal

* schedule computations in the expression tree on _p_ (a fixed number) of
  processors.
  
 for more info please see https://github.com/rtohid/scheduler/blob/master/model/dependency_graph.pdf

# ********** 08/26/2020 **********
