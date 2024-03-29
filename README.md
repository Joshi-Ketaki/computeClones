# Detect computation code clones between applications.

## Code Clones:
To improve programmability and find opportunities for computation optimization at the application code level, it is essential to analyze the source code of the application. We look at code clone detection in order to accomplish this. Code clones are computational patterns that are similar or identical. Finding code clones opens up possibilities for scalability, code reuse, and enhanced application understanding

1. Enhanced programmability: When application developers reuse code from libraries that have already been extensively optimized, they save time and effort by not having to rewrite code or investigate optimizations.

2. Enhanced application understanding and scalability: Additionally building complex computational modules by reusing smaller modules increases efficiency of application understanding and enables rapid development of newer application modules. This is especially critical in domains such as cognitive sciences or AI/ML model development which involve complex computations. This provides the application developer or domain expert the opportunity to experiment and understand newer applications rather than investing time in building its components.

This is critical for ensuring programmability, improving understanding of newer domain applications and ease of adaptation to emerging applications, especially for domain experts like neuroscientists. To demonstrate this we develop a tool to identify code clones in cognitive models. 

## Design: 
Compared to existing methods of source-code text based or semantic clone detection, our Intermediate Representation (IR) based code clone detection provides information true to the control and data flow of the computation in the model and is independent of source language constructs. It is therefore, useful in different application domains. Compared to existing methods which look at program dependency graphs built from pre-processing semantic information of source language constructs, we encourage the use of program dependency graph built at the IR level within the compiler itself. 

## Applications used for Testing:
Neuroscience research uses cognitive brain modelling to understand and analyze underlying psychological processes for human cognition such as attention allocation, perception dynamics and decision making. These are essentially complex mathematical computations and can be modularized into commonly occurring operations. These are perfect candidates for code clone study as they provide an opportunity to exhibit code reuse as means to simplify understanding of newer cognitive models. The tool we offer for detecting code clones assists in identifying identical operations between models. The models are available in the test directory.

## Building the Tool:
Dependencies:
1. Working LLVM compiler build and build system (e.g. `Make`)
2. `Cmake`

Run the following command (assuming `Make` is the default build system):
`cmake .. && make`
This command will generate and run the build files. An `clone-checker` executable will be created in the project root directory.

## Running the Tool:
`clone-checker` can be run in the follwing manner:
`clone-checker function1 file1.ll function2 file2.ll` 
where file1.ll is the intermediate representation file that has function1 and file2.ll is the intermediate representation file that has function2. The files are the intermediate representation dumps as we perform clone detection that is independent of the source language.

## Availibility of The Tool:
[1] This tool was developed as part of work for the following paper: 
Ján Veselý, Raghavendra Pradyumna Pothukuchi, Ketaki Joshi, Samyak Gupta, Jonathan D. Cohen, and Abhishek Bhattacharjee. 2022. [Distill: domain-specific compilation for cognitive models.](https://dl.acm.org/doi/abs/10.1109/CGO53902.2022.9741278) In Proceedings of the 20th IEEE/ACM International Symposium on Code Generation and Optimization (CGO '22). IEEE Press, 301–312. https://doi.org/10.1109/CGO53902.2022.9741278

[2] The tool is now a part of [Psyneulink](https://princetonuniversity.github.io/PsyNeuLink/),which is a state-of-art
open source cognitive modelling environment.
