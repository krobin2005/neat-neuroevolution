<!--
OUTLINE ONLY. Project II rules: the final README text must be written by Kyle,
not by GenAI. Replace every [bracketed prompt] with your own words, then delete
the prompts and this comment.
-->

# Evolving Neural Networks through Augmenting Topologies (NEAT)

## Why I chose this topic
The reason why I was rather forward about researching NEAT was predominantly due to my lab work with Prof. Castro. In his lab, I am the Lead of AI Research in Digital Olfaction Prediction, essentially scent prediction based on molecular structure and augmentation. You see, in our lab we work in claude workflows of machine learning and use models of loss measured neural networks through augmenting weights via gradient decent; however, through NEAT we get to extend this idea, and I have been eager to learn more.  

## Background: neural networks in one page
Neural networks are essentially a set of machine learning algorithms that are based after the human mind. Given the name. In more of a computer science sense, it is helpful to draw the comparison of a search tree, where there is a root, there are nodes, and leafs. When referring back to a NN it is effectively the same, however with different names. A NN consists of layers at a minimum of three. There is first an input layer (what would be most similar to a root node) where raw data is stored and initially passed into either a hidden layer or an output layer. Next would be the hidden layer, where there could be an infinite about of layers, this is where actual computation is occurring. Finally, there is the output layer where a result is stored as a prediction or also commonly a regression result (most similar to the leaf of a search tree).

Each individual node, or in this case neuron, processes data in its own way. Data is passed through and multiplied by a weight (which is the strength of the incoming connection). Typically a NN will train weights on gradient decent and augment them to minimize a statistical loss.

## What does NEAT do different? 
[What neuroevolution is. How NEAT works: minimal start, add-node / add-connection mutations, innovation numbers, speciation. Cite Stanley & Miikkulainen 2002.]

## Experiment 1: NEAT solves XOR
- How to run: `pip install -r requirements.txt` then `python xor_neat.py`
- [What you expected before running it]
- [What happened: generations needed, hidden neurons added, fitness plot from results/]
- [What surprised you]

## My own questions
[Experiments you ran by changing config-xor.ini or the code: population size, mutation rates, starting with hidden neurons, etc. What did each change do, and why?]

## What I learned / what was hard
[The hardest concept and how it finally clicked.]

## References
- Stanley, K. O., & Miikkulainen, R. (2002). Evolving Neural Networks through Augmenting Topologies. *Evolutionary Computation*, 10(2).
- neat-python documentation: https://neat-python.readthedocs.io
- [Add videos, readings and any AI assistance you used]
