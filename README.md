[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif "Trained Agent"

# Deep RL Project: Continuous Control (Reacher)

## Introduction

The project's objective is to train an agent to move 2-joint robot arms to a specific location in the following Unity environment.

![Trained Agent][image1]

A reward of +0.1 is provided for a robot arm to reach the specific location guided by a big bubble. Thus, the goal of the agent is to figure out a right amount of torques on the 2 joints so that the arm is able to reache the position

The robot-arm state space has 33 dimensions and contains the robot-arm's position, rotation, velocity, and angular velocities. Given this information, the agent has to learn how to contro the robot-arm's joints. Four continuous actions are available with the range of [-1, 1]

To improve the reliability of the agent training, the task is configured with 20 agents. As a result, the agent will observe 20 x 24 states and order 20 x 4 actions. The codes in the notebook will train an agent to achieve an average score of +30 of 20 agents over 100 consecutive episodes by using DDPG algorithm.


## Getting Started

#### Requirements
- Linux OS
- Python environment
- [Unity 20-arm Reacher environment](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
- Git

#### Steps

1. Install Git and Anaconda

2. Create Python environment on Anaconda
```
conda create --name drl python=3.6
conda activate drl
```

3. Clone the the following repository and install Python dependencies to run the code
```
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
pip install .
```

4. Create IPykernel to use the current environment
```
python -m ipykernel install --user --name drl --display-name "drl"
```

5. Download the following Linux Unity environment zip archive file.
    - [Unity 20-arm Reacher environment](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)

6. Place the file in the current root folder of this repository, and unzip (or decompress) the file. 

7. Run Jupyter/Ipython Notebook and Change the kernel to "drl"

8. Make Unity Environment to point to the file decompressed by the step 5
```
env = UnityEnvironment(file_name='/data/Reacher_Linux_NoVis/Reacher.x86_64')
```

9. Follow the steps in the notebook `Continuous_Control.ipynb` from top to bottom.


## Instructions

All the codes (Model, Training and Simulation) are written in `Continuous_Control.ipynb`. Please follow the notebook from top to bottom to create, train and test the agent.
It can be directly modified for any changes of the algorithm inside a notebook