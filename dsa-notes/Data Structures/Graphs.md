## Basic Graph Theory
- **Strongly Connected**: a directed graph is strongly connected if every vertex is reachable from every other vertex. 
- A graph is a tree if:
	- it is fully connected 
	- there are no cycles 
	- For a graph to be a tree it must have exactly `n-1` edges 
## Advanced Graph Theory

#### Eulerian Properties
- **Eulerian Graphs**: A graph is called Eulerian if it has an Eulerian Cycle and called Semi-Eulerian if it has an Eulerian Path.
- **Eulerian Trail**: (or **Eulerian path**) is a trail in a finite graph that visits every edge exactly once (allowing for revisiting vertices).
	- An undirected Graph has an eularian path if:
		1. All vertices with non-zero degree are connected. We don’t care about vertices with zero degree because they don’t belong to Eulerian Cycle or Path (we only consider all edges). 
		2. If zero or two vertices have odd degree and all other vertices have even degree. Note that only one vertex with odd degree is not possible in an undirected graph (sum of all degrees is always even in an undirected graph)
	- A directed graph has an eularian path if:
		1. at most 1 vertext has `in - out = 1` and at most 1 vertext has `out - in = 1` and all other vertecies have `in == out`
- **Eulerian Cycle**: is an eularian trail that starts and ends on the same node. Or put another way, an eularian cycle is a cycle in a finite graph that visits every edge once.
	- An undirected graph has Eulerian cycle if:
		1. All vertices with non-zero degree are connected. We don’t care about vertices with zero degree because they don’t belong to Eulerian Cycle or Path (we only consider all edges). 
		2. All vertices have even degree.
	- A directed graph has an eularian cycle if:
		1. All verticies with non-zero degrees belong to a single strongly connected component. 
		2. The in-degree and out-degree of every vertext is the same.
#### Cut Theory
- A "cut" is a set of edges that divides the graph into two disjoint sets of nodes. This set of "cuts" is called a **Cut Set**
- The smallest weighted edge in a cut set will be in the MST of a graph. This is the basis of Kruskal's Algorithm 
