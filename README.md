# Recursive-modularity-partitioning
Recursive Spectral Modularity Partitioning of the Karate Club

This project implements a community detection algorithm, **Recursive Spectral Modularity Partitioning**, to analyze the famous Zachary's Karate Club graph. The goal is to mathematically "discover" the social rift that split the club into two factions.

The algorithm works by:
1.  **Spectral Bisection:** Using the Fiedler vector to find the "best" way to cut the graph in two.
2.  **Modularity Check:** Using Newman's modularity score to decide if a proposed split is "good." A split is only accepted if it increases the overall modularity of the graph partitioning.
3.  **Recursion:** Applying this process recursively, splitting communities into smaller sub-communities until no more "good" splits can be found.

This repository analyzes the results by:
* Visualizing the community splits at each iteration.
* Tracking the evolution of node-level metrics (degree, betweenness, closeness, clustering) within their new communities.
* Discussing how a node's "centrality" changes depending on the context (the whole graph vs. its local community).

### Dependencies
* `networkx`
* `numpy`
* `matplotlib`
* `pandas`
