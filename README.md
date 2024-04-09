# CSCM64_Lab06
## Software Testing

## Exercise 1
## Exercise 1

A subset $C \subseteq \mathbb{R}^2$ of the Euclidean plane is called convex if for all points $p, q \in C$ the line segment joining $p$ and $q$ is contained in $C$. In coordinates, this means that we have $&alpha;p + (1-&alpha;)q \in C$ for all $&alpha; \in [0,1]$ and all $p, q \in C$.

For every subset $S \subseteq \mathbb{R}^2$ of the Euclidean plane, there exists a smallest convex set containing $S$. This set is called the convex hull of $S$.

A (convex) polygon $P$ is the convex hull of a finite set of points. It can be specified by a sequence of points $(p_0, ..., p_{n-1})$ such that the boundary of $P$ is the union of the line segments joining $p_i$ and $p_{i+1}$ for $i = 1, ..., n-1$ and the line segment joining $p_{n-1}$ and $p_0$.

Consider the computational problem Convex Hull, specified below:

- **Input:** A non-empty finite list $(p_0, ..., p_{n-1})$ of points in the plane. Each point is given by a pair of 32-bit floating point numbers.
- **Output:** A finite list $(i_1, ..., i_m)$ of indexes such that the convex hull of the set $\{p_0, ..., p_{n-1}\}$ is the polygon specified by the sequence $(p_{i_1}, ..., p_{i_m})$.

For example, on input $(0,0),(1,1),(0,1),(1,0),(0.5,0.5)$, the sequences $(0,3,1,2)$ and $(1,3,0,2)$ are valid outputs. For the same input, the sequences $(0,1,3,2)$ and $(0,4,3)$ are examples of invalid outputs.

The Java class `GiftWrap` in the Code for this lab implements Jarvis’s wrapping algorithm to solve the Convex Hull problem.


**Tasks.**
1. Suggest two or three different partitions of the domain of valid inputs that are suitable for
testing an implementation of the Convex Hull problem.
2. Derive test inputs for the problem based on your partitions using SimultaneousWeak Equivalence
Testing.
3. Describe a method for computing for a given input all valid outputs to the Convex Hull problem from one given valid output.
Use this to correctly implement the method `defineEqualConvexHulls` in the Java code. The method should take two lists of integers $L1=\{i_1, ..., i_m\}$ and $L2=\{j_1, ..., j_m\}$, and a list
of points $P=\{p_0, ..., p_{n-1}\}$, and decide whether the polygons defined by $\{p_{i_1}, ..., p_{i_m}}\$ and $\{p_{j_1}, ..., p_{j_k}}\$.


5. Implement your test suite using JUnit to test the implementation of Convex Hull provided in the Java code.
