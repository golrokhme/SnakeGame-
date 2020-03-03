This is the Readme file for Snake, a game I created for my E40m lab 3b project.

General explanation: in E40m class at Stanford, we create a 8*8 LED plane where we can control the LED display using Arduino. Through the implementation of this project, We learn about serial communication of information, working with Arduino, etc. 

For my project I have used 5 * 8 blue LEDs and 3 * 8 red LEDs. 2 push buttons representing an `interfaces for 
turning left and right. 
 
The game I implemented is a very simple implementation of the famous game snake where, a snake is moving on the
blue region of my LED plane (the upper 5 * 8 region). The features I implemented for my snake game: 

-the initial state of the game is when the size of the snake is 1 LED and the snake is located at (3,3)
-The snake has 3 lives, depicted by 3 3*2 squares in the red region of my LED space
-whenever the snake hits the invisible wall (exits the range of my 5 * 8 blue LED space) 
 or the snake hits its own body, the game stops and the snake loses one life.
 (with the snake's direction being the last direction, so if user pushes the left button 
 that leads to snake turn left, if the snake hits the wall, the assumption is that the snake
 was moving towards the wall). 
-after losing a life, the game stops until the user presses the left or right button that leads to 
 the snake moving towards a new direction. 
-if the snake loses all its lives the user loses and the game goes to its inital state 
 (a size 1 snake located at (3, 3) with 3 lives) 
- The win condition happens when the snake's length is 40 and it covers all of the blure region
----In the case of winning, game ends by a wave like mov efrom upper left corner to the lower right corner
    (LEDs in each line paralel to the diameter turn on and stay on for half a second
     to depict the winning, I have coded it so when you upload the code on arguino / turn it on the first 
     time, it demonstrates how the winning looks like (the diameter wave like movement) and then goes to 
     the initial state) 

-Turning left and right : in most snake games, you have to use the 4 key arrows on the keyboard, however, 
 in my version of the game, I used two push buttons, (I followed the debounce switch instruction from the 
 lab) where the left one represents the snake turning to its left, and the right one represents the snake 
 turning to its right. Note that to play this game you have to sympathize with the snake in its turning, 
 for instance when the snake moving up (away from you) pushing the left button leads to the snake turning to 
 its left which is your left as well, but if the snake is moving down (towards you) pushing the left button 
 leads to the snake turning to its left which is your right. This makes the game somewhat fascinating and 
 challenging
-food, when the snake eats one food, or in the initial state of the game (when variable ate = true) 
 a random LED that is not on the snake's body turns on representing the food that the snake has to eat
 to grow in length. when the snake's head reaches the food, it "eats" the food, and its size increases 
 by one. 
-In the game I used the brightness feature of the LEDs by having more relative time being ON for the brighter 
LEDs in one cycle. and in this way I tried to distinguish between the snake's head and body and the food.

You can find a link to the video of me playing this cool game here:   
https://www.youtube.com/watch?v=JaVdVF7n5Ek&lc=z235gvnwgoeovf10lacdp43bp3fpag40cpot1nhfn3tw03c010c
