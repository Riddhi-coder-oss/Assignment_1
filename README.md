# Find Directly Connected Vertices

# Number of vertices
n = int(input("Enter number of vertices: "))

# Create adjacency list
graph = []

for i in range(n):
    graph.append([])

# Number of edges
e = int(input("Enter number of edges: "))

# Accept edges
print("Enter the edges (u v):")

for i in range(e):
    u, v = map(int, input().split())

    # Undirected graph
    graph[u].append(v)
    

graph[v].append(u)

# Display adjacency list
print("\nAdjacency List:")

for i in range(n):
    print(i, "->", graph[i])

# Select a vertex
selected = int(input("\nEnter the vertex to find its direct neighbours: "))

# Display neighbours
print("Direct neighbours of vertex", selected, ":")

for vertex in graph[selected]:
    print(vertex, end=" ")

# Number of connections
print("\nNumber of direct connections:", len(graph[selected]))
