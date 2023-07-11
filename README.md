## Introduction
The final project of my *Basic Programming* course. The goal was to make a clone of the famous *Pac-Man* arcade game using C++.

## Implemented Features :
- Randomly Generated Map
- Custom Colors
- Leader Board
-  Easter Eggs

## The  Code In A Nutshell
### How the game works
The maze is randomly generated (based on the dimensions that the user enters) using *DFS* algorithm.
Ghosts are able to track the player through using a *BFS* algorithm that finds the path to Pac-Man or a block near it, this is done for sake of randomness in their behavior, otherwise they would all choose the same path and stick together!
The algorithm uses a *vector* to *queue* / *push_back* and *dequeue* / *pop_back* the cells of the map to search for the location of Pac-Man. Since every time Pac-Man moves the coordinations of it only change by one cell updating the *BFS* algorithm doesn't really matter because the ghost will be in the general direction of Pac-Man.
So to conclude, only the red ghost -*Blinky*- tracks the exact position of Pac-Man and is the most aggressive one among the 3 ghosts! The other two aim for 2 blocks ahead or 2 blocks behind Pac-Man.
### Graphics
All the visuals are either ASCII art that were either drawn or copied from google and changed a bit to suit the rest of the game.
I shall mention that the Unicode used is *Noto Sans Canadian Aboriginal*.
### Saving Data
The 3 files `scoreBorad.txt`, `maze.txt` and `creature.txt` are used to store the data of the game. `scoreBorad.txt` stores the 10 highest records of players, `maze.txt` and `creature.txt` are used as checkpoints, so you can save your progress and continue playing later!

## How To Run The Code
It's worthy of mention that the code uses libraries like `windows.h` which is only available in *Windows* operating system, so be sure to run the code on an appropriate device.
When your environment is ready, either clone the repo or download it as a zip file. Now you can either run the code manually through opening the `pacman.cpp` file or just run the ‍‍‍‍‍‍‍‍‍‍‍‍‍‍`pacpac.exe` file. **Be Careful** that the GUI is designed using Unicode characters, so use an appropriate terminal that shows them correctly (something like Msys2 or the built-in terminal of *VScode* worked for me).
 
## Resources
[BFS algorithm](https://www.youtube.com/watch?v=KiCBXu4P-2Y)<br>
[Maze generation](https://www.youtube.com/watch?v=Y37-gB83HKE)<br>
[Understanding Ghosts behavior](https://gameinternals.com/understanding-pac-man-ghost-behavior)<br>
[Some inspirations](https://www.youtube.com/watch?v=vC0d1rDmPBs)<br>
[Noto Sans Canadian Aboriginal Font](https://fonts.google.com/noto/specimen/Noto+Sans+Canadian+Aboriginal)
## Credits
Course Instructor: [Dr. Kheradpisheh](https://www.linkedin.com/in/saeed-reza-kheradpisheh-7a0b18155/) <br>
Project Mentor: [Mobin Nesari](https://www.linkedin.com/in/mobin-nesari/)<br>
My teammate: [Farid Karimi](https://www.linkedin.com/in/farid-kmi/)
