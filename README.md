# AiBenchmarkToolkit
A toolkit for benchmarking core mathematics and AI implementations across hardware and libraries.

This is a Work in Progress [WIP]!

This is a proof of concept, first implementation of the idea of benchmarking AI implementations. My hope is that after contributions this will become a valuable resource for future AI research.

There are still a lot of TODOs to be implemented for the proof-of-concept. My plan is to create an initial proof-of-concept based on previous research work as a starting point for this project. I am hoping to also gauge the interest in such a project.

This idea is inspired by the work of Dave Plummer and his Primes benchmark used to compare programming language performance computing prime numbers. The repository is located here: https://github.com/PlummersSoftwareLLC/Primes

## Goals
1. Efficiency (Implementations that run faster are also more resource efficient)
2. Reference Implementations (Using data can help determine which implementation is best for a specific scenario)
3. Approximate Implementations (Using data to understand trade-offs in implementations which are more efficient but with trade-offs)
4. Hardware Selection (Using data to determine what kinds of hardware selection is appropriate for a specific scenario)

There isn't necessarily a 'best' solution when selecting hardware, frameworks, and programming languages when wanting to solve AI and machine learning problems. Rather, if we had a set of reference implementations and comparative results including data on induced error and cost per implementation.

# TODO:
- [] Makefile - To help orchestrate things
- [] Initial Python implementations of algebraic basics
  - [] Newton's Method
  - [] Test data
  - [] Dot product
  - [] Cross product
  - [] Opening data
  - [] List more benchmarks
  - [] Basic NN
  - [] Perceptron
  - [] Interpolation
  - [] Integration
  - [] Differentiation
  - [] RNG generation
  - [] Hard Approximations (Lookup tables etc ...)
  - [] CUDA (CuDF and others)
- [] Aim of this research
- [] Contribution Policies
- [] Security Policies
- [] Artefacts in actions
- [] Profilers
  - [] PyTorch
  - [] Pandas.profile
  - [] Pandas.line_profile
- [] References

# Useful Links
- https://www.answer.ai/posts/2024-07-11--gpu-cpp.html
