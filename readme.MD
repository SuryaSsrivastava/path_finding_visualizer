# Shortest path visualizer

## Dijastra Algorithm

Below are the detailed steps used in Dijkstra’s algorithm to find the shortest path from a single source vertex to all other vertices in the given graph.
Algorithm

```

function Dijkstra(Graph, source):
2:	for each vertex v in Graph:	// Initialization
3:	    dist[v] := infinity	// initial distance from source to vertex v is set to infinite
4:	previous[v] := undefined	// Previous node in optimal path from source
5:	dist[source] := 0	// Distance from source to source
6:	Q := the set of all nodes in Graph	// all nodes in the graph are unoptimized - thus are in Q
7:	while Q is not empty:	// main loop
8:	    u := node in Q with smallest dist[ ]
9:	    remove u from Q
10:	    for each neighbor v of u:	// where v has not yet been removed from Q.
11:	        alt := dist[u] + dist_between(u, v)
12:	        if alt < dist[v]	// Relax (u,v)
13:	            dist[v] := alt
14:	            previous[v] := u
15:	return previous[ ]

```

## A* Algorithm

```
make an openlist containing only the starting node
   make an empty closed list
   while (the destination node has not been reached):
       consider the node with the lowest f score in the open list
       if (this node is our destination node) :
           we are finished 
       if not:
           put the current node in the closed list and look at all of its neighbors
           for (each neighbor of the current node):
               if (neighbor has lower g value than current and is in the closed list) :
                   replace the neighbor with the new, lower, g value 
                   current node is now the neighbor's parent            
               else if (current g value is lower and this neighbor is in the open list ) :
                   replace the neighbor with the new, lower, g value 
                   change the neighbor's parent to our current node

               else if this neighbor is not in both lists:
                   add it to the open list and set its g

```

### instructions
'''
1. Click once to mark starting point.
2. click again to mark destination point.
3. click to make walls.
4. press space to start running algorithm in action.
5. Right click to erase the marking.

'''
  
### Installing/dependencies 


Either install from packages by typing these commands in your terminal

```
pip install pygame
```

## Screenshots

### Dijastra

![Dijastra](https://i.ibb.co/X23LzxL/Screenshot-2020-10-10-191424.png)

![dijastra](https://i.ibb.co/hmwGDVz/Screenshot-2020-10-10-191516.png)

![dijastra](https://i.ibb.co/Sw7CZZ8/Screenshot-2020-10-10-191544.png)

![dijastra](https://i.ibb.co/9GDLzL6/Screenshot-2020-10-10-191609.png)

### A* 

![A*](https://i.ibb.co/ncL1ngb/Screenshot-2020-10-10-191845.png)

![A*](https://i.ibb.co/KG999qx/Screenshot-2020-10-10-191912.png)
