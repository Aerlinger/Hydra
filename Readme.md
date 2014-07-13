# Hydra

A lightweight paradigm for Distributed Computing


##### Anthony Erlinger
######  v0.0.0 (2104/7/2)


Hydra is a dynamic, lightweight paradigm for developing massively
parallel algorithms. At a high level, Hydra


#### A quick note

This document was written in a sort of free form format to get
thoughts onto "paper" so to speak. Much if it is still being refined and
is subject to change. The problems/solutions/implementations discussed are all
defined with a "broad brush" such that specific solutions and strategies can be isolated.


##TOC

  I. A Background
    1. What is Hydra?
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
        1. 
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


# Motivation


Bridge the gap between the development and deployment of massively parallel algorithms
and deploying them on a virtual cluster of machines. Conventional tools
used for 

Modern datasets are often too large to practically handle on a single
machine. 

R, Excel, Matlab, and Python (henceforth to be referred to as 'REMP')
are among the most popular:wq



# Why?

As the volume of data grow at an exponential rate every year,
there has been an increasing demand for distributed computation. The
current de-facto platform for processing 

 - An algorithm is an abstraction. It should be testable and able to be
developed on a single machine or a cluster. 


# The problem

The design and deployment of distributed algorithms is becoming
increasingly complex as the size of data grow. Existing solutions, such
as Hadoop and Storm, are powerful and flexible at scale but are
difficult to configure, test, deploy. Furthermore, such technologies are
beholden to old methods and techniques of development (Ex. Java, XML). 

# Interoperability between small and large data.

At present, data analysis is generally performed in two distinct steps.
First,   

  - Decouple an algorithm's implementation from the data it processes.
    1. Design and test an algorithm in a local environment on a local
machine using a subset of the overall data to be processed.
    2. Simulate a distributed environment locally through multiple
processes running in parallel. (Something like a reactor pattern [REF]).
Processes are an abstraction, it doesn't matter if they run on a single
machine or across a network.

  - Bridge the gap between tools used for data analysis at small scale
(R, IPython, Excel, Matlab) and those used at massive scale (Hadoop,
Storm, etc.)
    - How? An algorithms is an abstraction. Decouple the implementation
of an algorithm from the data it acts on. Why should separate toolsets
be used 

##Monetization opportunity:
  - Open source software
  - Platform as a service
  - 


I. Data analysis and exploration

  a. R
  b. E
  a. Python/IPython
  c. Matlab

I. Data analysis at scale
  a. Hadoop

Acronym: REMP (R Excel Matlab Perl)
