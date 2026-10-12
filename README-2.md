# BFS vs DFS -- 26-Node (A--Z) Empirical Performance Analysis System

## Overview

This project compares Breadth-First Search (BFS) and Depth-First Search
(DFS) on a graph containing 26 nodes, labelled **A through Z**. Searches
start at node **A** and are evaluated using three goal scenarios:

-   **Best case:** goal node B
-   **Average case:** goal node M
-   **Worst case:** goal node Z

The program records the path found, the number of nodes expanded, and
execution time. It uses Python's `time.perf_counter()` to measure
runtime and is designed to use `py-spy` to sample Python call-stack
activity and produce a flame graph named `profile.svg`.

## Architecture

The system is documented using all four levels of the C4 model:

1.  **Level 1 -- System Context:** A user/researcher supplies graph and
    goal-case inputs; the system returns performance metrics and
    profiling output.
2.  **Level 2 -- Container:** Graph Input & Case Configurator, Search
    Engine, BFS Module, DFS Module, Performance Profiler, and
    Output/Results.
3.  **Level 3 -- Component:** Frontier, Visited Set, Goal Test, and Node
    Counter & Timer.
4.  **Level 4 -- Code:** `graph`, `bfs(graph, start, goal)`,
    `dfs(graph, start, goal)`, `test_cases`, and `benchmark_search()`.

The supplied diagrams are `Level1.drawio`, `Level2.drawio`,
`Level3.drawio`, and `Level4.drawio` (diagram image exports may use
`.png` filenames).

## Algorithms

### Breadth-First Search (BFS)

BFS explores the graph level by level. The architecture describes a FIFO
frontier implemented with `collections.deque`.

### Depth-First Search (DFS)

DFS explores a branch deeply before backtracking. The architecture
describes a LIFO frontier implemented with a Python list used as a
stack.

Both searches use a visited set to avoid repeated visits and cycles,
test whether the current node matches the goal, and count expanded
nodes.

## Benchmarking and profiling

-   Run each configured search case for **three iterations**.
-   Measure elapsed time with `time.perf_counter()`.
-   Calculate and report average execution time and node-expansion
    counts.
-   Use `py-spy` for sampling-based profiling and export `profile.svg`
    when profiling is available.

Runtime values depend on the environment and should be taken from the
actual program output rather than assumed from this README.

## Requirements

-   Python 3
-   `py-spy` for the optional external profiling step

Install the profiler with:

``` bash
python -m pip install py-spy
```

## Running

The submitted architecture document describes the functions and
workflow, but does not specify the implementation script's filename or
command-line interface. After identifying the Python file containing
`benchmark_search()`, run it with:

``` bash
python <your_script_name>.py
```

To profile a script with `py-spy`, use the actual script filename:

``` bash
py-spy record -o profile.svg -- python <your_script_name>.py
```

If `py-spy` is not available as a command, try invoking it through the
Python environment where it was installed, or verify that the
environment's scripts directory is on `PATH`.

## Expected output

The report describes output containing: - Search algorithm and goal
scenario - Path found - Number of nodes expanded - Execution duration /
average runtime - `profile.svg` flame graph when profiling is run
successfully

## Notes

-   This README is based on the supplied SLE-3 report and C4 diagrams.
-   The actual Python source code and measured benchmark results were
    not included among the supplied files, so this document does not
    claim specific timings or node counts.
