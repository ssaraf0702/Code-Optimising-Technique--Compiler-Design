# Compiler Optimising Techniques
Different optimisation techniques implemented

## INTRODUCTION
The code optimization in the synthesis phase is a program transformation technique, which tries to improve the intermediate code by making it consume fewer resources (i.e. CPU, Memory) so that faster-running machine code will result. 

## HYPOTHESIS
Compiler optimizing process should meet the following objectives :
* The optimization must be correct, it must not, in any way, change the meaning of the program.
* Optimization should increase the speed and performance of the program.
* The compilation time must be kept reasonable.
* The optimization process should not delay the overall compiling process.
## APPROACH

### Machine Independent Optimization 
* This code optimization phase attempts to improve the intermediate code to get a better target code as the output. The part of the intermediate code which is transformed here does not involve any CPU registers or absolute memory locations.
* Creating Basic blocks from the intermediate code by marking leaders across the code.
* Building Control Flow Graphs and performing Live Variable Analysis to resolve liveness.


### INPUT
A text file containing 3 address intermediate code.
## TYPES OF OPTIMISATIONS DONE
#### Constant Folding
Expressions with constant operands can be evaluated at compile time, thus improving run-time performance and reducing code size by avoiding evaluation at compile-time. In the code fragment below, the expression (3 + 5) can be evaluated at compile time and replaced with the constant 8.
#### Constant Propagation
Constants assigned to a variable can be propagated through the flow graph and substituted at the use of the variable.
#### Common Subexpression Elimination
An expression is a Common Subexpression (CSE) if the expression was previously computed and the values of the operands have not changed since the previous computation. Recomputing the expression can be eliminated by using the value of the previous computation.
#### Dead Code Elimination
Code that is unreachable or that does not affect the program (e.g. dead stores) can be eliminated.
#### Loop Unrolling
Loop overhead can be reduced by reducing the number of iterations and replicating the body of the loop.

### OUTPUT
Optimised intermediate code in 3 address code format.

