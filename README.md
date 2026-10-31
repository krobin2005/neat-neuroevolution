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
[What neuroevolution is: evolution changes both the weights AND the shape, using only a fitness score, no gradients. How NEAT works: starts with no hidden layer at all (ties back to your layers paragraph), add-node / add-connection mutations, innovation numbers so parents with different shapes can be crossed, speciation so new structure gets time to improve. Cite Stanley & Miikkulainen 2002.]

## Experiment 1: Is it a 7? (gradient descent vs. NEAT)
- Run it: open `colab/3_Is_it_a_7_GD_vs_NEAT.ipynb` in Colab and click Run all
- [The setup in your words: real handwritten digits, the network answers "7 or not 7", and both methods get the correct answers to learn from]
- [What you expected before running it]
- [What happened: gradient descent 97.6% vs. NEAT 95.0% on 597 unseen digits, and how much smaller NEAT's network was (8 hidden neurons / 529 parameters vs. 0 hidden / 44 parameters)]
- [NEAT's mistakes were mostly 4s and 5s it called 7s. Why might those digits fool it?]
- [What this tells you: when you have the answers, is NEAT worth it?]

## Experiment 2: Balancing a pole (where gradient descent can't start)
- Run it: open `colab/4_Pole_Balancing_NEAT.ipynb` in Colab and click Run all
- [The setup in your words: a cart pushes left or right to keep a pole upright, and there is no "correct push" for each moment, only a score for how long it stayed up]
- [Why gradient descent has nothing to learn from here]
- [What happened: NEAT balanced 500 steps (the max) on new starts vs. about 20 for random pushing, with 0 hidden neurons]
- [Connect it to the paper: this is the same kind of task the paper used to show NEAT beating other methods]

## My own question: how much does luck matter?
[You reran NEAT 5 times on the circle task with only the random seed changed: 78.0%, 86.5%, 74.0%, 88.0%, 74.5%. What does that range tell you about trusting a single run, and how does it relate to the paper averaging over many runs?]

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
