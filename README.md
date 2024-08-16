# DoomMaster
The main objective of this project was to develop a reinforcement learning agent capable of playing the DOOM3D game efficiently. To achieve this, we used the PPO algorithm, a popular policy gradient method, and integrated it with the VizDoom environment via OpenAI Gymnasium. The model was trained over 150,000 epochs, and curriculum learning was employed to help the agent overcome local minima and improve overall performance.

# Key Highlights
1. Proximal Policy Optimization (PPO): Utilized PPO for its stability and efficiency in training policy-based reinforcement learning models.
2. VizDoom Integration: Connected the DOOM3D game environment using OpenAI Gymnasium to provide the necessary observations and rewards for the RL agent.
3. Curriculum Learning: Applied curriculum learning techniques to gradually increase the difficulty of the tasks, helping the agent avoid getting stuck in local minima.
4. Extensive Training: Trained the model for 150,000 epochs to ensure robust performance in the game environment.

# Prerequisites
Ensure you have the following Python libraries installed:

1. stable-baselines3
2. gymnasium
3. vizdoom  (this is the game engine built using Python. The advantage is that it can run with very high Frames per second thus making training much faster)
4. numpy

The most important aspect is to use Curriculum learning that mimics the way humans learn. We gradually increase the difficulty level, training the model for sufficient number of epochs for 
each difficulty and thus achieve the final trained model. This ensure that the model, if faced with very difficult learning environment, might not be able to learn anything as it might not get
any action that could be exploited. This is especially true for environments with a large number of possible actions.
