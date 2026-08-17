# Data Structures and Algorithms Concept Hierarchy

## Foundational Concepts

1. Variable — basic — ang lalagyan ng data na may pangalan
2. Array — basic — ang ordered na list ng values na may index
3. String — basic — ang sequence ng characters
4. Integer — basic — ang whole number na walang decimal
5. Boolean — basic — ang true o false value
6. Operator — basic — ang symbol na nagpe-perform ng operation
7. Function — basic — ang reusable block ng code na may return value
8. Index — basic — ang position ng element sa array
9. Length — basic — ang bilang ng elements sa data structure
10. Null — basic — ang absence ng value

## Core Concepts

1. Linked List — basic — ang sequence ng nodes na may pointer sa next
2. Singly Linked List — basic — ang linked list na may isang direction lang
3. Doubly Linked List — intermediate — ang linked list na may forward at backward pointers
4. Stack — basic — ang LIFO na data structure
5. Queue — basic — ang FIFO na data structure
6. Deque — intermediate — ang double-ended queue na pwedeng mag-add sa both ends
7. Circular Linked List — intermediate — ang linked list na ang last node ay naka-connect sa first
8. Head — basic — ang first node sa linked list
9. Tail — basic — ang last node sa linked list
10. Node — basic — ang element ng linked list na may data at pointer

## Implementation Concepts

1. Binary Tree — basic — ang tree na may dalawang children lang per node
2. Binary Search Tree — intermediate — ang binary tree na may ordering property
3. AVL Tree — advanced — ang self-balancing binary search tree
4. Red-Black Tree — advanced — ang self-balancing BST na may color property
5. Heap — intermediate — ang complete binary tree na may heap property
6. Min Heap — intermediate — ang heap na ang parent ay laging mas mababa
7. Max Heap — intermediate — ang heap na ang parent ay laging mas mataas
8. Hash Table — basic — ang data structure na gumagamit ng hash function
9. Hash Function — basic — ang function na nagco-convert ng key sa index
10. Collision — intermediate — ang pagkakataon na dalawang key ay may same hash
11. Graph — basic — ang collection ng vertices at edges
12. Vertex — basic — ang node sa graph
13. Edge — basic — ang connection sa pagitan ng dalawang vertices
14. Adjacency Matrix — intermediate — ang 2D array na nagre-represent ng graph
15. Adjacency List — intermediate — ang list na nagre-represent ng graph neighbors

## Integration Concepts

1. Linear Search — basic — ang pag-search sa bawat element ng isa-isa
2. Binary Search — intermediate — ang pag-search sa sorted array gamit ang divide and conquer
3. Bubble Sort — basic — ang pag-sort sa pamamagitan ng pag-swipe ng adjacent elements
4. Selection Sort — basic — ang pag-sort sa pamamagitan ng pag-select ng minimum
5. Insertion Sort — intermediate — ang pag-sort sa pamamagitan ng pag-insert ng element
6. Merge Sort — intermediate — ang divide and conquer na sorting algorithm
7. Quick Sort — intermediate — ang divide and conquer na sorting gamit ang pivot
8. Heap Sort — intermediate — ang sorting algorithm na gumagamit ng heap
9. Counting Sort — intermediate — ang non-comparison based na sorting algorithm
10. Radix Sort — advanced — ang sorting algorithm na nagso-sort digit by digit

## Architectural Concepts

1. Divide and Conquer — intermediate — ang paghahati ng problema sa mas maliliit na sub-problems
2. Greedy Algorithm — intermediate — ang pagpili ng locally optimal na choice sa bawat step
3. Dynamic Programming — advanced — ang pag-solve ng problems gamit ang memoization
4. Backtracking — advanced — ang pag-explore ng lahat ng possible na solutions
5. Recursion — intermediate — ang function na tumatawag sa sarili nito
6. Iteration — basic — ang pag-repeat ng code gamit ang loop
7. Stack Overflow — intermediate — ang error kapag naubusan ng stack space
8. Tail Recursion — intermediate — ang recursion na ang last action ay ang recursive call
9. Memoization — advanced — ang caching ng function results para hindi mag-recompute
10. Tabulation — advanced — ang bottom-up na approach ng dynamic programming

## Design Concepts

1. Time Complexity — basic — ang pagsukat ng oras na kailangan ng algorithm
2. Space Complexity — basic — ang pagsukat ng memory na kailangan ng algorithm
3. Big O Notation — basic — ang notation para sa upper bound ng complexity
4. Omega Notation — intermediate — ang notation para sa lower bound ng complexity
5. Theta Notation — intermediate — ang notation para sa tight bound ng complexity
6. Amortized Analysis — advanced — ang average-case analysis over operations
7. Best Case — basic — ang minimum na oras na kailangan ng algorithm
8. Worst Case — basic — ang maximum na oras na kailangan ng algorithm
9. Average Case — intermediate — ang average na oras na kailangan ng algorithm
10. Trade-off — intermediate — ang pagpili sa pagitan ng dalawang competing factors

## Advanced Concepts

1. Breadth-First Search — intermediate — ang pag-traverse ng graph level by level
2. Depth-First Search — intermediate — ang pag-traverse ng graph gamit ang stack
3. Dijkstra's Algorithm — advanced — ang shortest path algorithm para sa weighted graphs
4. Bellman-Ford Algorithm — advanced — ang shortest path algorithm na kaya ang negative weights
5. Floyd-Warshall Algorithm — advanced — ang all-pairs shortest path algorithm
6. Kruskal's Algorithm — advanced — ang minimum spanning tree algorithm gamit ang greedy
7. Prim's Algorithm — advanced — ang minimum spanning tree algorithm gamit ang priority queue
8. Topological Sort — intermediate — ang pag-order ng vertices sa DAG
9. Cycle Detection — intermediate — ang pag-detect ng cycle sa graph
10. Strongly Connected Components — advanced — ang maximal na set ng reachable vertices

## Production Concepts

1. Cache — basic — ang mabilis na memory na nagko-cache ng madalas na data
2. Cache Hit — basic — ang pag-access ng data na nasa cache
3. Cache Miss — basic — ang pag-access ng data na wala sa cache
4. LRU Cache — intermediate — ang cache na nagre-remove ng least recently used
5. FIFO Cache — intermediate — ang cache na nagre-remove ng oldest
6. Branch Prediction — advanced — ang CPU optimization para sa conditional branches
7. Locality of Reference — intermediate — ang pattern ng memory access
8. Spatial Locality — intermediate — ang pag-access ng malalapit na memory locations
9. Temporal Locality — intermediate — ang pag-access ng same memory location
10. Memory Leaks — intermediate — ang hindi na-garbage collect na memory

## Optimization Concepts

1. Algorithm Optimization — intermediate — ang pagpapabilis ng algorithm
2. Data Structure Selection — intermediate — ang pagpili ng tamang data structure
3. Space-Time Trade-off — intermediate — ang pagpili sa pagitan ng space at time
4. Precomputation — intermediate — ang pag-compute ng results ahead of time
5. Lazy Evaluation — intermediate — ang pag-compute lang kapag kailangan
6. Eager Evaluation — basic — ang pag-compute ng lahat agad
7. Bit Manipulation — intermediate — ang pag-optimize gamit ang bitwise operations
8. Parallel Processing — advanced — ang pag-process ng data sa multiple cores
9. Distributed Computing — advanced — ang pag-process ng data sa multiple machines
10. Streaming Algorithms — advanced — ang algorithms para sa real-time na data

## Expert/Strategic Concepts

1. NP-Completeness — advanced — ang class ng problems na hindi polynomial-time solvable
2. P vs NP Problem — advanced — ang unsolved problem sa computer science
3. Approximation Algorithms — advanced — ang algorithms na nagbibigay ng near-optimal na solutions
4. Randomized Algorithms — advanced — ang algorithms na gumagamit ng randomness
5. Online Algorithms — advanced — ang algorithms na nagpo-process ng input incrementally
6. Offline Algorithms — advanced — ang algorithms na kailangan ang buong input
7. Competitive Analysis — advanced — ang pag-compare ng online at offline algorithms
8. Amortized Complexity — advanced — ang average complexity over sequence of operations
9. Potential Method — advanced — ang technique para sa amortized analysis
10. Yao's Principle — advanced — ang lower bound technique para sa randomized algorithms
