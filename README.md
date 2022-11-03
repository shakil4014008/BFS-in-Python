# BFS-in-Python

class Solution:
    # bfs on a connected, directed graph
    def bfsOfGraph(self, V, adj):
        que = [0]
        visited = [0] * V
        visited[0] = 1
        result = []
        while que:
            node = que.pop(0)
            #append result here as it is level by level
            result.append(node) 
            for nei in adj[node]:
                if visited[nei] == 0:
                    visited[nei] = 1
                    que.append(nei)
        return result
