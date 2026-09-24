# Summary
This document is the official specification for the Loom programming language. This document outlines the features, behavior, and syntax of the latest version as implemented by the [Loom Compiler](https://github.com/Tweety-Lab/Loom).

## Philosophy
The design of Loom is built around several core pillars.

1. **Developer Experience.** Loom's forefront goal is to provide an intuitive and enjoyable programming experience. Its features are designed to behave predictably and as-expected, minimizing complexity and allowing developers to focus on writing code rather than wrangling their tooling.

2. **Portability.** Loom can be easily deployed across many platforms and hardware configurations, including resource-constrained systems such as embedded environments.

3. **Safety.** Loom disregards outdated, unsafe, raw pointer models in favor of a modern smart pointer model with deep semantic integration.

These pillars are propagated from Loom's central purpose: to bridge the gap between low-level systems programming and the enjoyable developer experience typically associated with high-level languages.

## Why Not X?
There are many fantastic languages out there, and it's important to know why Loom was created when the pre-existing options seem to offer similar solutions.

### Why Not C++?
C++ is an incredibly powerful and mature language that has been an industry standard for decades. It's longevity and incredibly large ecosystem are some of it's biggest strengths. However, many of its challenges stem from its long history.

C++ was developed for a different era of computing and as such has accumulated decades of features, conventions, and legacy mechanisms that we now have modern solutions for. Older features, such as header-based inclusions and manual memory management cause issues many modern languages entirely avoid.

Modern C++ features akin to smart pointers and modules address some of these concerns. However, their adoption is slowed significantly due to C++'s lack of central tool-chain and often times the setup required to use these features is more effort than it's worth, leaving the majority of projects still relying on legacy code.