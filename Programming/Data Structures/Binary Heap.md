# Basics
A Binary Heap (not to be confused for the memory allocator heap) is a data structure which reduces the nodelike structure of a binary tree, into a 1 dimensional array, with indexing rules:
```
struct BinaryHeap<T> {
	heap: Vec<T>
}
```
We consider the first element of the heap to be the root node, and the next two elements, e.g. `BinaryHeap.heap[1..=2]` to be their children. The next 4 consecutive elements will belong to the left and right children of those two nodes, so on and so forth. We can attach these indexing rules as:
``` Rust
// Returns index of parent
fn parent(i: usize) -> usize {
	(i-1)/2
}
// Returns index of left child
fn left_child(i: usize) -> usize {
	i*2+1
}
// Returns index of right child
fn right_child(i: usize) -> usize {
	i*2+2
}
```
While incredibly useful due to its good cache locality and quick index calculation, it is not very space efficient, as it occupies a space of $2^d$ elements depending on the depth of the tree $d$. This is however, useful when you know your tree will be balanced, and either way it is useful for implementing a min or max heap for priority queues.
# Priority Queue
The priority queue works using a binary heap, which is ordered using `shift_up` and `shift_down` operations, and whose elements can be obtained via `push` and `pop`, similar to a regular queue. The difference between a standard queue, which is FIFO, a priority queue goes in order of some ordering.
