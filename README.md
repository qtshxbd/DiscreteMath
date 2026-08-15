# Discrete Math Toolkit

A Python library implementing core discrete mathematics building blocks —
built alongside Math 55 coursework (combinatorics, graph theory, number
theory).

## Features

- **`combinatorics.py`** — permutations and combinations (counts and
  enumerations), inclusion-exclusion, and the pigeonhole principle.
- **`graphs.py`** — an adjacency-list `Graph` class with BFS, DFS,
  connectivity checks, and cycle detection (both directed and undirected).
- **`number_theory.py`** — primality testing, Sieve of Eratosthenes,
  GCD/LCM, extended Euclidean algorithm, modular inverse, and fast modular
  exponentiation.

## Quick start

```bash
git clone https://github.com/qtshxbd/DiscreteMath.git
cd DiscreteMath
pip install -r requirements.txt   # only needed for running tests

python -m discrete_math.combinatorics
python -m discrete_math.graphs
python -m discrete_math.number_theory
```

## Example

```python
from discrete_math.graphs import Graph

g = Graph()
for u, v in [("A", "B"), ("B", "C"), ("C", "D"), ("D", "A")]:
    g.add_edge(u, v)

g.bfs("A")        # ['A', 'B', 'D', 'C']
g.has_cycle()      # True
```

## Running tests

```bash
python -m pytest tests/ -v
```

## Possible extensions

- Dijkstra's / A* shortest-path for weighted graphs
- RSA toy implementation using the number theory module
- Visualizations of graphs with `networkx` + `matplotlib`

## License

MIT
