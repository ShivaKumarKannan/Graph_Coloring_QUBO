# Graph_Coloring_QUBO

Graph Coloring Problem : Find the minimum number of colors we can use to color the vertices of a graph such that no two vertices sharing an edge are the same color. 

A decision variable xij is either 0 or 1 : 1 if vertex i is color j and 0 if not. 

There are two constraints we must create constraint penalties for, namely : a vertex must have only one color, and that no two vertices with a common edge may have the same color. 
