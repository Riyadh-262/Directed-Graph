# Directed-Graph
Randomly Generate a Directed Graph Represented by Adjacency Matrix Using C Program
This C program demonstrates the creation and analysis of a directed graph using the adjacency matrix representation. The primary goals are to:
1. Randomly generate a graph structure.
2. Calculate the total sum of in-degrees and out-degrees.
3. Measure the execution time to observe performance scaling with increasing graph size.

📐 Graph Representation
The graph is represented by a two-dimensional array, int adj[NODE][NODE], where NODE is defined as $5000$.
 If adj[i][j] = 1, there is a directed edge from vertex $i$ to vertex $j$.
 If adj[i][j] = 0, there is no directed edge from vertex $i$ to vertex $j$.

✨ Features
Random Generation: Uses rand() % 2 to create edges randomly, resulting in a dense graph where any edge exists with a 50% probability.
Degree Calculation: Computes the in-degree and out-degree for all vertices.
Verification: Confirms the graph theory principle that the sum of all in-degrees is equal to the sum of all out-degrees (which equals the total number of edges).
Performance Analysis: Measures the execution time for graph sizes from $1000$ to $5000$ vertices using the clock() function.

🛠️ Prerequisites
A C compiler (like GCC).

🚀 How to Compile and Run
Save the code: Save the provided C code into a file named Directed_Graph.c.
Compile the program using a C compiler: gcc Directed_Graph.c -o graph_analyzer
Run the executable: ./graph_analyzer

📊 Expected Output
The program will output the results for five different graph sizes, demonstrating how the time required (in milliseconds) increases as the number of vertices, $N$, and consequently the size of the adjacency matrix ($N^2$), grows.

Vertices = 1000
In-degree = XXXX
Out-degree = XXXX
The sum of in_degrees and out_degrees are equal.
Required time = XX.XX ms

Vertices = 2000
In-degree = XXXX
Out-degree = XXXX
The sum of in_degrees and out_degrees are equal.
Required time = XX.XX ms
...

⚙️ Time Complexity Analysis
The complexity of the core operations, Generation and Degree Calculation, is dominated by the nested loops that iterate through the $N \times N$ adjacency matrix:
Function,Complexity,Notes
generateDirectedGraph(N),O(N2),Iterates through all N2 cells.
getInDegree(N),O(N2),Iterates through all N2 cells.
getOutDegree(N),O(N2),Iterates through all N2 cells.
