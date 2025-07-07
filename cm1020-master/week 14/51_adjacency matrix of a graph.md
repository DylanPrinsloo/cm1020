In this lesson, we will discuss two different ways of
representing graphs. The first one is the use of the adjacency list to
represent a graph. The second one is the use
of the adjacency matrix. Finally, we will discuss some properties of
the adjacency matrix. For example, the relation
between the sum of the degree sequence of a graph and its corresponding
adjacency matrix. So far we have seen
that a graph can be represented by a set of vertices and a set of
edges or connections. For example, the set V and E of the graph shown in
the slide are as follows. The set of vertices is V
which contains a, b, c, d, and e and the set of edges
E which contain e_1, e_2, e_3, e_4, e_5, e_6, and e_7. The adjacency list of
a graph G is a list of the vertices in G and their corresponding
individual adjacent vertices. For example, the adjacency list of the graph shown
below is as follow. The vertex A has B and C
as its adjacent vertices. The vertex B has A, C, and D as its
adjacent vertices. The vertex C has A, B, D, and E as its
adjacent vertices. The vertex D has B, C, and E as its
adjacent vertices. Finally, the vertex C and D are adjacent to E. Given the
following adjacency list, we want to draw the
graph it represents. Clearly, this graph
consists of five vertices. We can use the adjacency
list to draw this graph. v_1 is adjacent to
v_1, v_2, and v_3. v_2 is adjacent to
v_1, v_4, and v_5. v_3 is adjacent to v_1 and v_4. v_4 is adjacent to
v_2, v_3, and v_5. Finally, v_5 is adjacent
to v_2 and v_4. So far we have seen
that a graph can be represented by a set of
vertices and a set of edges, it's corresponding
degree sequence, and it's adjacency list. A graph can also be represented by its
corresponding adjacency matrix. For example, given
the following graph, its corresponding adjacency
list is as follow. The values highlighted in red correspond to an edge
between v_1 and v_2. The values in the
leading diagonal highlighted in orange
correspond to the loops. As you can see, the one at v_1, v_1 means that there
is a loop at v_1. Similarly, the one at v_2, v_2 means that there
is a loop at v_2, and the zero at v_3, v_3 means that there is no
loop at the vertex v_3. Let's look at the
previous graph again. As you can see, the values in blue represent the edge between v_1 and v_2, the values in green represents the edge between v_1 and v_3, whereas the values
in orange represent the parallel edges
between v_2 and v_3. Hence, apart from the loops, every other edge is represented twice in
the adjacency matrix. Hence for consistency,
we can also represent the loops twice by multiplying the values in the
leading diagonal by two. The adjacency matrix of the
graph G becomes as follow. The adjacency matrix of an
undirected graph is symmetric. This results from the fact that every edge is represented
twice in the adjacency matrix. For example, the adjacency matrix of the graph shown on
the slide is symmetric. The number of edges in an
undirected graph is equal to half the sum of all the elements m_ij of its corresponding
adjacency matrix. To put this in another way, the sum of all the elements
of the adjacency matrix of an undirected graph is equal to the sum of its corresponding
degree sequence. For example, let's consider
the same graph as before. The degree of each
vertex is added to the graph four for v_1, five for v_2, and three for v_3. The sum of the degree sequences
of this graph is equal to 5 plus 4 plus 3 which
is equal to 12. As you can see is
equal to the sum of all the elements of its
adjacency matrix which is one plus one plus one plus one plus two plus two
plus two plus two. The sum of the degree sequence
is equal to the sum of all the elements of this
adjacency matrix M. Hence, the number of edges
in this graph is equal to 12 over 2
which is equal to 6. In the following directed graph, you can see that each edge
has a defined direction. So the adjacency matrix
of G is as follow. As the direction of the
edge is considered, each edge is counted only
once in the adjacency matrix. Hence, the number of
edges is equal to the sum of all the elements
m_ij of the adjacency matrix. For example, the first row in M squared shows the number of
paths of Length 2 from v_1. One path of Length 2 to v_1 and no paths of Length 2
from v_1 to v_2 or to v_3. The second row in
the adjacency matrix squared shows the number of
paths of Length 2 from v_2. There are four paths
of Length 2 to v_1, there is one path
of Length 2 to v_2, there are two paths
of Length 2 to v_3. The third row of the
adjacency matrix squared shows the number of
paths of Length 2 from v_3. There is one path of
Length 2 to v_1 and no paths of Length 2 from
v_3 to v_2 or to v_3. In this lesson, we discussed two other ways of
representing a graph. The first one is the use
of the adjacency list, the second one is the use of the adjacency matrix
to represent a graph. Finally, we looked
at some properties. For example, the relation
between the sum of the degree sequence of a graph and its corresponding
adjacency matrix.