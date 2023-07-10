
## Introduction

This project is the final project of my *Basic Programming*  course. The goal was to make a clone of the famous *Pac-Man* arcade game.  

### Implemented Features :

- Randomly Generated Map

- Custom Colors

- Leader Board

- Adding an Easter Egg to the game 

## Maze generation
The maze is randomly generated based on the dimensions that the user enters using *DFS* algorithm. It's implemented using a class named `maze`. Besides that,
the C++ `random` library was used as well. Here is the code snippet:  

```c++

random_device rd;

mt19937  eng(rd());

uniform_int_distribution<mt19937::result_type> random(1,4);

Orientation random_direction =  Orientation(random(eng));

```

  

## Ghosts behavior

The Ghosts are able to track the player through using a BFS algorithm that finds the path to Pac-Man or a block near it , this is done for sake of randomness in ghost behavior, otherwise they would all chose the same path and stick together, only Blinky the red ghost tracking the exact position of the player and is the most aggressive.

  

the algorithm uses a vector to queue / (push_back) and dequeue / (pop_back) the cells of the map to search for the Pac-Man location. since every time Pac-Man moves the coordination of Pac-Man only changes by one cell updating the BFS algorithm doesn't really matter because the ghost will be in the general direction of the Pac-Man.

  

## Graphics

  

All the visuals are either ascii art that I build myself or copied from google and changed a bit to suit the rest of the game.

  

and the Unicode are from the font Noto Sans Canadian Aboriginal.

  

## Saving Data

  

In order to save your progress mid game and keep track of the scores in leader board and compete with people who played before you I had to write everything in a **.txt** file and read it when needed to construct the leader board or map.

  

## How To Run The Code
It's worthy of mention that the code uses libraries like `windows.h` which is only available in *Windows* operating system, so be sure to run the code on an appropriate device.
  

## Resources

  

[BFS algorithm](https://www.youtube.com/watch?v=KiCBXu4P-2Y)

  

[Maze generation](https://www.youtube.com/watch?v=Y37-gB83HKE)

  

[Understanding Ghosts behavior](https://gameinternals.com/understanding-pac-man-ghost-behavior)

  

[Some inspirations](https://www.youtube.com/watch?v=vC0d1rDmPBs)

  

[Noto Sans Canadian Aboriginal Font](https://fonts.google.com/noto/specimen/Noto+Sans+Canadian+Aboriginal)

  

## Credits
Course Instructor: [Dr. Kheradpisheh](https://www.linkedin.com/in/saeed-reza-kheradpisheh-7a0b18155/)
Project mentor: [Mobin Nesari](https://www.linkedin.com/in/mobin-nesari/)

----
#### Winter 2022-2023
