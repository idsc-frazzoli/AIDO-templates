# README


## Running the template

The template is interfaced with a makefile to run the most important steps of the development process.

- make install:
This command will install the Docker container which runs code based on the supplied Github repository. It is recommended to fork the repository https://github.com/duckietown/gym-duckietown-agent and to build upon that. For all used packages, please ensure that they are listed in the file "setup.py" in the repository. This will ensure that Docker correctly installs the environment.

- make learn:
The "make learn" command starts the learning process within the Docker environment. Once finished, the Docker container saves the model in another Docker container used solely for evaluation.
TODO: - make sure learned agent is saved for execution

- make container: (might not be necessary additionally)

- make evaluate-sim-local:
This runs the evaluation Docker container in the simulation environment. From the collected logs, statistics about the performance based on the [competition rules](http://docs.duckietown.org/AIDO/out/aido_rules.html) are computed (follow the link for more details).
TODO: - write evaluate function in simulator, - Also provide logs of what happened other than the score

## Development process

To develop your own reinforcement learning submission, we recommend forking the repository [https://github.com/duckietown/gym-duckietown-agent](https://github.com/duckietown/gym-duckietown-agent).

In this file you can edit the "agent.py" file and implement your own agent. When adding new dependencies, likewise add the used packages to the requirements in the "setup.py" file. 


TODOs:
- Should be able to manually specify which rewards are awarded for what.
- Should have a memory buffer / volume attached to run DQN etc.
-
