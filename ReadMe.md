# Training OpenAI Gym Half Cheetah environment using Soft-Actor-Critic with maximum entropy algorithm

## Contributors:
#### Tej Kiran
#### Ji Liu

## Required libraries and tested environment settings
Please make sure to create the environment using the provided conda environment file
    
    -Create conda enviornment
        conda env create -f EnvSAC.yml

  ## Instructions to run the code:   
    Step 1: Clone the repositiory
    
    Step 2: Open terminal, activate the python environment and cd to the above "code" location
    
    Step 3: To train the network run "python3 sac_train.py"

    Step 4: To train the network run "python3 sac_test.py"

  

  ## Training
  The Model has been trained in 3 different stages with the temperature parameter alpha reset at the beggining of every stage
  <ul>
    <li>Stage 1 : 500 complete episodes</li>
    <li> Stage 2 : 5000 episodes each terminated at 100th step</li>
    <li>Stage 3 : 1000 episodes each terminated at 500th step </li>
  </ul> 
   
  ## Results
  * The normalized reward plot is as shown below

  ![Alt text](./doc/Images/RewardPlot.png?raw=true "Reward Plot")

  * The achieved results in the simulation is as shown in the below


https://github.com/itej89/SoftActorCritic-halfcheetah/assets/37236721/f4239e7d-371a-43b8-a726-bb46343c3616



  ## Errors and solutions
To avoid path errors when training on nvidia GPU, please run the following commands

    - export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:~/.mujoco/mujoco210/bin
    - export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/lib/nvidia
    - export LD_PRELOAD=/usr/lib/x86_64-linux-gnu/libGLEW.so
