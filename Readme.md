# Medusa

A lightweight paradigm for Distributed Computing

#### Anthony Erlinger
```
v0.0.0 (2104/7/2)
```


### A quick note

This document was written in a sort of free form format to get
thoughts onto "paper" so to speak. Much if it is still being refined and
is subject to change. The problems/solutions/implementations discussed are all
defined with a "broad brush" such that specific solutions and strategies can be isolated.


##[[TOC]]

  I. A Background
    1. What is Medusa?
    1. Definition of the Problem
    1. A quick summary of the past and present state of distributed
       numerical computation
      - MapReduce
    1. Current and prior efforts

  II. Value domain
    1. Lightweight
    1. Rapid prototyping integration
    1. Process level concurrency (vs. Thread level concurrency)
    1. The concept of "Affordable abstractions"
      1. Async by default
      1. Process as an abstraction
      1. Data sources as an abstraction
        1. Relational vs. Nonrelational
        1. Structured vs. Unstructured
        1. Small vs. Large
        1. Local vs. Remote
    1. Functional vs. OO for distributed computing
      - Statelessness
      - "Fit" with Mapreduce
    1. Cohesion
    1. Ecosystem convergence

  II. Implementation Domain: 
    1. Domain of the problem
    1. Service 
    1. Solutions
      a. Julia
        i. Why Julia?
        ii. Benefits and drawbacks?
          - Simplicity
          - Youth
          - The GIL (?)
      a. LightTable
    1. Client/Server implementation
      1. 
    1. 
    1. 

  III. Specification domain
    1. Patterns for distributed computing
      1. Reactor pattern for async IO?
    1. Grammar of graphics
    1. Interactive distributed 
    
  IV. Application domain
    1. Analytical processing

  IV. References

