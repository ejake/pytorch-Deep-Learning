## Source of 16-gated_GCN.ipynb and complementary resources.

🥳 NEW LECTURE 🥳
Graph Convolutional Networks… from attention!
In attention 𝒂 is computed with a [soft]argmax over scores. In GCNs 𝒂 is simply given, and it's called "adjacency vector".
Slides: https://github.com/…/py…/blob/master/slides/11%20-%20GCN.pdf
Notebook: https://github.com/…/pytorch…/blob/master/16-gated_GCN.ipynb

Summary of today's class.

Slide 1: *shows title*.
Slide 2: *recalls self-attention*.
Slide 3: *shows 𝒂, points out it's given*.
The end.

Literally!
I've spent the last week reading everything about these GCNs and… LOL, they quickly found a spot in my mind, next to attention!
The key concept here is the *sparsity* (constraints) of the graph.
In self-attention, every element in the set looks at each and every other element.
If a sparse graph is given, we limit each element (node / vertex) to look only at a few other elements (nodes / vertices).
Now, if every incoming node is treated equally, this might seem a little weak, as learning algorithm.
Don't you worry! Let's reason on the edges (connecting the incoming nodes).
Enters the "gated" GCN, where the incoming node / message is modulated by a gate 𝜂.
Here 𝜂 if function of the representation (embedding / feature) of the incoming edge, which is a normalised sigmoid MLP (k=1 1D CNN, actually).
Finally, because-why-not, let's add some residual connections to smooth a little the loss landscape.

Tadaaaa!
The end.
P.S. I can't remember the last time I studied this much in such a short lapse of time. My brain is trying to escape my skull… I feel drunk and nauseated. But yes, one more lesson added to my collection.

Next week (if I survive ICLR): training your own energy model from scratch.

https://twitter.com/alfcnz/status/1255371270029488129
