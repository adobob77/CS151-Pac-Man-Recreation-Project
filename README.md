<pre>
# CS151-Pac-Man-Recreation-Project

PROJECT PROPOSAL

PacMan Recreation Project 

Team Members: Andrei Orlov, Ivan Gabriel Cristobal, Joseph Hawkins

Description: A recreation of the original Pac-Man[1] arcade game

Problem to Solve: Many arcade games in the past weren’t playable on modern devices, since they were only used in arcades.
Solution: Designing and creating a functioning playable arcade game, so that a user wouldn’t have to seek out an arcade to play an old arcade game.

describe assumptions / operating environments / intended usage:
Project assumes basic familiarity with arcade games and their basic mechanics.
The expected operating system is Windows 10/11.
It’s intended for users to be able to play the game. Arrow keys are used for movement control, and no other controls are required.

High-Level Description of the Solution:
-Maze: Maze object, holds positions of all characters within the maze. Controls events within the maze, mostly regarding a “game clear” state and the timed release of ghosts from the center “jail”.
-PacMan: Player character. Moves around the maze, and is intended to collect all pellets and avoid ghosts.
-Ghost (abstract): Abstract class intended to be a blueprint for unique ghost ai
	-Inky: Follows PacMan directly, goes to the top-right corner when scattering.
	-Blinky: Targets a specific pellet in front of PacMan, the pellet is double the distance from Inky to Pinky’s target, from PacMan. Moves to the bottom-right corner when scattering.
	-Pinky: Targets a pellet two pellet’s distance in front of PacMan. Moves to the top-left corner when scattering.
	-Clyde: Follows PacMan directly, but scatters when within an 8-pellet radius. Scatters to bottom-left corner.
-Pellet: Point object. Stationary within the maze, disappears upon contact with PacMan. All of them must be collected before the game is complete.
	-Power Pellet: Same as the regular pellet, but “powers up” PacMan when collected. Ghosts are slowed, scatter AI is activated, and PacMan gains the ability to eat ghosts for 10 seconds.
	-Point Item: Extra point item occasionally spawns in PacMan’s starting position, which gives some extra points when collected. Not necessary for a game clear.
	-Fruit: Point object. Stationary under the ghost case, appears once every few minutes, disappears upon contact with Pac-Man. Optional.

Functionality:
Remake the character sprites and mazes from original pacman
Implement the movement mechanics for the ghost and packman, so they can collide , and path find
Design a UI to control packman and display info for the game

Operations
	Andrei: Ghost AI, Maze foundation (coordinate system)
	Ivan: Unit Interface
	Joseph: Pacman movement or UI

References:
	[1]: https://en.wikipedia.org/wiki/Pac-Man
</pre>
