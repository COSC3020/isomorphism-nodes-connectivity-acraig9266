# Plagiarism Statement
I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
No sources were used

# Isomorphism

Prove that if two graphs $A$ and $B$ have the same number of nodes and are
completely connected, they must be isomorphic. I have started with the formal
definition of isomorphism below. Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$G_1=(V_1 , E_1)$ is isomorphic to $G_2 = (V_2, E_2)$ if there exists a
one-to-one and onto function (bijection) $f: V_1 \rightarrow V_2$ such that $(u,v)
\in E_1$ iff $(f(u),f(v)) \in E_2$.
By definition, a completely connected graph has an edge connecting every individual pair of nodes in the graph. Since this means every node has a direct connection to every other node, each node has n - 1 edges connected to it.

Base case: With a graph containing 2 nodes that is completely connected, there is only one way for it to exist which is with 1 edge connecting the two existing nodes. Since there is only one way to create a graph of 2 nodes that is completely connected, all completely connected graphs with 2 nodes must be isomorphic.

To create a completely connected graph with 3 nodes, a new node can be added to the existing connected graph containing 2 nodes from the base case. For the graph to remain completely connected, the new node must have an edge from it to both previously existing nodes and there is only one way to do this which involves adding two edges. Since there is only one way to add a new node to an existing completely connected graph of size 2 while remaining completely connected, we know that any node added to a completely connected graph with 2 nodes can be mapped to any new node added to any other graph of previous size 2 that retains complete connectivity. Since the initial graphs containing 2 nodes were already isomorphic and the new nodes being added to each graph can be mapped directly to each other, any graph of 3 nodes that is completely connected can be called isomorphic to any other. This can be generalized to find that to retain the completely connected property of a graph while adding a new node, the new node can only be created in 1 way using n-1 (where n is the new number of nodes) edges to connect the new node to all existing nodes. Since the new node being added to a graph of size n that remains completely connected can only be created in one way, by using n-1 edges, we know that any node being added to a connected graph of size n while retaining complete connectivity can be mapped to any node being added to any other connected graph of size n that retains complete connectivity. Since we know that the graphs of size n-1 were isomorphic and the new nodes being added can be mapped to each other, the new graph of size n must also be isomorphic for all cases where n is a positive integer. Building upon our base case of a graph containing 2 nodes we can find that a completely connected graph of size n is isomorphic to any other completely connected graph of size n.
