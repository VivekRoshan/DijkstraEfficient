# DijkstraEfficient
Readme:

 * For the classes EdgeWeightedDigraph.java and DijkstraSP.java we need to take the input from the command line argument.
 * The code will take the first argument(arg[0]) as the file name(input.txt/usa.txt etc).
 * The source and Destination are to be given in the last line of the input file(Displays an error otherwise).
 * Output gets displayed on the console(The Shorts path among source and Destination).
Note: The input file given should be present in the src folder(same project folder) of these java files as we just give the input file name(relative path) and not the actual path.

Point.java:
 * Point class is used to caputure the (x,y) coordinates of the node and for computing the euclidean distance among two vertices.

DirectedEdge.java:
 * This class represents a weighted edge in a EdgeWeightedGraph.
 * The graph given according to the requirement is a undirected/bidirectional graph. 
 * Hence a pair of vertices v,w can be considered as v -> w and w -> v. The weight is the euclidean distance between the vertices.

EdgeWeightedDigraph.java: 
 * An edge-weighted digraph is an implementation of adjacency lists. All the coded operations take constant running time. 
 * This class constructs and represents an entire graph and its adjacency list. 
 * The graph is constructed from the inputs given in the text file according to the required format.
 
DijkstraSP.java
 * This class finds a shortest path from source to the destination considering all the path possible between them where the weights are the euclidean distances between the nodes. 
 * The program takes use of a binary heap for the priority queue.
 * Regarding Running time:
 * The program takes time proportional to E'logV',where V' is the number of vertices and E' is the number of edges that the algorithm examines.
 * The methods distTo() hasPathTo() methods take constant time and the method pathTo() method takes time proportional to the number of edges in the shortest path returned.
Approach: The approach used is idea 1 of all the ideas suggested in the document. 
 * The main idea is that, we need to compute the shortest path among source and destination.
 * The classical dijkstra's algorithm finds the shortest path from source to all the other vertices of the graph.
 * Our algorithm is designed in such a way that, it computes the shortes path from source to the other vertices till the destination vertex is reached.
 * From the classical dijkstra's algorithm, the space required is quadratic, hence we try to decrease the time and space required to compute the shortest path among source and destination.
 * In order to decrease the space and time, we check the shortest paths, till the destination vertex is visited (marked[destination] becomes true). 
 * In this approach, we can say that the running time is E'logV',where V' is the number of vertices and E' is the number of edges that the algorithm examines.
 * In the classic dijstra using an adjacency list and binary heap, the running time would be ElogV where E is total number of edges and V is total number of vertices.
 * From the implemented approach, the running time is proportional to the distance between source and destination.

Time Complexity:

EdgeWeightedDigraph.java, all the methods have a constant running time.

DijkstraSP, have a running time of E'log V' where V' is the number of vertices and E' is the number of edges that the algorithm examines. 


