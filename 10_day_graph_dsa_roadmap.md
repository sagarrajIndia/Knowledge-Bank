# 🗺️ 10-Day Graph Data Structures & Algorithms Roadmap

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![LeetCode Track](https://img.shields.io/badge/LeetCode-Graph%20Curriculum-FFA116?logo=leetcode&logoColor=black)](https://leetcode.com/)
[![Track Progress](https://img.shields.io/badge/Progress-0%2F10%20Days-brightgreen)](#-day-1-foundations--graph-representations)

A comprehensive, logically sequenced 10-day roadmap designed to master graph theory, core graph algorithms, and coding interview problem patterns. Each day pairs core theory with top video tutorials, interactive visualizations, and curated practice problems.

---

## 📑 Table of Contents

- [Complexity Reference Sheet](#-complexity-reference-sheet)
- [Day 1: Foundations & Graph Representations](#-day-1-foundations--graph-representations)
- [Day 2: Fundamental Traversals (BFS & DFS)](#-day-2-fundamental-traversals-bfs--dfs)
- [Day 3: Cycle Detection & Bipartite Graphs](#-day-3-cycle-detection--bipartite-graphs)
- [Day 4: Directed Acyclic Graphs (DAGs) & Topological Sort](#-day-4-directed-acyclic-graphs-dags--topological-sort)
- [Day 5: Disjoint Set Union (DSU) & Minimum Spanning Trees (MST)](#-day-5-disjoint-set-union-dsu--minimum-spanning-trees-mst)
- [Day 6: Single-Source Shortest Paths (Dijkstra & 0-1 BFS)](#-day-6-single-source-shortest-paths-dijkstra--0-1-bfs)
- [Day 7: All-Pairs Shortest Paths & Negative Weights](#-day-7-all-pairs-shortest-paths--negative-weights)
- [Day 8: Bridges & Articulation Points (Tarjan's Algorithm)](#-day-8-bridges--articulation-points-tarjans-algorithm)
- [Day 9: State-Space Search & Bidirectional BFS](#-day-9-state-space-search--bidirectional-bfs)
- [Day 10: Advanced Grid Graphs & Backtracking](#-day-10-advanced-grid-graphs--backtracking)
- [Recommended Visualizers & Resources](#-recommended-visualizers--resources)

---

## 📊 Complexity Reference Sheet

| Algorithm | Primary Use Case | Time Complexity | Auxiliary Space |
| :--- | :--- | :--- | :--- |
| **BFS / DFS** | Traversal, Components, Unweighted Shortest Path | $O(V + E)$ | $O(V)$ |
| **Kahn's (Topo Sort)** | Dependency resolution, DAG cycle check | $O(V + E)$ | $O(V)$ |
| **Kruskal's (with DSU)** | Minimum Spanning Tree (sparse graphs) | $O(E \log E)$ | $O(V)$ |
| **Prim's** | Minimum Spanning Tree (dense graphs) | $O(E \log V)$ | $O(V)$ |
| **Dijkstra's** | Single-Source Shortest Path (non-negative weights) | $O((V + E) \log V)$ | $O(V)$ |
| **Bellman-Ford** | SSSP (handles negative edge weights & cycles) | $O(V \cdot E)$ | $O(V)$ |
| **Floyd-Warshall** | All-Pairs Shortest Path | $O(V^3)$ | $O(V^2)$ |
| **Tarjan's (Bridges)** | Critical connections & single points of failure | $O(V + E)$ | $O(V)$ |

---

## 📅 Roadmap Breakdown

### 📌 Day 1: Foundations & Graph Representations
Understand fundamental graph terminology and memory trade-offs across representations.

- [ ] **Theory to Cover:**
  - Vertices, directed vs. undirected, weighted vs. unweighted, cyclic vs. acyclic.
  - **Edge List:** Space $O(E)$, lookup $O(E)$.
  - **Adjacency Matrix:** Space $O(V^2)$, lookup $O(1)$, neighbor iteration $O(V)$.
  - **Adjacency List:** Space $O(V + E)$, neighbor iteration $O(\text{deg}(u))$.
- 🎥 **Video Lessons:**
  - [Graph Representation: Adjacency Matrix & List (Jenny's Lectures)](http://www.youtube.com/watch?v=5hPfm_uqXmw)
  - [4 Ways to Represent Graph Data Structures (Greg Hogg)](http://www.youtube.com/watch?v=J_C3sUVH4ZE)
- 💻 **Hands-On Tasks:**
  - [ ] Implement an undirected, weighted graph using an Adjacency List.
  - [ ] Write a helper function to convert an Edge List to an Adjacency Matrix.

---

### 📌 Day 2: Fundamental Traversals (BFS & DFS)
Master iterative level-order traversal and recursive deep path exploration.

- [ ] **Theory to Cover:**
  - **Breadth-First Search (BFS):** Queue-based level exploration, finding unweighted shortest paths ($O(V + E)$).
  - **Depth-First Search (DFS):** Stack/recursion traversal, backtracking, component counting ($O(V + E)$).
  - 2D grid graph modeling (cells as vertices, adjacent moves as edges).
- 🎥 **Video Lessons:**
  - [Graph Traversals: BFS & DFS (Abdul Bari)](http://www.youtube.com/watch?v=pcKY4hjDrxk)
  - [BFS & DFS Complete Guide (Jenny's Lectures)](http://www.youtube.com/watch?v=vf-cxgUXcMk)
- 💻 **Practice Problems:**
  - [ ] [LeetCode 200: Number of Islands](https://leetcode.com/problems/number-of-islands/)
  - [ ] [LeetCode 133: Clone Graph](https://leetcode.com/problems/clone-graph/)
  - [ ] [LeetCode 1971: Find if Path Exists in Graph](https://leetcode.com/problems/find-if-path-exists-in-graph/)

---

### 📌 Day 3: Cycle Detection & Bipartite Graphs
Detect cycles across directed and undirected graphs, and validate bipartite properties.

- [ ] **Theory to Cover:**
  - Cycle detection in undirected graphs using parent pointers in BFS/DFS.
  - Cycle detection in directed graphs using 3-state tracking (unvisited, visiting, visited).
  - Bipartite graph verification using 2-coloring.
- 🎥 **Video Lessons:**
  - [Detect Cycle in Undirected Graph using BFS (take U forward)](http://www.youtube.com/watch?v=BPlrALf1LDU)
  - [Cycle Detection in Directed Graph (Techdose)](http://www.youtube.com/watch?v=0dJmTuMrUZM)
- 💻 **Practice Problems:**
  - [ ] [LeetCode 785: Is Graph Bipartite?](https://leetcode.com/problems/is-graph-bipartite/)
  - [ ] [GFG: Detect Cycle in an Undirected Graph](https://www.geeksforgeeks.org/problems/detect-cycle-in-an-undirected-graph/1)
  - [ ] [GFG: Detect Cycle in a Directed Graph](https://www.geeksforgeeks.org/problems/detect-cycle-in-a-directed-graph/1)
  - [ ] [InterviewBit: Black Shapes](https://www.interviewbit.com/problems/black-shapes/)

---

### 📌 Day 4: Directed Acyclic Graphs (DAGs) & Topological Sort
Handle ordering dependencies and dependency resolution in acyclic graphs.

- [ ] **Theory to Cover:**
  - Kahn's Algorithm (in-degree reduction using BFS).
  - DFS-based Topological Sort (reverse post-order).
  - Cycle detection inside DAG-based workflows.
- 🎥 **Video Lessons:**
  - [Topological Sort | Kahn's Algorithm (WilliamFiset)](http://www.youtube.com/watch?v=cIBFEhD77b4)
  - [Topological Sort DFS (Tushar Roy)](http://www.youtube.com/watch?v=ddTC4Zovtbc)
- 💻 **Practice Problems:**
  - [ ] [LeetCode 207: Course Schedule](https://leetcode.com/problems/course-schedule/)
  - [ ] [LeetCode 210: Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
  - [ ] [LeetCode 802: Find Eventual Safe States](https://leetcode.com/problems/find-eventual-safe-states/)

---

### 📌 Day 5: Disjoint Set Union (DSU) & Minimum Spanning Trees (MST)
Group elements dynamically and compute minimum-weight connected subgraphs.

- [ ] **Theory to Cover:**
  - **Disjoint Set Union (DSU):** Path compression and union by rank/size ($O(\alpha(V))$).
  - **Kruskal's Algorithm:** Greedy edge selection using DSU ($O(E \log E)$).
  - **Prim's Algorithm:** Cut-property selection using min-priority queues ($O(E \log V)$).
- 🎥 **Video Lessons:**
  - [Prim's & Kruskal's Algorithms (Abdul Bari)](http://www.youtube.com/watch?v=4ZlRH0eK-qQ)
  - [Kruskal's Algorithm in 2 Minutes (Michael Sambol)](http://www.youtube.com/watch?v=71UQH7Pr9kU)
- 💻 **Practice Problems:**
  - [ ] [LeetCode 684: Redundant Connection](https://leetcode.com/problems/redundant-connection/)
  - [ ] [LeetCode 1584: Min Cost to Connect All Points](https://leetcode.com/problems/min-cost-to-connect-all-points/)
  - [ ] [InterviewBit: Commutable Islands](https://www.interviewbit.com/problems/commutable-islands/)

---

### 📌 Day 6: Single-Source Shortest Paths (Dijkstra & 0-1 BFS)
Determine optimal paths on weighted networks with non-negative costs.

- [ ] **Theory to Cover:**
  - **Dijkstra's Algorithm:** Greedy relaxation using a min-heap ($O((V + E) \log V)$).
  - **0-1 BFS:** Double-ended queue (`deque`) optimization for edge weights restricted to $\{0, 1\}$ in $O(V + E)$.
- 🎥 **Video Lessons:**
  - [Dijkstra's Algorithm - Single Source Shortest Path (Abdul Bari)](http://www.youtube.com/watch?v=XB4MIexjvY0)
  - [Dijkstra's Algorithm in 3 Minutes (Michael Sambol)](http://www.youtube.com/watch?v=_lHSawdgXpI)
- 💻 **Practice Problems:**
  - [ ] [LeetCode 743: Network Delay Time](https://leetcode.com/problems/network-delay-time/)
  - [ ] [LeetCode 1391: Check if There is a Valid Path in a Grid](https://leetcode.com/problems/check-if-there-is-a-valid-path-in-a-grid/)
  - [ ] [InterviewBit: Smallest Multiple with 0 and 1](https://www.interviewbit.com/problems/smallest-multiple-with-0-and-1/)

---

### 📌 Day 7: All-Pairs Shortest Paths & Negative Weights
Compute distances between all pairs of vertices and handle negative edge weights.

- [ ] **Theory to Cover:**
  - **Bellman-Ford Algorithm:** Edge relaxation dynamic programming; detecting negative-weight cycles ($O(V \cdot E)$).
  - **Floyd-Warshall Algorithm:** DP-based matrix relaxation: $D^k[i][j] = \min(D^{k-1}[i][j], D^{k-1}[i][k] + D^{k-1}[k][j])$ ($O(V^3)$).
  - **Johnson's Algorithm:** Reweighting graph edges using Bellman-Ford, then running Dijkstra from every vertex.
- 🎥 **Video Lessons:**
  - [Floyd-Warshall All-Pairs Shortest Path (Abdul Bari)](http://www.youtube.com/watch?v=oNI0rf2P9gE)
  - [Bellman-Ford Algorithm (Abdul Bari)](http://www.youtube.com/watch?v=FtN3BYH2Zes)
- 💻 **Practice Problems:**
  - [ ] [LeetCode 1334: City With Smallest Number of Neighbors at a Threshold](https://leetcode.com/problems/find-the-city-with-the-smallest-number-of-neighbors-at-a-threshold-distance/)
  - [ ] [LeetCode 787: Cheapest Flights Within K Stops](https://leetcode.com/problems/cheapest-flights-within-k-stops/)
  - [ ] [CP-Algorithms: Johnson's Algorithm Reference](https://cp-algorithms.com/graph/all-pair-shortest-path-johnson.html)

---

### 📌 Day 8: Bridges & Articulation Points (Tarjan's Algorithm)
Find critical edges and single points of failure that disconnect the graph.

- [ ] **Theory to Cover:**
  - Discovery time (`tin`) and lowest reachable ancestor time (`low`).
  - Bridge condition: $\text{low}[v] > \text{tin}[u]$.
  - Articulation point condition: $\text{low}[v] \ge \text{tin}[u]$ (handling the root node separately).
- 🎥 **Video Lessons:**
  - [Bridges in Graph using Tarjan's Algorithm (take U forward)](http://www.youtube.com/watch?v=qrAub5z8FeA)
  - [Articulation Points & Biconnected Components (Abdul Bari)](http://www.youtube.com/watch?v=jFZsDDB0-vo)
- 💻 **Practice Problems:**
  - [ ] [LeetCode 1192: Critical Connections in a Network](https://leetcode.com/problems/critical-connections-in-a-network/)
  - [ ] [GFG: Articulation Point - I](https://www.geeksforgeeks.org/problems/articulation-point-1/1)
  - [ ] [LeetCode 924: Minimize Malware Spread](https://leetcode.com/problems/minimize-malware-spread/)

---

### 📌 Day 9: State-Space Search & Bidirectional BFS
Treat complex game boards, puzzles, and string transformations as graph state machines.

- [ ] **Theory to Cover:**
  - Problem modeling: defining distinct game states as vertices and valid moves as edges.
  - Bidirectional BFS to prune branching factor from $O(b^d)$ down to $O(b^{d/2})$.
- 🎥 **Video Lessons:**
  - [Word Ladder - Breadth First Search (NeetCode)](https://www.youtube.com/results?search_query=neetcode+word+ladder)
  - [Bidirectional BFS Tutorial (GeeksforGeeks)](https://www.geeksforgeeks.org/bidirectional-search/)
- 💻 **Practice Problems:**
  - [ ] [InterviewBit: Knight on the Chessboard](https://www.interviewbit.com/problems/knight-on-chess-board/)
  - [ ] [LeetCode 127: Word Ladder](https://leetcode.com/problems/word-ladder/)
  - [ ] [LeetCode 126: Word Ladder II](https://leetcode.com/problems/word-ladder-ii/)

---

### 📌 Day 10: Advanced Grid Graphs & Backtracking
Consolidate grid searches, boundary flood fills, and state tracking.

- [ ] **Theory to Cover:**
  - Boundary-connected traversal (reverse thinking: flood-fill inward from boundaries).
  - Backtracking on 2D matrices while preventing cycles and preserving visited paths.
  - Multi-pointer priority generation on state transitions.
- 🎥 **Video Lessons:**
  - [Surrounded Regions Solution (NeetCode)](https://www.youtube.com/results?search_query=neetcode+surrounded+regions)
  - [Word Search Backtracking (NeetCode)](https://www.youtube.com/results?search_query=neetcode+word+search)
- 💻 **Practice Problems:**
  - [ ] [LeetCode 130: Surrounded Regions / Capture Regions on Board](https://leetcode.com/problems/surrounded-regions/)
  - [ ] [LeetCode 79: Word Search](https://leetcode.com/problems/word-search/)
  - [ ] [LeetCode 212: Word Search II](https://leetcode.com/problems/word-search-ii/)
  - [ ] [InterviewBit: Smallest Sequence with Given Primes](https://www.interviewbit.com/problems/smallest-sequence-with-given-primes/)

---

## 🛠️ Recommended Visualizers & Resources

- [VisuAlgo Graph Traversal & SSSP](https://visualgo.net/en) — Step-by-step graphical visualizer for tracing DFS, BFS, Dijkstra, and Kruskal algorithms.
- [CP-Algorithms (Graph Section)](https://cp-algorithms.com/) — Theoretical proofs, edge cases, and clean implementations.
- [CS Academy Graph Editor](https://csacademy.com/app/graph_editor/) — Create and test custom graphs visually.

---

## 📝 How to Use This Repository

1. **Fork or Star** this repository to keep it in your GitHub dashboard.
2. Clone it locally:
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   ```
3. Commit your solutions inside structured daily directories (`/Day01`, `/Day02`, etc.).
4. Check off the items directly in this `README.md` as you complete each topic and problem!