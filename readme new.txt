Name   - Deepak Varghese

Task 1 

Tower of Hanoi 

In hanoi_facts2 file the following part in preconds 

(smaller disk1 disk2)
(smaller disk1 disk3)
(smaller disk1 disk4)
(smaller disk1 disk5)
(smaller disk2 disk3)
(smaller disk2 disk4)
(smaller disk2 disk5)
(smaller disk3 disk4)
(smaller disk3 disk5)
(smaller disk4 disk5)

and 

(smaller disk1 A)
(smaller disk1 B)
(smaller disk1 C)
(smaller disk2 A)
(smaller disk2 B)
(smaller disk2 C)
(smaller disk3 A)
(smaller disk3 B)
(smaller disk3 C)
(smaller disk4 A)
(smaller disk4 B)
(smaller disk4 C)
(smaller disk5 A)
(smaller disk5 B)
(smaller disk5 C)

and the names of the variables 

(disk1 Object)
(disk2 Object)
(disk3 Object)
(disk4 Object)
(disk5 Object)
(A Object)
(B Object)
(C Object)

is common for the Tower of Hanoi domain as it defines all the disks and pegs and the possible scenarios that can possibly happen in that domain. These can be used for any facts file.


7 Puzzle problem 

In 7 Puzzle problem the naming of the objects 

(Tile11 Object)
(Tile12 Object)
(Tile13 Object)
(Tile21 Object)
(Tile22 Object)
(Tile23 Object)
(Tile31 Object)
(Tile32 Object)
(Tile33 Object)
(1 Object)
(2 Object)
(3 Object)
(4 Object)
(5 Object)
(6 Object)
(7 Object)

and the following part of preconds 

(adj Tile11 Tile12)
(adj Tile11 Tile21)
(adj Tile12 Tile11)
(adj Tile12 Tile13)
(adj Tile12 Tile22)
(adj Tile13 Tile12)
(adj Tile13 Tile23)
(adj Tile21 Tile11)
(adj Tile21 Tile31)
(adj Tile21 Tile22)
(adj Tile22 Tile21)
(adj Tile22 Tile23)
(adj Tile22 Tile12)
(adj Tile22 Tile32)
(adj Tile23 Tile13)
(adj Tile23 Tile22)
(adj Tile23 Tile33)
(adj Tile31 Tile21)
(adj Tile31 Tile32)
(adj Tile32 Tile31)
(adj Tile32 Tile22)
(adj Tile32 Tile33)
(adj Tile33 Tile32)
(adj Tile33 Tile23)

is common for the 7 Puzzle probelm as it defines all the tiles and the adjacencies for that domain. 

References 

1) https://github.com/arjunvekariyagithub/PDDL 
