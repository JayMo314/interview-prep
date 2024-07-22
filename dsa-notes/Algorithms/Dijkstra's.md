### Description 
- The result of this algorithm is the cost of the shortest path from the source node to every node in the graph. 
### One Liner
- Relax all edges of a node while using a priority queue to choose the next node to process, a visited set to ignore previously processed nodes, and an array to store distances for each node. 
### Notes
- The result of Dijkstra's is the min cost to reach each node from the source node
- Dijkstra's algorithm is essentially incrementing all possible paths from `src` to `dst` and the least expensive path will reach the `dst` first 
- Dijkstra is a greedy algorithm in that it only processes the smallest path each time. This greedy behavior can be adapted for use in other applications. see [Swim In Rising Water](https://www.youtube.com/watch?v=amvrKlMLuGY&ab_channel=NeetCode)

### Code
```java
public int[] dijkstra(List<int[]>[] graph, int n, int k){
//call with n+1 for 1-indexed arrays

//1. Init dist array, visited array and priority queue
int[] dist = new int[n];
for (int i = 1; i <= n; i++){
	dist[i] = Integer.MAX_VALUE;
}

dist[k] = 0;

boolean[] visited = new boolean[n];
PriorityQueue<int[]> pq = new PriorityQueue<>((a,b) -> (a[1] - b[1]);

//2. Seed priority queue with source node and weight zero
pq.add(new int[]{k,0});

//3. Process queue until empty
while(!pq.isEmpty()){

	//a. Pop node
	int[] curr = pq.poll();
	int u = curr[0], uDist = curr[1];
	
		//b. If not vistied then mark as visited and add neighbors
	if(!visited[u]) {
		visited[u] = true;
		
		//c. Relax Edges
		for(int[] nei : graph[u]) {
			int v = nei[0], w = nei[1];
			
			//i. Relax Edge
			if(dist[v] == Integer.MAX_VALUE || uDist + w < dist[v]){
			dist[v] = uDist + w;
			
			//ii. Put edge in PQ
			pq.add(new int[]{v, dist[v]});
		
		}
	}
}

//4. Return array with shortest distances 
return dist;

}
```
