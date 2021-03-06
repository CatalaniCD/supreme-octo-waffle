# Introduction to Computer Problem Solving

### 1.1 | Introduction

     Computer problem solving is demanding! requires thought, careful planning, logical precision, persistence and attention to detail.
     But is also Challenging, Exiting, and satisfiying experience with considerable room for personal creativity and expression.
     Approach with this spirit and your chances of success are greatly amplified!
     
     1.1.1 | Programs and Algorithms
     - Goal of the Book : Study in depth the process of algorithm design with particular emphasis of problem solving of the task.
     - Program : A set of explicit and unambiguous instructions expressed in a programming language.
     - Input : Data provided to a program to produce the output
     - Output : Computer solution to a problem
     - Algorithm : A set of explicit and unambiguous finite steps which when carried out for a given set of initial conditions, 
     produce the corresponding output and terminate in a finite time.
     
     1.1.2 | Requirements for solving problems by computer
     - Algorithm Desing requires a "CONCIOUS DEPTH UNDESTANDING" far greater than than we are likely to encounter in almost
     any other problem-solving situation.
     - Phone Directory Problem : Only when a Data Structure is symbolically linked with an algorithm we can expect high performance.
  
### 1.2 | The Problem Solving Aspect

    """ Computer problem solving is about understanding """
    
    1.2.1 | Problem Definition Phase
    - Work out "what must be done?" rather than "how to do it?"
    - Extract from the problem statement ( often quite imprecise and maybe even ambiguous) a set of precisely defined tasks.
    
    1.2.2 | Getting Started with the problem
    - Always there are many ways to solve a problem, then is important how to decide which are fruitless and which productive
    - If goes straight to the implementations, there is a block. Here is required to work out in an implementation-independent solution.
    - Not to be concerned about detail
    - Old Computer Proberb : " the sooner you start coding your program, the longer it is going to take "
    
    1.2.3 | The use of specific examples
    - Map the specific problem to an general type of problem and try to work out the mechanism that will allow us 
    to solve this specific problem.
    - Geometrical or schematic diagrams representing certain aspects of the problem can be usefully employed in many instances
    
    1.2.4 | Similarities among problems
    - start on a problem by considering a specific example
    - bring as much experience as possible to bear the current problem
    - a good habit is to always make an effort to be aware of similarities among problems
    - the more experience, tools and techniques one can bring to bear in tackling a given problem
    - There is cases of experience blocking the discovery of a desirable and better solution to a problem
    - Have cautious reliance on past experience
    - It is usually wise, in the first instance at least, to try independently to solve the problem
    - """ Every problem must be considered on its merits """
    - Capability to methaphorically turn a problem upside down, inside out, sideways, backwards, forwards, and so on
    - Once developed this skill it shouldd be possible to get started with any problem
    
    1.2.5 | Working backwards from the solution
    - Assume that you already have the solution for the problem and then try to work backwards to the starting conditions
    - Even a guess at the solution to the problem may be enough to give us a foot hold to start on a problem
    - write down ,as we go along the solution attempt,  the various steps and explorations made
    - Technique : when we have solved a problem, conciusly reflect back on the way we went about discovering the solution
    - """ Practice is the most crucial thing of all developing problem-solving skills """
    - """ We Learn most when we invent """ J. Piaget
    
    1.2.6 | Geneal problem-solving strategies
    - General and powerful computational strategies
    - Map a problem to one of these strategies and achieve considerable computational efficiency
    - divide-and-conquer : divide the original problem into two or more subproblems and solve them more efficiently
    - applications on sorting, selection and searching
    - binary search complexity is log2 n comparisons
    - sorting complexity is reduced from n^2 to n log2 n
    - binary doubling : reverse of divide and conquer ( avoid generation of intermediate terms )
    - dynamic programming : often used when we have to build up a solution to a problem via a sequence of intermediate steps
    - optimal substructure & overlapping problems: optimal solution can built up from optimal solutions to smaller problems
    - revelevant for optimization problems / operations research
    - dp techniques : greedy search, backtracking, brach and bound
    - minimum amount of resources consumption on exploring solutions that have been stablished to be suboptimal
    
### 1.3 | Top-Down Design

     """ primary goal in computer problem solving : design an algorithm which is capable of being implemented as a 
     correct and efficient computer program """
     
     - aspects of problem-solving and algorithm design
     - define problem to be solved, vague idea of how to solve it, bring to bear powerful techiniques for designing algorithms
     
     """ successful algorithm design lies in being able to manage the inherent complexity of problems """
     
     - people is limited to focus one problem at time and a very limited span of logic or instructions
     - algorithm desing technique to overcome focus limitations : top-down design / stepwise refinement
     - top-down desing : 
          - from a vague outline to a precisely defined algorithms and program implementation
          - way of handling inherent logical complexity and details
          - build the solution in a stepwise fashion
          - encounter specific and complex implementation details after done sufficient groundwork on the overall problem structure
    
    1.3.1 | Breaking a problem into sub-problems
    - from problem-solving groundwork to the broadest solution outline
    - single statement or a set of statements
    - top-down design : take the general statements about the solution, one at a time, and break them down into a set of precise subtasks.
    - preservation of the overall structure in the solution, comprehensible algorithm, solution proof of correctness 
    - breakdown process stops when the subtask can be implemented as program statements
    - Most algorithms : 2 or 3 levels, more for large projects
    - smooth interface between stepwise refined algorithm and the final program implementation
    - keep implementation task as simple as possible
    
    1.3.2 | Choice of a suitable data structure
    - decision when formulating computer solutions : choice of proper data structure
    - programs operate on data, the way the data is organized impacts on every aspect of final solution
    - proper data structures leads to simple, transparent and efficient implementations
    - improper data structure leads to clumsy, inefficient and difficult implementations
    - data structure selection can be refined as the algorithm is developed
    - data structures and algorithms are usually intimately linked
    - each problem must be considered on its merits
    - Questions to decide about a data structure :
          1. How can intermediate the results be arranged to allow fast access to information that will reduce the amount 
          of computation required ar a later stage ?
          2. Can the data structure be easily searched ?
          3. Can the data structure be easily updated ?
          4. Does the data structure provide a way of recovering an earlier state in computation ?
          5. Does the data structure involve excessive use of storage ?
          6. Is it possible to impose some data structure on a problem that is not initially apparent ?
          7. Can the problem be formulated in terms of one of the common data structures (e.g. array, set, queue, stack, tree, graph, list) ?

    1.3.3 | Construction of loops
    - implementation subtasks lead to iterative constructs and structures that are conditionally executed
    - essetial structure for loops : 
         - initial conditions before loop begins
         - invariant relation after each iteration
         - loop termination conditions
    
    1.3.4 | Establishing initial conditions for loops
    - stablish initial conditions for a loop
    - set the loop variables in order to solve the smallest problem associated with the loop
    - typically the iterations are 0 <= i <= n
    - the smallest problem usually match i == 0 or i == 1
    
    1.3.5 | Finding the iterative construct
    - once solved the smallest problem, extend to next smallest problem
    - the solution for the next smallest problem can be built from the smallest problem
    - loop construction is simmilar to mathematical induction
    
    1.3.6 | Termination of loops
    - in genearl loop termination conditions are dictated by the nature of the problem
    - in 'for' loop iteration terminates after n steps
    - in 'while' loop iteration may terminate when a conditional expression becomes false, cannot determine number of iterations; no guarantee of loop termination
    - monotonically increasing / decreasing of x
    - 'while' termination by forcing condition for loop continuation to become false : one or more tests possible
          - case of while index if array[i-1] < [i],  monotonically increase i, else break
    
### 1.4 | Implementation of Algorithms

    - The Implementation of algorithms designed in a top-down fashion should ve an almost mechanical process
     * Top-Bottom Rule
     - If an algorithm has been properly designed the path of execution should flow in a straight line from top to bottom
     - Programs implemented this way are easier to understand, modifty and debug
     
    1.4.1 | Use of procedures to emphasize the modularity
    - Modalirize the program, improve development and readability
    - Follow top-down design
    - Allow us to implement a set of independent procedures to perform specific and well-defined tasks
    - Use of dummy procedures to create the program flow
    
    1.4.2 | Choice of variable names
    - Choose appropiate variable and constant names
    - Program becomes self-documenting
    - Helpful : clear definition of all variables and constants at the start of the program
    1.4.3 | Documentation of programs
    - Associate a brief and accurate comment at procedure's begin
    - Add information that the program shows to the user during execution
    - Document for people unfamiliar with the process and input requirements
    - Avoid ambiguos specifications
    - Catch inputs and inform it in an appropiate manner
    
    1.4.4 | Debugging of programs
    - Detecting logical errors by adding print statements in strategic points in the computation
    - Simplest way to implement debugging is to have a boolean varaible (e.g _debug_) which is set to true when the verbose debugging output for the program is required
    - Best practice : Work the program through by hand before ever attempting to execute it
    - This will catch most errors
    - Check each module or isolated task for typical input conditions
    - Use of 2-dim table consisting of two steps executed against all the variables and tests used in the section of the program in consideration
    - Update each variable or test value
    - Ensure to follow a stright line along the path of execution
    - Rule : When debugging avoid assumptions
    
    1.4.5 | Program Testing
    - Test whether or not a program will handle all variations of the problem it was designed
    - Will it cope the limiting or unusual cases ? (Boundary cases)
    - Test : Solve the smallest problem possible
    - It is often not possible or necessary to write programs that handle all input conditions
    - Wherever possible programs should be accompanied by input or output assertions
    - It is not always practical to implement programs that can handle all possible input conditions
    - Build inte a program mechanisms that allow it to gracefully and informatively respond to the user when it receives input conditions it was not designed to handle
    - Design algorithms to be general and handle a whole class of problems rather than just one specific case
    - Use fixed constants only when necessary
    
### 1.5 | Program Verification

    - More than half of effort and resources are spent in correcting errors and modifications
    - Creation of clearly written code at the time of program development
    - Top-down design can serve as very useful aid to write readable and understandable programs
    - Application of a systematic procedure to determine program correctness
    - Program verification : application of mathematical proof techniques to establish that the output from arbitrary inputs is in accord with formally defined output specifications
    - Best Practice : develop the proof in a top-down fashion along with the top-down development
    
    1.5.1 | Computer model for program execution
    - Program verification requires test cases, that is { input, ouput } pairs
    - Execution path that follows for a given input conditions
    - The written implementation may have whole set of execution paths
    - Each instruction change the computation state, or make a test on the state
    - The tests are used to branch the sequential flow of execution
    - This model for program execution provides us with a foundation to construct correct proofs of algotihms
    
    1.5.2 | Input and output assertions
    - Provide specifications about the inputs and ouputs
    - Input assertions, output assertions
    - Assertions are constraints to the values 
    
    1.5.3 | Implications and simbolic execution
    - Conditional applied to input, { if input not in constrainst, continue }
    - Symbolic execution refers to the sets used as input, output
    - Add intermediate assertions to IO
    - Best Practices : Use straight line segment, branching segments, loop segments
    - VC(A-B) : Verification segment from A to B
    
    1.5.4 | Verification of straight-line program segments
    - Evaluate variables at the end of the segment
    
    1.5.5 | Verification of program segments with branches
    - Evaluate {True, False} branching
    - Assertion for 'True', Assertion for 'False'
    
    1.5.6 | Verification of program segments with loops
    - Assertion : Loop invariant, property that captures the progressive computational role fo the loop, and remain true always
    - Show that the loop invariant is true initially : VC(A-B)
    - Precondition : use input assertion
    - Show that the loop invariant is false after the loop execution
    - Postcondition : use output assertion
    
    1.5.7 | Verification of program segments that employ arrays
    - Apply 1.5.6
    
    1.5.8 | Proof of termination
    - Loop Termination
    - Property of a data that guarantees termination : Sentinel
    - Terminate from an Epsilon Expression. Expression that includes variables modified in the loop
    - Termination conditions : TC(A), TC(B)
    
### 1.6 | Efficiency of algorithms

    - Tied to design, implementation, and analysis of algorithms
    - Every algorithm may use computer resources to complete a task
    - Resources more relevant in relation to efficiency are central processor time (CPU time) and internal memory.
    - Desirable to design economic algorithms (CPU and Memory)
    - Design Habits, Inherent complexity of the Problem.
    - Each problem has its own characteristics, demand specific responses
  
    1.6.1 | Redundant computations
    - Redundant computations or unnecessary storage
    - Serious when embedded within a loop
    - Most common mistake in loops, recalculate part of the expression that remains constant in the loop
    - Eliminate redundancies
    
    1.6.2 | Referencing array elements
    
    1.6.3 | Inneficiency due to late termination
    1.6.4 | Early detection of desired output conditions
    1.6.5 | Trading storage for efficiency gains
### 1.7 | The analysis of Algorithms
    1.7.1 | Computational Complexity
    1.7.2 | The order notation
    1.7.3 | Worst and average case notation
    1.7.4 | Probabilistic avarage case notation
    
