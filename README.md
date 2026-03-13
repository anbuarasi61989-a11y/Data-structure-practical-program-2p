# Data-structure-practical-program-2 # Graph DFS using visited array

def dfs(node, adj, visited):
    visited[node] = True
    print(node, end=" ")

    for neighbour in adj[node]:
        if not visited[neighbour]:
            dfs(neighbour, adj, visited)


# Adjacency list
adj = {
    0: [1, 2],
    1: [0, 3, 4],
    2: [0],
    3: [1],
    4: [1]
}

visited = [False] * 5

print("DFS Traversal:")
dfs(0, adj, visited)
