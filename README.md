Detect computation clones in two programs.

This work was done as part of the research for Distill: Domain-specific compilation for cognitive models (https://ieeexplore.ieee.org/document/9741278)
We detect computation clones between two different computation flows depicting cognitive models. This helps to identify if a two cognitive models (or any two computations) are similar 
to each other. If yes, it helps in the analysis of comparing computation costs for either and using the less costly one.
We build this using LLVM's function comparator framework in our algorithm.
