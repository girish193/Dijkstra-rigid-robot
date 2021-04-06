# Dijkstra-rigid-robot

## Run Code
Open the file "Mobile Robot (Dijkstra).py" in an IDE (Spyder, VS Code etc) of your choice. Enter valid input such that point does not lie in obstacle space or outside of workspace. For invalid inputs it exits with invalid input prompt. The video visualization can be found in 'Mobile Robot Visualization.mp4'.

## Description
This code aims at implementing Dijkstra algorithm for a point robot to solve a given map. All the nodes corresponding with different points (x,y) on the map are explored until a goal is found.

## Dependencies
python -version 3
numpy
sys
matplotlib
time

## Function Descriptions

### 1) workspace_check
In this functiom the given value is checked to see if it lies in the workspace.

### 2) obstacle_space
In this function the given value is checked against obstacles and true is returned if it lies outside obstacle space and also takes into consideration the clearance needed for the mobile robot. Obstacles which are given are C shaped polygon, rounded rectangle, ellipse, circle and polygon.

### 3) dijkstra
In this function the initial input values are taken and action sets is called and top, topleft, top right, bottom left, bottom right,bottom, left ,right are performed to generate next set of moves. These values are stored in a list and if thse values are not valid, they are removed. The nodes are also removed if they are present in the visited nodes. Finally, the cost of the node generated is updated only if it is less than its earlier cost. 

## NOTE :
It takes around 15 minutes (Intel(R) Core(TM) i5-9300HF CPU @ 2.4GHz, RAM = 8GB) to find optimal path using BFS for start point (0,0) and end point (400,300).

Using Matplotlib, animation is generated. Firstly, animation for node exploration is generated and followed by optimal path trajectory's animation. 150 frames for node exploration and 50 frames for solution trajectory are used as default values for the animation. The resulting animation is also stored in Point_Robot_Visualization.mp4 file.

If you get error while trying to save the animation in .mp4 file format, installation of FFMPEG may be required. [https://ffmpeg.org/download.html]
