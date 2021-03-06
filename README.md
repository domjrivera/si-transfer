# si-transfer

Transfer learning across multiple types of space invader type games with OpenAI Gym. Initial work is part of a final project effort for TTIC 31170. For the purposes of our efforts, we focused on implementing

Implemented by Jack Barbey, Jay Dhanoa, & Alex Hummels.

Built using the initial DQN implementation using the PTAN package, and some of the starting code it has for training a basic DQN model.

## Prerequisites

- The Pytorch AgentNet package (https://github.com/Shmuma/ptan) - `pip3 install ptan`
- OpenAI Gym: `pip3 install gym gym[atari]`
- Python OpenCV: `pip3 install opencv-python`
- tensorboardX for PyTorch: `git clone https://github.com/lanpa/tensorboardX && cd tensorboardX && python3 setup.py install`

## General model outline

For any of the following scripts, you can run `python3 script_name.py -h` to print argparse information.

## Expert Model Training

The relevant code can be found in `python3 train_model.py`. We trained expert models in Assault, Demon Attack, and Space Invaders.

## Multi-Environment Training

Here, we attempt to simultaneously train a model on both Space Invaders and Demon Attack. It can be run from `python3 train_model_multienv.py`

## Actor-Mimic Training

Here we use the Actor-Mimic protocol (outlined here: https://arxiv.org/pdf/1511.06342.pdf, by Parisotto et al.) to train Space Invaders and Demon Attack together. It can be run from `python3 train_model_actormimic.py`

## Transfer Learning

We implemented transfer learning to learn from models generated by the first three scripts in `transfer_model.py`.

## Results

Graphs of some of our results can be found in `plot_results.ipynb` and the `figures` directory.

## Old Notebooks

Our initial implementation is stored under `old_notebooks.ipynb`.
