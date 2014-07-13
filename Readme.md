# Hydra

A lightweight and dynamic toolset for Distributed Computing


##### Anthony Erlinger
######  v0.0.0 (2104/7/2)


## Abstract

Hydra is a lightweight and dynamic framework built with the purpose 
of simplifying the design, development, testing, 
and deployment of large-scale distributed algorithms. This is
accomplished by providing a rich development environment focused 
on ease of integration on a local machine.


##### A quick note

> This document was written in a sort of free form format to get
> thoughts onto "paper" so to speak. Much if it is still being refined and
> is subject to change. The problems/solutions/implementations discussed are all
> defined with a "broad brush" such that specific solutions and strategies can be isolated.


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

**Summary:** Two camps for data analysis: Those that are used by people REMPE (R, Excel, Matlab,
Python, Etc.) and those that Hadoop/Mapreduce. Both of which
take a different approach for different reasons. Hadoop scales to
"arbitrarily large" datasets by splitting the work across multiple
machines (embarrassingly parallel). REMPE is much simpler, but more
flexible for small datasets. REMPE runs in a single process
(usually) within a single thread.

###### Why use a different approach for small and large scale?

REMP is limited in usefulness and utility due to
limitations in its design for handling datasets that are anything other
than very small by today's standards (hundreds of thousands to millions
of datapoints).

##### Solution: Split data across a multi-process architecture

Hadoop/Mapreduce is limited by unnecessary complexity complexity of
deployment and lack of consistency with REMP. 
oo



---

As the size and complexity of data grows exponentially every year, so does the
technology intended to process, manage and analyze said data. Modern
hardware, software, and network infrastructure have adapted to
accomodate the demand for "Big Data," yet the techniques and methods
used for large scale analysis and computation remain monolithic and
difficult to develop and use.

This is made apparent by the asymmetry in software and languages used by analysts for
processing data and the software that ultimately gets deployed in a
production environment. For instance, a data analyst spends the
majority of his/her time preprocessing and
"wrangling" a dataset on a workstation using something like R, Excel,
Matlab, Python, etc (Henceforth to be called REMPE). The limitations of
such languages and programs are reflected by their age. None of them
were ever intended to process large datasets and certainly none of them
were intended to be able to run on and certainly none of them were
indended to run in an environment on multiple machines.

To accommodate for these need, a paradigm called "Map Reduce" was
developed at Google. The most common mapreduce framework in existence
today is known as Hadoop.


For the past twenty years there has been a exponential growth in the
amount of data produced every year. In turn, there has been a variety of
technologies at the hardware, software, and infrastructural level
developed with the 

Modern datasets are often too large to be effectively processed. 
As such, a common practice is to download a small subset of the
full data and analyze it within a program on a single worstation
machine. There are several such programs regularly used for this
purpose. Most prominent amongst these data analysis programs and
languages are are R, Excel, Matlab, and Python (henceforth to be referred to as 'REMP').

Of course, a single workstation machine has neither the computing power

In practice, "Big data" algorithms are developed in a series of discrete
steps. 

  - Querying the data
  - Filtering the data
    - Outlier removal
    - Type inference and structure
    - 
  - Meta-analysis
    - Inferring the structure of the schema




# Why?

As the volume of data grow at an exponential rate every year,
there has been an increasing demand for distributed computation. The
current de-facto platform for processing 

A shift from 

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


