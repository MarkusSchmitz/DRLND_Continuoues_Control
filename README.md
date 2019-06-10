[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif "Trained Agent"
[image2]: https://user-images.githubusercontent.com/10624937/43851646-d899bf20-9b00-11e8-858c-29b5c2c94ccc.png "Crawler"


# Project 2: Continuous Control

### Introduction

For this project, the work will be with the [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment.

![Trained Agent][image1]

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

The Benchmark Mean Reward is 30.

### Solving the Environment

This project uses a Unity environment that contains a single agent. The task is episodic, and in order to solve the environment,  the agent must get an average score of +30 over 100 consecutive episodes.
```python
env = UnityEnvironment(file_name='Reacher.exe')
```
### Instructions
This project runs locally on Windows 10 environment. Here are the steps to setup the environment:
1. Create (and activate) a new environment with Python 3.6.
	```
	- __Windows__: 
	```bash
	conda create --name drlnd python=3.6 
	activate drlnd
	```

2. Install these dependencies in the environment on windows 10
	- __Install Unity ML-Agents__
	```bash
	pip3 install --user mlagents
	```	
	- __Install Unity Agents__
	```bash
	pip install unityagents
	```	
	- __Install Pytorch__
	```bash
	conda install pytorch torchvision cudatoolkit=9.0 -c pytorch
	```
3. Download the `Reacher` environment from one of the links below and select the environment that matches your Windows operating system:
    - **_Version 1: One (1) Agent_**
        - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
        - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)
 
4. Place the file in the `continuous_control/` folder, and unzip (or decompress) the file.

### Train the agent 
Execute  the cells within `Continuous_Control.ipynb` in order to initialize the environment with making necessary adjustments for the path to the UnityEnvironment in the code, initialize the agent, and perform the training of a single agent.