# CSCI210 Assignment 6 - Sample Data Files

This folder contains sample data files for testing your implementations in Assignment 6.

## Files Included

### 1. tasks.csv
Contains 20 sample tasks with the following columns:
- `task_id`: Unique identifier for each task (integer)
- `task_name`: Description of the task (string)
- `priority`: Priority level (1 = highest priority, 4 = lowest)
- `time_estimate`: Estimated time to complete in hours (float)

**Usage:** Test your priority queue and task scheduler implementation.

### 2. network.txt
Contains 31 weighted edges representing a network graph with nodes A-P.
Format: `node1 node2 weight` (space-separated)

**Characteristics:**
- 16 nodes (A through P)
- 31 edges
- Weights range from 1.0 to 7.0
- Suitable for testing Dijkstra's algorithm

**Usage:** Test your graph implementation and shortest path algorithms.

### 3. social_network.json
Contains a social network with 20 users and their connections.

**Structure:**
- `users`: Array of 20 user names
- `connections`: Array of user pairs representing friendships
- `metadata`: Additional information about the network

**Characteristics:**
- 20 users (Alice through Tara)
- 38 undirected connections
- Forms a connected graph (all users are reachable from any starting point)
- Average degree: 3.8 connections per user

**Usage:** Test graph traversals, connected components, and social network analysis.

## Testing Suggestions

### For Priority Queues (Part 1):
1. Load tasks from `tasks.csv`
2. Insert them into your priority queue
3. Extract tasks in priority order
4. Verify that priority 1 tasks come out first

### For Graphs (Part 2):
1. Build a graph from `network.txt`
2. Run Dijkstra's algorithm from node 'A'
3. Find shortest paths to all other nodes
4. Test BFS/DFS traversals

### For Social Network Analysis:
1. Load the social network from JSON
2. Calculate degree centrality
3. Find connected components (should be 1 if fully connected)
4. Calculate shortest paths between users
5. Find the average path length

## Expected Results (for validation)

### Task Scheduling
Tasks should be processed in this priority order:
- Priority 1: Tasks 1, 4, 8, 11, 20 (executed first)
- Priority 2: Tasks 2, 5, 7, 12, 16, 18 (executed second)
- Priority 3: Tasks 3, 10, 13, 15, 17, 19 (executed third)
- Priority 4: Tasks 6, 14 (executed last)

### Network Graph
Some shortest paths from A:
- A to B: 4.0 (direct)
- A to C: 2.0 (direct)
- A to E: 6.0 (A→C→B→E)
- A to F: 4.0 (A→C→F)

### Social Network
- Most connected users: Kate (6 connections), Frank (5 connections)
- Least connected users: Several users with 3 connections each
- Network diameter: Approximately 5-6 (longest shortest path)

## Notes
- All files use standard formats (CSV, space-delimited text, JSON)
- Edge weights in network.txt are floats for compatibility with Dijkstra's algorithm
- The social network is undirected (friendships are bidirectional)
- Feel free to modify these files or create your own test cases
