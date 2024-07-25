# Repo content
Repository featuring the visual evaluation notebook of the RL project of Marcus and Lukas (WWI21DSB). <br><br>
In general the project has been about tuning, training and evaluating a DQN and a SAC model on the highway-env environment (https://highway-env.farama.org/index.html) as well as comparing their performance.

## IMPORTANT
The video visualizations do not show up after downloading from Colab and pushing to GitHub. The notebook needs to be run again with the model paths changed to the correct location after downloading the models from the drive like found below.

#### IMPORTANT: The other notebooks are located on Kaggle since hyperparametertuning and training have been done there.

#### The train notebooks do not feature any graphics visualizing training progression. We have decided to log all that data and integrate a wandb callback to create a broad range of visual training insights in a central and persistent place. Links to wandb spaces are listed below.
The wandb tracking board is divided into several sections. The most important one is the rollout section, which shows the reward curve during training as well as the lenght of the episode, so how long the agent survives. For DQN also the curve of the exploration rate is of interest. The eval section shows essentially the same, but for the eval runs, that happen every 1 000 or 10 000 steps in our project depending on the exact configuration. For SAC this is also quite interesting since these eval runs happen on the open environment without road borders (see report for details). <br>
The train section shows the loss curves during training, providing very detailed additional insights. The most important insights there are that the loss in the best DQN run (20 000 step model) goes down quite nicely, and also the actor loss of the SAC model shows a clear downward trend. The critic loss is increasing, which makes sense since with the agent crashing at a later point of time there are many new observations to learn that of course the agent can not handle nicely right away. <br>
It is important to note that only 10 runs are visualized at a time in wandb (so selection in the side bar is needed)!


# DQN
##### Parameter tuning notebook: https://www.kaggle.com/code/lukasgren/rl-dqn-parameter-tuning
##### Graphics for tuning runs: https://wandb.ai/lukasgrengames/dqn_tuning_RL_final_end 
##### Final training notebook: https://www.kaggle.com/code/lukasgren/rl-dqn-final-training
##### Graphics for final training: https://wandb.ai/w02marcus/sac_final_training (both are in one place for comparison despite the sac in the name)
##### Trained models: https://drive.google.com/drive/folders/1lGXklN8rJmDaZjx3BCEQuaX0mqTSGc2y?usp=sharing 

# SAC
##### Parameter tuning notebook: https://www.kaggle.com/code/wmarcus/sac-parameter-tuning/notebook
##### Graphics for tuning runs: https://wandb.ai/w02marcus/sac_tuning_borders_new
##### Final training notebook: https://www.kaggle.com/code/wmarcus/sac-final-training
##### Graphics for final training: https://wandb.ai/w02marcus/sac_final_training
##### Trained models: https://drive.google.com/drive/folders/1NfbXXmA2UX4tO_jsM420l2cu1Qn3wCRH?usp=sharing 
