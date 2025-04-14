This program solves mazes, finding the fastest(s) path(s) to the exit.


To build this project, clone the repository using git clone, then run make to compile the project.


Next, use ./amazed < tests/files/(name of the file you want to test).


If you want to create maps, use laby_gen.pl

usage of the generator : 

- laby_gen.pl size density nb_of_robots

- Size is the number of rooms and density the percentage of probability of connexions between rooms


You should have an output like that :


#number_of_robots

3

#rooms

##start

0 1 0

##end

1 13 0

2 5 0

3 9 0

#tunnels

0-2

2-3

3-1

#moves

P1-2 

P1-3 P2-2 

P1-1 P2-3 P3-2 

P2-1 P3-3 

P3-1 

#moves shows the moves of the robots, P[number] is the name of the robot (P1 for robot 1), and -[variable] is the name of the room where the robot goes (it can be a string, a number, a float...).


So, P1-2 means that the robot 1 goes to the room 2, P1-3 P2-2 means that the robot 1 goes to the room 3 and the robot 2 goes to the room 2, etc.


Feel free to add your own tests, wich you can run using make tests for functionnal tests and make test_run for unit tests.


