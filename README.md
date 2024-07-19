# Repo content
Repository featuring the visual evaluation notebook of the RL project of Marcus and Lukas (WWI21DSB). <br><br>
In general the project has been about tuning, training and evaluating a DQN and a SAC model on the highway-env environment (https://highway-env.farama.org/index.html) as well as comparing their performance.

#### IMPORTANT: The other notebooks are located on Kaggle since hyperparametertuning and training have been done there.

#### The train notebooks do not feature any graphics visualizing training progression. We have decided to log all that data and integrate a wandb callback to create a broad range of visual training insights in a central and persistent place. Links to wandb spaces are listed below.
The wandb tracking board is divided into several sections. The most important one is the rollout section, which shows the reward curve during training as well as the lenght of the episode, so how long the agent survives. For DQN also the curve of the exploration rate is of interest. The eval section shows essentially the same, but for the eval runs, that happen every 1 000 or 10 000 steps in our project depending on the exact configuration. For SAC this is also quite interesting since these eval runs happen on the open environment without road borders (see report for details). <br>
The train section shows the loss curves during training, providing very detailed additional insights. The most important insights there are that the loss in the best DQN run (20 000 step model) goes down quite nicely, and also the actor loss of the SAC model shows a clear downward trend. The critic loss is increasing, which makes sense since with the agent crashing at a later point of time there are many new observations to learn that of course the agent can not handle nicely right away.


# DQN
##### Parameter tuning notebook: 
##### Graphics for tuning runs: https://wandb.ai/w02marcus/dqn_tuning_RL
##### Final training notebook:
##### Graphics for final training: https://wandb.ai/w02marcus/sac_final_training (both are in one place for comparison despite the sac in the name)

# SAC
##### Parameter tuning notebook: https://www.kaggle.com/code/wmarcus/sac-parameter-tuning/notebook
##### Graphics for tuning runs: https://wandb.ai/w02marcus/sac_tuning_borders_new
##### Final training notebook: https://www.kaggle.com/code/wmarcus/sac-final-training
##### Graphics for final training: https://wandb.ai/w02marcus/sac_final_training
