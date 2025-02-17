# Graph_Coloring_QUBO

Graph Coloring Problem : Find the minimum number of colors we can use to color the vertices of a graph such that no two vertices sharing an edge are the same color. 

Let vertices be {v1, v2, ..., vm} and let the possible colors to choose from to color each vertex be {c1, c2, ..., cn}

A decision variable xij is either 0 or 1 : 1 if vertex i is color j and 0 if not. 

There are two constraints we must create constraint penalties for, namely : a vertex must have only one color, and that no two vertices with a common edge may have the same color. 

Handling Constraint 1 : A vertex must only have one color. 
If vertex v4 is colored c5, x45 = 1 and x4i for all possible i is 0. Hence, the condition can be written as x41 + x42 + ... + x4n = 1 (only one of the variables in this equation can be 1 and others must be 0). Hence, 

Handling Constraint 2 : 2 vertices sharing an edge must not be the same color. 
Suppose x_11, x_12, ..., x_1n are (0, 0, 1, 0, ..., 0). Suppose vertices 1 and 3 share an edge. Then, if x_31, x_32, ..., x_3n are also (0, 0, 1, 0, ..., 0), both vertices are the same color and the second constraint is violated. The penalty associated with violating the second constraint is $\sum^{n}_{j=1} x_{i}{j}$
