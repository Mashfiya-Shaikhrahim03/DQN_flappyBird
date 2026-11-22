# Flappy Bird RL

This is my Reinforcement Learning project where I tried to train an agent to play Flappy Bird using a Deep Q-Network (DQN).

I built the main parts of the DQN myself to understand how an RL agent actually learns from an environment.

## Installation

Install the required packages:

```bash
pip install flappy-bird-gymnasium
pip install pyyaml
```

Run the project:

```bash
python agent.py
```

## Environment

I used Gymnasium and the Flappy Bird Gymnasium environment for this project.

The agent gets the game state from the environment, chooses an action, and receives a reward.

Gymnasium documentation:

https://gymnasium.farama.org/

## What I Did

I implemented a DQN agent with the following parts:

* DQN neural network
* Agent class
* Experience replay memory
* Epsilon-greedy exploration
* Policy network
* Target network
* Hyperparameters using YAML
* Model saving

The basic learning process is:

```text
State
  ↓
DQN
  ↓
Action
  ↓
Flappy Bird
  ↓
Reward
  ↓
Replay Memory
  ↓
Train DQN
```

## DQN

The DQN takes the current game state and predicts the Q-value for each possible action.

My network is built using PyTorch with linear layers and ReLU activation.

## Experience Replay

I store the experiences of the agent in replay memory:

```text
(state, action, next_state, reward, done)
```

During training, I randomly sample a mini-batch from the memory and use it to train the network.

## Exploration

I used epsilon-greedy exploration.

At the beginning, the agent takes more random actions so it can explore the environment. As training continues, epsilon decreases and the agent starts using what it has learned.

## Target Network

I used a separate target DQN to make the training more stable.

The target network is periodically synchronized with the policy network.

## Configuration

I kept the main training parameters in `parameters.yaml` so I can change them without changing the main code.

## Project Structure

```text
FlappyBird_RL/
│
├── agent.py
├── dqn.py
├── experience_replay.py
├── game_flappy_bird.py
├── parameters.yaml
└── README.md
```

## What I Learned

This project helped me understand DQN beyond just the theory.

I learned how the agent interacts with an environment, how experiences are stored and sampled, how Q-values are calculated, and why things like experience replay, epsilon-greedy exploration, and target networks are used.

## Future

I want to improve this project further by experimenting with:

* Better hyperparameters
* Reward shaping
* Double DQN
* Dueling DQN
* Training and reward graphs
# Flappy Bird RL

This is my Reinforcement Learning project where I tried to train an agent to play Flappy Bird using a Deep Q-Network (DQN).

I built the main parts of the DQN myself to understand how an RL agent actually learns from an environment.

## Installation

Install the required packages:

```bash
pip install flappy-bird-gymnasium
pip install pyyaml
```

Run the project:

```bash
python agent.py
```

## Environment

I used Gymnasium and the Flappy Bird Gymnasium environment for this project.

The agent gets the game state from the environment, chooses an action, and receives a reward.

Gymnasium documentation:

https://gymnasium.farama.org/

## What I Did

I implemented a DQN agent with the following parts:

* DQN neural network
* Agent class
* Experience replay memory
* Epsilon-greedy exploration
* Policy network
* Target network
* Hyperparameters using YAML
* Model saving

The basic learning process is:

```text
State
  ↓
DQN
  ↓
Action
  ↓
Flappy Bird
  ↓
Reward
  ↓
Replay Memory
  ↓
Train DQN
```

## DQN

The DQN takes the current game state and predicts the Q-value for each possible action.

My network is built using PyTorch with linear layers and ReLU activation.

## Experience Replay

I store the experiences of the agent in replay memory:

```text
(state, action, next_state, reward, done)
```

During training, I randomly sample a mini-batch from the memory and use it to train the network.

## Exploration

I used epsilon-greedy exploration.

At the beginning, the agent takes more random actions so it can explore the environment. As training continues, epsilon decreases and the agent starts using what it has learned.

## Target Network

I used a separate target DQN to make the training more stable.

The target network is periodically synchronized with the policy network.

## Configuration

I kept the main training parameters in `parameters.yaml` so I can change them without changing the main code.

## Project Structure

```text
FlappyBird_RL/
│
├── agent.py
├── dqn.py
├── experience_replay.py
├── game_flappy_bird.py
├── parameters.yaml
└── README.md
```

## What I Learned

This project helped me understand DQN beyond just the theory.

I learned how the agent interacts with an environment, how experiences are stored and sampled, how Q-values are calculated, and why things like experience replay, epsilon-greedy exploration, and target networks are used.

## Future

I want to improve this project further by experimenting with:

* Better hyperparameters
* Reward shaping
* Double DQN
* Dueling DQN
* Training and reward graphs
