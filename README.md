# Evolving Neural Networks through Augmenting Topologies (NEAT)

## Why I chose this topic
The reason why I was rather forward about researching NEAT was predominantly due to my lab work with Prof. Castro. In his lab, I am the Lead of AI Research in Digital Olfaction Prediction, essentially scent prediction based on molecular structure and augmentation. You see, in our lab we work in Claude workflows of machine learning and use models of loss measured neural networks through adjusting weights via gradient descent; however, through NEAT we get to extend this idea, and I have been eager to learn more.  

## Background: neural networks in one page
Neural networks (NN) are essentially a set of machine learning algorithms that are based on the human mind, hence the name. In more of a computer science sense, it is helpful to draw the comparison of a search tree, where there is a root, there are nodes, and leaves. When referring back to a NN it is effectively the same, however with different names. A NN consists of layers at a minimum of two but most commonly more. There is first an input layer (what would be most similar to a root node) where raw data is stored and initially passed into either a hidden layer or an output layer. Next would be the hidden layer, where there could be any number of layers; this is where actual computation is occurring. Finally, there is the output layer where a result is stored as a prediction or also commonly a regression result (most similar to the leaves of a search tree). Where the comparison diverts completely is that in a tree each node only has one parent while in a NN a neuron gets inputs from several other neurons. 

Each individual node, or in this case neuron, processes data in its own way. Data is passed through and multiplied by a weight (which is the strength of the incoming connection). Typically a NN will train weights on gradient descent and adjust them to minimize a statistical loss. The neuron will also add all of the weighted inputs together and add a bias before passing the numbers into a function that will return an output for the next node.

## What does NEAT do differently?
Neuroevolution takes the structure of a neural network and minimizes a loss through evolution instead of gradient descent. While gradient descent will alter weights to minimize loss, NEAT (Stanley & Miikkulainen, 2002) will alter the weights as well as the topology (NN structure), such as adding nodes, to maximize a fitness score. 

## Experiment 1: Is it a 7? (gradient descent vs. NEAT)
- Run it: open `colab/3_Is_it_a_7_GD_vs_NEAT.ipynb` in Colab and click Run all

The experiment revolves around a NEAT and gradient NN learning what is the number 7 on real handwritten pixels. The model will answer "7 or not 7". Something I expected in this experiment was that I thought both implementations of gradient descent and NEAT would be successful. This later proved to be true with gradient descent predicting with 97.6% accuracy and NEAT at 95%; however NEAT predicted on a far smaller network: 0 hidden neurons and 44 parameters for NEAT, vs. 8 hidden neurons and 529 parameters for gradient descent. For these sorts of implementations my experimentation showed that with labeled answers gradient descent will win on accuracy, but NEAT leads in using a far smaller network while also not needing to define a topology. 

## Experiment 2: Balancing a pole (where gradient descent can't start)
- Run it: open `colab/4_Pole_Balancing_NEAT.ipynb` in Colab and click Run all

The main benefit of NEAT is displayed in great proportion throughout this experiment in comparison to a gradient descent based NN. In problems where a decision is not proven to be correct, gradient descent cannot learn; so in turn it is guessing. Gradient descent's only feedback is how close it is to the right answer. NEAT however can learn through augmenting topologies and continue with mutations that push the model to a higher fitness. NEAT pushed to balance the pole for 500 steps (the max) while on the other hand random pushing can make it about 20 steps, a clear and significant win for NEAT. I chose to also use this experiment because it is what is used in the NEAT paper with the exception that the paper balances two poles instead of one.  

## Teaching it: the class activity
- Open `colab/5_Class_Activity_Break_NEAT.ipynb` in Colab

The class activity takes an XOR gate and has NEAT solve it. XOR cannot be solved without hidden neurons so it requires NEAT to add nodes. The first portion is a normal NEAT run on the problem and plots fitness, species, and a final network. The second portion takes altered parameters that are intended to break NEAT and show its weaknesses and requirements. The alterations are listed below:

- A: can’t add neurons (it can never solve XOR)
- B: no species (new ideas get no protection)
- C: only 10 networks instead of 150
- D: huge random weight jumps
- E: adds neurons too eagerly
- F: can’t add or remove connections

I am hoping for a class discussion following some experimentation. This is the same study done in the paper's ablation study however at a smaller scale where each of NEAT's necessities are turned off to show how they all matter. 

## Reflection: What I learned / what was hard
Upon starting project 2 I understood the greater concept of evolving neural networks, although I did not really understand what was going on behind the curtain. Reading and working on NEAT experimentation has helped me understand how models of machine learning are applicable in several mediums; consequently, it also embedded the common saying in computer science that there is "no free lunch". What I mean in saying this is that NEAT can be especially effective in some scenarios, but other implementations are better in other instances. Pushing me to understand that in everybody's project in this module are crucial in all of their own ways. What I thought was particularly difficult in the project is comprehending and digesting difficult papers such as NEAT. It tends to take me a couple of reads and extensive research to grasp the idea of high academic material.      

## What's in this repo
| File | What it is |
| --- | --- |
| `colab/` | The five Colab notebooks: XOR, circle, Is it a 7?, pole balancing, and the class activity |
| `gd_vs_neat.ipynb` | All the gradient descent vs. NEAT experiments in one notebook |
| `neat_activity.ipynb` | The class activity (experiment cards A–F) |
| `xor_neat.py`, `config-xor.ini` | First warm-up run: NEAT evolves a network that solves XOR. The GitHub workflow runs this on every push |
| `requirements.txt` | Python packages: `pip install -r requirements.txt` |
| `.github/workflows/neat.yml` | GitHub Actions workflow |

## References
- Stanley, K. O., & Miikkulainen, R. (2002). Evolving Neural Networks through Augmenting Topologies. *Evolutionary Computation*, 10(2), 99–127.
- neat-python documentation: https://neat-python.readthedocs.io
- Handwritten digits dataset: scikit-learn `load_digits` (UCI optical recognition of handwritten digits)

## GenAI disclosure
- The notebooks, code, GitHub workflow and slides were built with help from Claude (Anthropic).
- All writing done by me, however used Claude for formatting such as the table for the "What's in this repo"
