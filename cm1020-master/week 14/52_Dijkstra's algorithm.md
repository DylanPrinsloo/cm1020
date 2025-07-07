# Dijkstra's Algorithm

## 📊 Introduction to Weighted Graphs

A weighted graph is a graph where each edge is assigned a numerical value. These weights can represent:
- Distances between cities
- Response times in communication networks
- Transaction costs
- Any quantifiable relationship between connected vertices

## 🔍 Overview of Dijkstra's Algorithm

In 1956, computer scientist Edsger Dijkstra developed an algorithm to compute the shortest path between vertices in a weighted graph. This algorithm:
- Finds the shortest path from a single source vertex to all other vertices
- Works effectively on graphs with non-negative edge weights
- Uses a greedy approach, always selecting the unvisited vertex with the smallest known distance

## 🔢 How Dijkstra's Algorithm Works

The algorithm maintains three key pieces of information:
1. **Distance**: The current shortest known distance from the start vertex
2. **Previous vertex**: The vertex through which we reached the current vertex
3. **Unvisited list**: Vertices that haven't been fully processed yet

### Algorithm Steps:

#### 1. Initialization
- Set distance to the start vertex as 0
- Set distance to all other vertices as infinity
- Set all previous vertices as undefined
- Add all vertices to the unvisited list

#### 2. Update Process (Iterative)
- Visit the unvisited vertex with the smallest known distance
- For each unvisited neighbor:
  - Calculate distance through current vertex
  - If calculated distance is less than known distance, update both distance and previous vertex
- Remove current vertex from unvisited list
- Repeat until all vertices have been visited

## 🧮 Step-by-Step Example

Consider finding the shortest path from vertex A to all other vertices in a graph:

### Iteration 1:
- Start at vertex A (distance = 0)
- Check neighbors B and C:
  - Distance to B = 0 + 3 = 3
  - Distance to C = 0 + 2 = 2
- Update table and remove A from unvisited list

### Iteration 2:
- Visit vertex C (smallest distance = 2)
- Check neighbors B, D, and E:
  - Distance to B via C = 2 + 1 = 3 (no update needed, equal to current)
  - Distance to D via C = 2 + 1 = 3 (update from ∞)
  - Distance to E via C = 2 + 5 = 7 (update from ∞)
- Remove C from unvisited list

### Iteration 3:
- Visit vertex B (distance = 3)
- Check neighbor D:
  - Distance to D via B = 3 + 2 = 5 (no update, greater than current distance of 3)
- Remove B from unvisited list

### Iteration 4:
- Visit vertex D (distance = 3)
- Check neighbor E:
  - Distance to E via D = 3 + 3 = 6 (update from 7)
- Remove D from unvisited list

### Iteration 5:
- Visit vertex E (distance = 6)
- No unvisited neighbors
- Remove E from unvisited list

### Final Result:
- Shortest path from A to E is 6, via path A → C → D → E

## 🧩 Pseudocode

```
function Dijkstra(Graph, source):
    // Initialization
    for each vertex v in Graph:
        distance[v] = INFINITY
        previous[v] = UNDEFINED
        add v to unvisited
    
    distance[source] = 0
    
    // Update process
    while unvisited is not empty:
        u = vertex in unvisited with smallest distance
        remove u from unvisited
        
        for each neighbor v of u:
            alt = distance[u] + edge_weight(u, v)
            if alt < distance[v]:
                distance[v] = alt
                previous[v] = u
                
    return distance[], previous[]
```

## 🔑 Key Takeaways

1. Dijkstra's algorithm efficiently finds shortest paths in weighted graphs
2. It uses a greedy approach, always selecting the next vertex with minimum distance
3. The algorithm maintains distances and previous vertices to reconstruct paths
4. After completion, you can determine both the shortest distance and the actual path
5. Dijkstra's algorithm is foundational in navigation systems, network routing, and many optimization problems

Understanding Dijkstra's algorithm is essential for solving path-finding problems in various applications from transportation networks to telecommunications.