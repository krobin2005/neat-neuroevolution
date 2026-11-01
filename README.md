<!--
OUTLINE ONLY. Project II rules: the final README text must be written by Kyle,
not by GenAI. Replace every [bracketed prompt] with your own words, then delete
the prompts and this comment.
-->

# Evolving Neural Networks through Augmenting Topologies (NEAT)

## Why I chose this topic
The reason why I was rather forward about researching NEAT was predominantly due to my lab work with Prof. Castro. In his lab, I am the Lead of AI Research in Digital Olfaction Prediction, essentially scent prediction based on molecular structure and augmentation. You see, in our lab we work in claude workflows of machine learning and use models of loss measured neural networks through augmenting weights via gradient decent; however, through NEAT we get to extend this idea, and I have been eager to learn more.  

## Background: neural networks in one page
Neural networks (NN) are essentially a set of machine learning algorithms that are based after the human mind. Given the name. In more of a computer science sense, it is helpful to draw the comparison of a search tree, where there is a root, there are nodes, and leaves. When referring back to a NN it is effectively the same, however with different names. A NN consists of layers at a minimum of two but most commonly more. There is first an input layer (what would be most similar to a root node) where raw data is stored and initially passed into either a hidden layer or an output layer. Next would be the hidden layer, where there could be any number of layers, this is where actual computation is occurring. Finally, there is the output layer where a result is stored as a prediction or also commonly a regression result (most similar to the leaves of a search tree). Where the comparison diverts completely is that in a tree each node only has one parent while in a NN a neuron gets inputs from several other neurons. 

Each individual node, or in this case neuron, processes data in its own way. Data is passed through and multiplied by a weight (which is the strength of the incoming connection). Typically a NN will train weights on gradient decent and adjust them to minimize a statistical loss.

## What does NEAT do different? 
Neuroevolution is taking the the structure of a neural network and using it to minimize a loss through evolution instead of gradient decent. While gradient decent will alter weights to minimize loss, NEAT will alter the weights as well as the topology (NN structure), such as adding nodes. 

## Experiment 1: Is it a 7? (gradient descent vs. NEAT)
- Run it: open `colab/3_Is_it_a_7_GD_vs_NEAT.ipynb` in Colab and click Run all
The experiment revolves around a NEAT NN learning what is the number 7 on real handwritten pixels. The model will answer "7 or not 7". Something I expected in this experiment was that I thought both implementations of gradient decent and NEAT would both be successful. This later proved to be true with gradient decent predicting on 97.6% accuracy and NEAT at 95%; however NEAT predicted on a far smaller network. For these sorts of implementations I actually don't NEAT is the better model, I rather think that NEAT is more effective in networks with several output nodes. 

## Experiment 2: Balancing a pole (where gradient descent can't start)
- Run it: open `colab/4_Pole_Balancing_NEAT.ipynb` in Colab and click Run all
- [The setup in your words: a cart pushes left or right to keep a pole upright, and there is no "correct push" for each moment, only a score for how long it stayed up]
The main benefit of NEAT is displayed in great proportion throughout this experiment in comparison to a gradient decent based NN. In real physics problems gradient decent will not function due to a need to know what the correct answer actually is. For gradient decent to function there needs to be a output node that is predetermined, so in turn it has nothing to learn and is just guessing. NEAT however can learn through augmenting topologies and continued to balance the pole for 500 steps (the max) while on the other hand random pushing can make it about 20 steps, a clear and significant win for NEAT. I chose to also use this experiment because it is what is used in the NEAT paper with the exception that the paper balances two poles instead of one.  

## Teaching it: the class activity
- Open `colab/5_Class_Activity_Break_NEAT.ipynb` in Colab
- [What the activity asks people to do (turn off parts of NEAT and predict what breaks) and why you designed it that way]
- [How it mirrors the paper's ablation study]
- [What the class found, if you want to add it after Nov 3]

## What I learned / what was hard
[The hardest concept and how it finally clicked. Maybe a before/after: early on you weren't sure what NEAT even was.]

## What's in this repo
[One line each in your words: `colab/` (the five notebooks), `gd_vs_neat.ipynb` (all experiments in one notebook), `neat_activity.ipynb`, `xor_neat.py` + `config-xor.ini` (the first warm-up run, also what the GitHub workflow runs), `requirements.txt`]

## References
- Stanley, K. O., & Miikkulainen, R. (2002). Evolving Neural Networks through Augmenting Topologies. *Evolutionary Computation*, 10(2), 99–127.
- neat-python documentation: https://neat-python.readthedocs.io
- [Handwritten digits dataset: scikit-learn `load_digits`]
- [Add videos, readings, and your GenAI use (notebooks, slides and code were built with Claude; this README text is your own)]
