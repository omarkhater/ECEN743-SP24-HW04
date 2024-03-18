# ECEN743-SP24-HW04

## Overview

1. You have to submit a PDF report, your code, and a video to Canvas.
2. Put all your files (PDF report, code, and video) into a **single compressed folder** named `Lastname_Firstname_A4.zip`.
3. Your PDF report should include answers and plots to all the questions.

## Installation Intructions

1. Please install Gymnasium with box2d (you can read more about Gymnasium [here](https://gymnasium.farama.org/)). You can find more about Gymnasium installation [here](https://github.com/Farama-Foundation/Gymnasium).
    ```
    pip install gymnasium[box2d]
    ```
2. Install PyTorch. You can follow the instructions provided [here](https://pytorch.org/get-started/locally/). To find out which CUDA version your machine has, you can run the command line utility ```nvidia-smi```.
3. **Requirements:** Python $\geq 3.8$, We recommend PyTorch $1.6$ or $2.1$.
4. It is strongly advised that you learn how to use virtual environment for Python. It creates an isolated environment from the system Python or other Python releases you have installed system-wide. It helps you manage Python packages in a clean fashion and allow you to only install necessary packages for particular projects. An exemplary, lightweight virtual environment module is `venv` [(link)](https://docs.python.org/3/library/venv.html). Your python distribution is likely to include it by default. If not, for example on Ubuntu, you can install it by
    ```
    sudo apt-get install python3-venv
    ```

## Assignment

### General Instructions

1.  You will complete this assignment in a Python (.py) file. The top-level code part ```__main__``` is given so that you do not need to write a separate train file.
2.  Type your code between the following lines
    ```
    ###### TYPE YOUR CODE HERE ######
    
    #################################
    ```
3. You do not need to modify the rest of the code for this assignment. However, feel free to do so if needed. The default hyperparameters should be able to solve LunarLander-v2.
4. The problem is solved if the **total reward per episode** is 200 or above. *Do not* stop training on the first instance your agent gets a reward above 200, and your agent must achieve a reward of  200 or above consistently.
5. The x-axis of your training plots should be  training episodes (or training iterations), and the y-axis should be episodic reward (or average episodic reward per iteration). You may have to use a sliding average window to get clean plots.\
6. **Video Generation:** You do not have to write your own method for video generation. Gymnasium has a nice, self-containted wrapper for this purpose. Please read more about Gymnasium wrappers [here](https://gymnasium.farama.org/api/wrappers/).

### Problems

In this homework, you will train a deep Q-Learning algorithm to land a lunar lander on the surface of the moon. We will use the Lunar Lander environment (LunarLander-v2) from  Gymnasium. The environment consists of a lander with $4$ discrete actions and a continuous state space. A detailed description of the environment can be found [here](https://gymnasium.farama.org/environments/box2d/lunar_lander/).

1. **Deep Q-Learning:** Implement deep Q-learning **with** experience replay and target network. You should include the training curve in the PDF (x-axis is the number of episode and the y-axis should be episodic cumulative reward). Use a sliding window average to get smooth plots. Include a description of the hyperparameters used. Also, you should submit a video of the smooth landing achieved by your RL algorithm. Try to find the optimal hyperparameters that will enable fast convergence to the optimal policy.  

2. **Ablation Study:** Perform ablation study to understand the importance of experience replay and target network. You should include the training curves, and  describe your observations and inferences.   

3. **Algorithmic Improvements:** As we discussed in the class, there has been a number improvements in the deep Q-learning algorithm and architecture, such as double DQN, dueling DQN, prioritized experience replay, and many other (see the slides and related papers).  Implement one (or more!) of these algorithmic ideas. Explain your implementation and demonstrate the benefit.  

4. **Deep Q-Learning on Another Environment:** Congratulations on implementing deep Q-Learning on the Lunar-Lander-v2 environment! Now,  learn the optimal  policy for another control problem (environment) using deep Q-Learning. You can select one environment from the *Classical Control* set, *Box2D* set or *Atari Games* set in Gymnasium.  In the PDF, you need to clearly specify the environment and provide a link to the corresponding page in Gymnasium. You need to include the training curve and describe the hyperparameters used. You should also include the video of the performance. 

### Credits

This homework code was assembled by past course assistant [Dr. Desik Rengarajan](https://github.com/DesikRengarajan).