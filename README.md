# SCC-in-a-graph
This program finds the strongly connected components (SCC) in a graph, and also classifies whether it is a DAG (directed acyclic graph) and performs the topological sort.
Here I have created the functions IS_DAG and TOPOLOGICAL_SORT which work in the following way:
The IS_DAG function takes the graph as its argument and checks whether the graph is a DAG or not based on the presence of a back edge in the graph.
The TOPOLOGICAL_SORT function basically prints the vertices of the graph in a topologically sorted order, as computed by the DFS on the graph.
The program also finds the strongly connected components present in the grapph. 
The first DFS has already been performed on the graph in the main function. Then the function STRONGLY_CONNECTED_COMPONENTS calls the function graph_transpose for creating the transpose graph for the originally entered graph. 
Then I have performed second DFS on the transpose graph, but in the main loop of this DFS, I have called the vertices in the decreasing order of their finishing times as computed by the first DFS. For this, I have used the topological sort order for calling the vertices. 
Then I have printed each tree in the depth first forest as a separate strongly connected component.
