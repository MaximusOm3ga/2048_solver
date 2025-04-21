This 2048 solver uses the Q-learning algorithm to play games and iterate on itself to better improve
It is currently ready to deploy with full functionality and working mechanisms

It works on any 2048 game running on a browser. Changes to the detection grids may be required for proper functioning as well as titles of current window and parameters of game
over

To detect what number is held in each square, the grid is divided according to game tiles and each tile randomly samples 50% of the pixels to get the average rgb value that is then 
used to get the closest value of the number according to the dictionary.
The game over detection uses OCR to detect the words 'Play Again' to determine whether the current game is over. If it is, the the algorithm restarts the game and starts playing

The algorithm uses a reward system that is rewarded for each new move that it does and penalised if grid shows no changes. Each time a new max number is achieved in the grid 
the algorithm is rewarded slightly more. A significant penalty is also awarded for each game over.

Even though the program is complete and deployable, the algorithm does not perform as well due to lack of hardware resources. To train the model requires a signinfiacant number
of hours and as of now, I have only been able to provide with about 5% of that time

Note: if you want to run the model, simply use the 2048 game at: https://play2048.co/ at fullscreen and run the model. Grids are optimized for a screen resolution of 1920x1080, so 
changes to grid shape might be required