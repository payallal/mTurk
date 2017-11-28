# Testing Temporal Discounting on mTurk


![Preview](https://github.com/payallal/temporal_discounting/blob/master/Assets/Task.gif)

Purpose
-------
Psychologists and economists, among other researchers study temporal discounting to better understand the tendency of people to change the way they value rewards depending on the time in which they expect to receive the reward. I initially came up with this simple program built using HTML, CSS and Javascript to run an experiment with Synergy Labs, a psychology research lab at Yale-NUS that studies love. Using this program, we test temporal discounting and its correlation to people's behavior in romantic relationships via Amazon Mechanical Turk. You are free to use this open source tool for experiments and any other non commercial purposes. 

How to use this software
------------------
You can use this software in one of two ways:
1. Download onto your computer (git pull) and use it during lab studies.
2. Upload to server and put it up online for use during online studies. You can find an example of how the tool looks online [here](https://payallal.github.io/mTurk/). However, I discourage you from using this URL for your experiments in case I decide to move it to another URL in the middle of your experiment (I wouldn't do this on purpose, but it could happen given that I don't actively track if that URL is being used). 

Walk through
--------
Here's how the tool works. 
1. Participants see an instructions page which gives them details on the task. 
![alt text](https://github.com/payallal/temporal_discounting/blob/master/Assets/Instructions.png)
2. When they click continue, the task begins - participants go through 6 sets wherein they're given choices between different amounts of money that they'll receive at different points of time in the future. 
3. The first set asks participants whether they'd rather have an x amount of money now, or $10 in 2 months. The x amount adjusts itself as the participant selects options. Each sets consists of 5 options. After the fifth option, the participant proceeds to the next set wherein s/he is given the choice to choose an x amount of money now or $10 in 3 months. The number of months increases with each set until it reaches 6. 
![Preview](https://github.com/payallal/temporal_discounting/blob/master/Assets/Task.gif)
4. Once the player is done with the last set, a thank you page shows up which gives the participant a code to save. This code is valuable information - it not only ensures that your participant completed the task, it contains the information of the options your participant chose during the task. Each number represents the choice your participant clicked on as they went through the task. In the image below for example, your participant selected 10 as his first choice when asked if he's rather have $5 now or $10 in 2 months. Then, when the choice changed (presumably to offer his $7.5 now or $10 in 2 months), he again selected $10. Note that after every 5 values in the array, the participant is in a new set. So the sixth value in the image below for example is your participants' answer to 'would you have $5 now or $10 in 3 months?'. Play the game yourself a few times to better understand the choices these numbers are conveying. 
![alt text](https://github.com/payallal/temporal_discounting/blob/master/Assets/Thanks.png)

Technical Instructions
----------
Once you have this downloaded on your computer or running on your server, start by calling or clicking the index.html file. This is the file which opens the instructions page. If you'd like to override the instructions and go straight to the task, call or click task.html. You can also make modifications to the task. 
1. Instructions: To modify instructions, look under the 'paragraph' div in index.html
2. Style: Instructions.css contains all the styling of the instructions (or index.html) page, and task.css contains the styling of the main task. 
3. Values provided during the task: The game starts with the option of $5 vs $10. You can change this by modifying the variables in task.html. However, I would discourage you from trying to do this unless you're experience with JavaScript. 
