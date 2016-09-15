# TTT-RL
Tic Tac Toe , Reinforcement Learning algorithms 
This project is practice RL methods.
There are tons of space for improvement. (eg, rotating/miroring board status) but I didn't do it due to simplicity of understanding the algorithms.

Still I'm not confident with Q Neural Network.
- what is the best MLP topology? leaky_relu or sigmoid? How many layers and neurons of hidden layer?
- what is the best board input?
- what is the best Epsilon and Alpha

I realized DQN is assumed that the most strongest A.I. but still it has so many hyper parameters to implement in reality.


# TTT Board Status
board is 9 integer list, X=1,O=-1,EMPTY=0 eg [0,1,1,-1,0,0,1,1,1]

# Random Algorithm
Just place any available position.

# Alpha Random
Slightly improved random algorithm. It searches and places win hand if any.

# Montecalro
- Simulates n times game with alpha-random policy games for each available pos. 
- calculates the win cases of each available pos, and picks the most won hand.

If N is more than 150, it is almost perfect brain.

# Q-Learning
Q(s,a)= previous Q(s,a) + alpha (reward+gamma*maxQ(s',a') )
Reward:WIN=1, LOSE=-1, DRAW=0 , and plyaing hand reward is 0

It is perfect gamer... Human never win.

# Q Neural Network
MLP:9-162-162-9 , leaky_relu
Input:board
Output:scores of each action
Training: update is same as Q-Learning. only amend the parameter of action index.

This link is very useful.
http://outlace.com/Reinforcement-Learning-Part-3/
