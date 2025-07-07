In this lecture, we will discuss a special type of graph
called a bipartite graph. First, we will examine the definition what a
bipartite graph is, then we will look at an
example of a bipartite graph. We will also discuss the
concept of a maximum matching. Finally, we will look at how the Hopcroft-Karp
algorithm is used to find the maximum matching
of a bipartite graph. Let's begun by defining what it means for a graph
to be bipartite. A graph G is a bipartite graph if we can divide the set of
vertices of V into two sets; V_1 and V_2, and each edge of the
graph is between one element of V_1 and
one element of V_2. Now, let's take a look at an example of a bipartite graph. The graph G is bipartite because we can divide the set
of vertices into two sets. V_1 containing A, B, C, and D and a set V_2
containing X, Y, and Z. Because each edge of
the graph is between one element of the set V_1 and one element
of the set V_2, we can make two observations. The first observation is that
the graph is two colorable. This means that we can represent the vertices of the
graph using two colors. In this example, the vertices in V_1 are orange, whereas yellow is used to
represent the vertices in V_2. The second observation
is that there are no cycles of an odd-length. For example, if we
add an edge between the vertices X and Y to
make an odd-length cycle, then the graph is not
longer bipartite graph. Considering a bipartite graph, a matching is a set of
pairwise non-adjacent edges, none of which are loops, that is no two edges
share a common endpoints. For instance, the orange edges represent a matching
in a graph G. A vertex is matched
or saturated if it is an endpoint of one of
the edges in the matching, otherwise the vertex
is unmatched. For instance, in the
graph shown here the vertex X is matched whereas the
vertex Y is unmatched. Now that we know
what a matching is, let's define a maximum matching. A maximum matching
is a matching of a maximum size such that
if any edge is added, it is no longer a matching. In other word, it's the largest possible number of edges that can still
form a matching. For instance, take the three
orange edges in this graph. They form a matching
because they don't share any
common endpoints. By adding, let's say this
red edge to the matching, it will share the same endpoint with the edge A to
X of the matching, which means that
the orange matching is a maximum matching. Note that in a bipartite graph, there might be many
possible maximum matchings. Now, let's look at how we can find a maximum matching
in a bipartite graph. The Hopcroft-Karp
algorithm is one of the most widely used
algorithms for solving the maximum matching problem
in a bipartite graph. Before running through
the algorithm, let's define three
useful key concepts. The first is an augmenting path. An augmenting path starts on a free node and
alternate between unmatched unmatched
edges ending on a free node and augments the cardinality
of the current machine. The second is
breadth-first search. A breadth-first search traverses the graph level by level, the third is depth-first search. A depth-first search
traverses a graph all the way to a leaf before
starting another path. Now let's consider the
following situation, where we have three job
positions and three candidates. The graph shows how the candidate skills match
to the job positions. For instance, candidate 2 has the right skills for
both job 1 and job 3. We will use the
Hopcroft-Karp algorithm to find the maximum matching
between candidates and jobs. This algorithm uses
two other algorithms to traverse the graph. This is the complete pseudocode for the Hopcroft-Karp algorithm. This means the from a
complete bipartite graph, a maximum cardinality
matching is produced, where each vertex
on each side is connected to exactly one
vertex on the other side. These can be represented
by a bipartite graph, and by applying the
Hopcroft-Karp algorithm, we can have a maximum matching where each candidate
is matched to a job. The graph starts with all
the nodes in each side of the graph where C and
J have no pairings. On the first iteration
of the algorithm, the breadth-first
search starts from all the three nodes
in C. For C_1, this tree is produced
connecting C_1 to J_2 and J_3. For C_2, the tree
connects to J_1 and J_3, and the final tree
produced start at C_3 connecting to J_1 and J_2. The layout with three
vertices in J has been found, and so the first part of
the iteration terminates. A path is found from
node J_2 up to C_1, and this path is removed from the layer trees
leaving J_3 unfilled, which is then also removed, this path is used to
augment the matching. The same process is followed
for J_1 with a part found to C_2 which leaves the vacancy J_3 unfilled and the
iteration therefore ends. At this point, we have
a semi matched graph. In the second iteration the depth first search
starts from node C_3, the only remaining free node in C and alternate
between unmarked edges and marked ages J_3 to
C_2 to the J_1 to C_3. An augmenting path is
found from J_3 up to C_3. This is the maximum
cardinality matching for this graph and every
job seeker is happy. In this lecture, we began by defining
a bipartite graph. Then we looked at an example
of a bipartite graph. Next we define a
maximum matching, we finally used the
Hopcroft-Karp algorithm to find a maximum matching.