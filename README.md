# Rubik-sCubeSolutionGenerator
This program takes in the scrambled state of your 3x3 Rubik's cube through a camera which reads the state of all six sides, then calculates the fewest steps required to completely solve the cube. The resulting answer string provided by this program is fed into an Arduino Uno R3 which rotates the servo motors asper the solution string. This code is part of a mega project consisting of a working robot that would solve the cube using -servo motors for arms- to rotate the cube as dictated by the program. 
The solving program uses OpenCV to cut up the cameras readings into a 3x3 grid and read the average colour of each grid to determine the color. This program will require some tweaking to the colour value ranges as it is set by default to my phone's camera and to the colour of my own cube. Further, after reading the colours the program calculates the fewest steps required using Kociemba's Algorithm that guarantees a solution under 20 moves of the cube.

# Installation & Working:
1. Download all the programs and files from the link: https://drive.google.com/drive/folders/1Z6nlFsSWFPV5zftUjY545VMElSgY0rdm.
2. Open and tweak the CubeSolutionGen.py python file as per your camera and cube's colours.
3. On running CubeSolutionGen.py hold the green face towards you and consider it as the base, w.r.t that read the sides in the order WHITE RED GREEN YELLOW ORANGE BLUE pressing the 'p' button on your keyboard when reading a side and confirming the colour selection by the program.
4. After reading all 6 sides the program will generate the solution string with the turns being represented in standard notation i.e. (R L U D F B being clockwise and R' L' U' D' F' B' being anti-clockwise)
