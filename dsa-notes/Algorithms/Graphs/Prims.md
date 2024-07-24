#### Description
- prims algorithm is a greedy algorithm that selects the smallest weighted edge that is not yet connected to the set of visited nodes. This is very similar to Kruskal's algorithm in that they both select the smallest edge from a [cut set](./Data Structures/Graphs). 

#### One Liner
- Start on a random node and put all it's edges in a priority queue, then pop the queue and repeat the process for the next node. 