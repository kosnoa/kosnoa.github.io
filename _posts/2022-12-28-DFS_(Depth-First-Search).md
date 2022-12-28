---
title: "DFS - Depth-First Search (WIP)"
date: 2022-12-28 16:13:34
categories:
- Algorithm
- C++
tags:
- C++
- DFS
- Algorithm
---
This posting will go over about DFS (Depth-First Search).

### What is DFS?
DFS(Depth-First Search) is an algorithm is that one type of algorithm that traverses the entire graph data structures or tree (i.e Brute-force), which focuses on "depth". DFS starts from a node and traverses the entire branch before it moves to the next branch. For example, when searching a maze, and the direction is fixed and reaches to the end, it would return to the closest fork and start a new traverse from a node that has not been visited.

### How does it work?

### Source Code (My personal Template)

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