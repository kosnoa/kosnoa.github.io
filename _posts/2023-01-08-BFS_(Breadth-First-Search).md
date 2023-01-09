---
title: "BFS - Breadth-First Search"
date: 2022-01-08 20:41:34
categories:
- Algorithm
- C++
tags:
- C++
- BFS
- Algorithm
- Graph
---
This posting will go over about BFS (Breadth-First Search).

### What is BFS?
BFS(Breadth-First Search) is one type of alogrithm that starts from the root node (or a different abitrary node) and searches the adjacent nodes first.
* Traverses from the starting node then to the closest nodes and the nodes located far are visited later.
* Focuses on searching widely, rather than deeply.
* It is used when we want to find the closest distance between two nodes or an arbitrary path.

### Characteristics of BFS
* It is not intuitive.
* It does not work recursively.
* It is mandatory to check if the node has been visited or not (else it can be looping infinitely).
* BFS uses Queue to save the visited nodes in order and call it in order. (First In First Out)

### How does it work?
<img src="https://media.discordapp.net/attachments/1057833095505645569/1061835681472720979/bfs.gif?width=908&height=511">
<font size="1">GIF of how BFS functions</font>

The order for this example is 0-1-4-2-3.

### Source Code
```cpp
#include <bits/stdc++.h>
using namespace std;

int arr[1001][1001];
bool visited[1001][1001];
int dx[] = {-1, 0, 1, 0};
int dy[] = {0, -1, 0, 1};
queue<pair<int, int>> qp;
int n;

void bfs(int y, int x)
{
    visited[y][x] = true;
    qp.push({x,y});
    while (!qp.empty())
    {
        int first = qp.front().first;
        int second = qp.front().second;

        for (int i=0; i<4; i++)
        {
            int ny = first + dy[i];
            int nx = second + dx[i];
            
            if (0 > nx || nx >= n || 0 > ny || ny >= n)
            {
                continue;
            }

            if (arr[ny][nx] == 1 && !visited[ny][nx])
            {
                qp.push({ny, nx});
                visited[ny][nx] = true;
            }
        }
    }
}

int main()
{
    ios_base::sync_with_stdio(false), cin.tie(nullptr);

    cin >> n;

    for (int i = 0; i < n; i++)
    {
        for (int j = 0; j < n; j++)
        {
            cin >> arr[i][j];
        }
    }

    for (int i = 0; i < n; i++)
    {
        for (int j = 0; j < n; j++)
        {
            if (arr[i][j] == 1 && !visited[i][j])
            {
                bfs(i, j);
            }
        }
    }

    return 0;
}
```
