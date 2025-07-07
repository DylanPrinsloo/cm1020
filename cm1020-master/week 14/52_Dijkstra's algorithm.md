In this lecture, we will
cover the following; first we will examine the
concept of weighted graphs. Then we will look Dijkstra's
algorithm which is used to compute the shortest path between two vertices
in a weighted graph. We will move on to define
Dijkstra's algorithm through an example demonstrating how Dijkstra's algorithm
works in practice. Finally, we will look at the pseudocode
of this algorithm. Weighted graph is a graph
in which each edge is assigned a numerical value as you can see in the
graph shown here. It can be used to model the
distance between cities, the response time in a
communication network, or the cost of a
transaction for example. In 1956, Edsger Dijkstra
a famous computer scientist introduced
an algorithm to compute the shortest path between any two nodes in a graph. This algorithm is known
as Dijkstra's algorithm. Now let's have a
look at an example demonstrating how Dijkstra's
algorithm works in practice. Here is the graph G,
our aim is to find the shortest path from a vertex A to every other vertex
in the graph G. The first column of this table contains all the
vertices of the graph G. The second column is
used to keep track of the shortest distance from the vertex A to any
other vertex of G, and the third column keeps track of the previous
visited vertices. A list called unvisited
is used to keep track of the vertices of the graph G that have
not been visited yet. Dijkstra's algorithm
works in two steps. The first step is
the initialization. The distance from the vertex A to all vertices in G is
initialized as follows; the distance from the vertex A to itself is equal to zero. The distance from the vertex A to all other vertices is
initially unknown, and will be initialized
to infinity. Also, the previous vertex is
initialized to undefined. At this stage, the
unvisited list is updated and every node
of the graph is added. The second step, the update step, is as follows; in
this first iteration, we will start by visiting
the unvisited vertex with the smallest known distance from the vertex A which
is the start vertex. We then examine its
unvisited neighbors B and C, and calculate the distance of each neighbor from
the start vertex A. The distance from A to B
is 0 plus 3 which is 3, the distance from A to C
is 0 plus 2 which is 2, as the calculated
distances for B and C are less than the known
shortest distance which were equal to infinity. The shortest distance is
then updated for B and C, and as we visited B and C via A, we also write this information in the previous vertex column. Finally, we update
the unvisited list by removing the vertex A. In the second iteration, we start by visiting
the unvisited vertex with the smallest known
distance from the start vertex, which is the vertex C. Then we examine its
unvisited neighbors B, D and E, and calculate the distance of each neighbor
from the start vertex A. The distance from A to B
is 2 plus 1 which is 3. The distance from A to D, is 2 plus 1 which is 3. The distance from A to E
is 2 plus 5 which is 7, as the calculated distances
of D and E are less than the known shortest distance which were equal to infinity. We can update the shortest
distances in our table. As we visit D and E
via the vertex C, we'll also write this information in the previous vertex column. Finally, we update
the unvisited list by removing the vertex C to
avoid visiting it again. In this third iteration, we start by visiting
the unvisited vertex with the smallest known
distance from the start vertex. Lets choose B. Then we examine its
unvisited neighbor D and calculate its distance
from the start vertex A. The distance from A to D
is 3 plus 2 which is 5, as the calculated
distance for D is greater than the known shortest distance which was equal to three, we won't update our table. Finally, we update
the unvisited list by removing the vertex B to
avoid visiting it again. In this fourth iteration, we start by visiting the unvisited vertex with the smallest known distance from the start vertex which is the vertex D. Then we examine
its unvisited neighbor E, and calculate its distance
from the start vertex A, which is 3 plus 3
which is equal to 6. The calculated
distance for E is less than the known shortest
distance which was seven. The shortest distance
to E is then updated, and as we visited E via D, we will also write
this information in the previous vertex column. Finally, we'll update
the unvisited list by removing the vertex D to
avoid visiting it again. In this fifth iteration, we start by visiting the last
unvisited vertex which is the vertex E. E doesn't have
any unvisited neighbors. So our table is complete. We only need to update the
unvisited vertices list. As a result of
Dijkstra's algorithm, we have a complete table of the shortest distance from
A to any other vertex, and the previous
path to that vertex. For instance, the shortest path distance
from A to E is 6, and the path can be built from the previous vertex
column A to C, to D, to E. We can put together all the steps that
we have just learn through in the example
into a pseudocode. In doing this, we can
identify two main part; initializing the table for
all the graph's vertices, visiting iteratively
all the vertices and updating their shortest
distance and previous vertex. We began this lecture by examining the concept
of weighted graphs. Then we introduce
Dijkstra's algorithm and showed via an example how this algorithm
is used to compute the shortest path between two
vertices of weighted graph. Finally, we put together all the steps shown in this
example onto a pseudocode.