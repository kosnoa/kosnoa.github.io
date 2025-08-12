---
title: "DFS - Depth-First Search"
date: 2022-12-28 16:13:34
categories:
- Algorithm
- C++
tags:
- C++
- DFS
- Algorithm
- Graph
---

### <center>What is DFS?</center>
DFS(Depth-First Search) is one type of algorithm that traverses the entire graph data structures or tree (i.e Brute-force), which focuses on "depth". DFS starts from a node and traverses the entire branch before it moves to the next branch. For example, when searching a maze, and the direction is fixed and reaches to the end, it would return to the closest fork and start a new traverse from a node that has not been visited.
    
### <center>How does it work?</center>
Blue indicates that the node has been visited.
<!-- <img src="https://media.discordapp.net/attachments/1057833095505645569/1058068016182611988/Presentation.gif"> -->
<font size="1">GIF of how DFS functions</font>

The order for that graph would be 1-2-4-5-3-6.

Time complexity for DFS is **O(V + E)** where V is the number of verticles and E is the number of edges.

### <center>Source Code</center>

```cpp
#include <bits/stdc++.h>
using namespace std;

int arr[1000][1000];
bool visited[1000][1000];
int dx[] = {-1, 0, 1, 0};
int dy[] = {0, -1, 0, 1};
int n;

void dfs(int y, int x)
{
    visited[y][x] = true;

    for (int i=0; i<4; i++)
    {
        int nx = x + dx[i];
        int ny = y + dy[i];
        
        if (nx < 0 || nx >= n || ny < 0 || ny >= 0)
        {
            continue;
        }

        if(arr[ny][nx] == 1 && !visited[ny][nx])
        {
            dfs(ny, nx);
        }

    }
}

int main()
{
    int n;
    cin >> n;

    for(int i=0; i<n; i++)
    {
        for (int j=0; j<n; j++)
        {
            cin >> arr[i][j];
        }   
    }

    for (int i=0; i<n; i++)
    {
        for (int j=0; j<n; j++)
        {
            if (arr[i][j] == 1 && !visited[i][j])
            {
                dfs(i, j);
            }
        }
    }

    return 0;
}
```