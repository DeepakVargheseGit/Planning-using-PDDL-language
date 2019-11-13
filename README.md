# Planning-using-PDDL-language

Designed appropriate descriptions of facts, actions, and goals, using the PDDL language, for two planning problems: the Tower of Hanoi problem, and the 7-puzzle problem (a variation of the 8-puzzle problem where two squares are clear instead of one). Used descriptions as inputs to a Graphplan implementation. 

Compiling and Running the Software
The Graphplan software can be downloaded from graphplan.zip. See the README file in that package for additional information. To compile the software on omega, unzip the directory, and, from that directory, type

make graphplan

Once the program compiles, it can be invoked from the commandline as follows:

graphplan -o [operators_file] -f [facts_file]

For example:

graphplan -o block_ops.txt -f block_facts3.txt

1) Argument operators_file specifies the location of a text file containing definitions of actions. For example, see block_ops.txt for definitions of actions appropriate for the blocks world.
2) Argument facts_file specifies the location of a text file containing definitions of facts about the environment, including objects (and types for those objects), general predicates that are always true, initial state description, and goal description. For example, see block_facts2.txt, block_facts3.txt, and block_facts4.txt for example fact descriptions for the blocks world.

Once you start running the software, it will ask you three questions. Just hit enter for each question, so as to use the default settings. If your descriptions of actions and facts are correct, the program will print out a plan achieving the stated goal.

Note that the preconds in each fact file will contain both statements that are always true in that domain (i.e., in the Tower of Hanoi domain or the 7-puzzle domain), and statements that simply describe the initial state for that specific planning problem. In addition to the facts files for the specific planning problems you are given, you will have to create a separate text file that includes all the statements that must be present in ANY facts file for that domain.


Tower of Hanoi Description

A description of the Tower of Hanoi domain can be found at Wikipedia. In all problems that your program will be tested with there will be five discs (called disk1, disk2, disk3, disk4, disk5) and three pegs (called A, B, C). In all your facts files you will have to include both a common part (defining objects and relations among objects) and a plan-specific part (describing the initial state and goal for each plan). Note that some of the five disks may not appear in some of the planning problems.

The two planning problems you have to solve are:

Problem 1

initial state:
(on disk1 disk2)
(on disk2 A) 
(clear disk1)
(clear B)
(clear C) 

goal:
(on disk1 B)
(on disk2 C)

Problem 2

initial state:
(on disk1 disk2) 
(on disk2 disk3)
(on disk3 disk4)
(on disk4 disk5)
(on disk5 C) 
(clear disk1) 
(clear A) 
(clear B)

goal:
(on disk1 disk2) 
(on disk2 disk3)
(on disk3 disk4)
(on disk4 disk5)
(on disk5 A) 


7-puzzle Description

7-puzzle is like 8-puzzle, except that there are only pieces numbered from 1 to 7 (not from 1 to 8), and there are two clear squares on the board. At any move, we can move a numbered piece to an adjacent clear square.
The two planning problems you have to solve are (X indicates a clear square):

Problem 1

initial state:
123
X56
4X7

goal:
123
456
7XX


Problem 2

initial state:
XX7
654
321

goal:
123
456
7XX



Task 2 

Two adults and two children are on the left side of the river. Each adult weighs 150 pounds. Each child has half the weight of an adult, so each child weighs 75 pounds. They all want to cross to the right side of the river. However, the only means of transportation they can use is a boat, and the boat can carry a maximum of 150 pounds. Thus, the boat can carry one adult without children, or one child, or two children. Any adult or child can operate the boat, but the boat cannot be operated without having at least one person on the boat. The goal is to come up with a plan for moving everyone from the left side to the right side using multiple boat trips.

Define appropriate actions for this planning problem, in the PDDL language. For each action, provide a name, arguments, preconditions, and effects. Also, describe the initial state and the goal, using PDDL.



Task 3 

We have state descriptions and action definitions written following the conventions used in the graphplan software of Task 1. One of the actions is defined as follows:

(operator
 aaa
 (params
 (<b> ttt1) (<c> ttt1))
 (preconds
 (ppp1 <b> <c>) (ppp2 <b>) (ppp3 <c>))
 (effects
 (eee1 <b> <c>) (eee2 <b>) (del eee2 <c>) (del eee3 <c>)))
 
Suppose we are at a state S1 described as follows (again, using graphplan syntax):

(A ttt1)
(B ttt1)
(C ttt1)
(ppp1 B C)
(ppp2 A)
(ppp2 B)
(ppp3 C)
(eee1 A C)
(eee2 C)
(eee3 C)
(eee3 A)

What is the state resulting from applying action aaa(B,C) to S1? Give a complete specification. 

Task 4 

Suppose that we are using PDDL to describe facts and actions in a certain world called JUNGLE. In the JUNGLE world there are 4 predicates, each predicate takes at most 3 arguments, and there are 5 constants. Give a reasonably tight bound on the number of unique states in the JUNGLE world. Justify your bound.

