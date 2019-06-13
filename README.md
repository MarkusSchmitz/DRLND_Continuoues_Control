[image1]: https://github.com/MarkusSchmitz/DRLND_Continuoues_Control/blob/master/reacher.gif?raw=true "Trained Agent"


# Project 2: Continuous Control

### Introduction

For this project, the work will be with the [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment.

![Trained Agent][image1]

This environment contains a bi-jointed (robot) arm that can move around its base joint. Additionally each arm has a green sphere that circles around it in a constand distance, but with varying direction and velocity.The goal is for the agent to keep it's outer joint (blue sphere) inside of the green goal sphere. For every timestep the agent is inside the goal sphere, it is awareded 0.1 points, otherwise none. 

The state of the environment contains the position, velocity, rotation of the arm as well as the goal sphere. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

In order to solve the environment, the agent must reach a average score of 30.

### Solving the Environment

This project uses a Unity environment that contains a single agent. The task is episodic, and in order to solve the environment,  the agent must get an average score of +30 over 100 consecutive episodes.
```python
env = UnityEnvironment(file_name='Reacher.app')
```
### Instructions
This ample of the project was computed on a MacOS with no GPU Accelearation.
In order to replicate the environent, follow these steps:

1. Create a new environment with Python 3.6 with Anaconda.
	```bash
	conda create --name drlnd python=3.6 
	activate drlnd
	```

2. Install the necessary dependencies in the environment with pip and conda:
	- __Install Unity ML-Agents__
	```bash
	pip install --user mlagents, unityagents
	```	
	```bash	
	- __Install Pytorch__
	conda install pytorch torchvision -c pytorch
	
	or

	conda install pytorch torchvision cudatoolkit=10.0 -c pytorch

	```
	- __Install tqdm__
	```bash
	pip install tqdm
	```
3. Download the `Reacher` environment from one of the links below and select the environment that matches your Windows operating system:
### Version 1: One (1) Agent
Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)

Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip

Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)

Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)
### Version 2: Twenty (20) Agents
Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)

Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)

Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)

Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)
 
4. Place the file in the uncompressed folder inside the `DRLND_Continuoues_Control/` folder.

### Train the agent 
Use the `p2_Continuous_Control.ipynb` in order to train the agent. The weights of the target nets are also saved as checkpoints.