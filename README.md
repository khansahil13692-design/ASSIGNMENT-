# ASSIGNMENT-
BC2025532
sahil khan


Q2. Circular Queue Using Array

Definition of Circular Queue A Circular Queue is a linear data structure that follows the FIFO (First In, First Out) principle. It is implemented using an array in which the last position is connected to the first position, forming a circular structure. In a circular queue, when the REAR reaches the last index, it can move back to the first index if space is available. Main Operations
ENQUEUE(x): Adds an element x at the rear of the queue. DEQUEUE(): Removes an element from the front of the queue. FRONT(): Returns the element present at the front without removing it. DISPLAY(): Displays all elements currently present in the queue.

Full and Empty Conditions
Queue Empty The queue is empty when there is no element available for deletion. Condition: FRONT = -1 Queue Full The queue is full when the next position of REAR is equal to FRONT. Condition: (REAR + 1) % SIZE == FRONT This condition helps the circular queue correctly distinguish between full and empty states.

How Circular Queue Works A circular queue uses two pointers: FRONT: Points to the first element. REAR: Points to the last element. When REAR reaches the last position of the array, it can return to position 0. Similarly, FRONT also moves circularly. Learn more

Why Circular Queue Provides Better Memory Utilization? In a linear queue, when elements are deleted from the front, the empty positions at the beginning may remain unused. For example: Before deletion: [10] [20] [30] [40] [50] After deleting 10 and 20: [ ] [ ] [30] [40] [50] Although two positions are empty, REAR has reached the last position. Therefore, a linear queue may show Overflow when trying to insert another element. A circular queue solves this problem by allowing REAR to move back to the beginning and use the empty positions. Therefore, a circular queue provides better utilization of available memory.

Time Complexity Operation Time Complexity ENQUEUE O(1) DEQUEUE O(1) FRONT O(1) DISPLAY O(n)

Explanation

ENQUEUE: Inserts an element at REAR, so it takes O(1) time. DEQUEUE: Removes an element from FRONT, so it takes O(1) time. FRONT: Directly accesses the front element, so it takes O(1) time. DISPLAY: Visits all queue elements, so it takes O(n) time.

Space Complexity The circular queue is implemented using an array of fixed size. Therefore, the space complexity is O(n), where n is the size/capacity of the queue. For example, an array of size 5 can store a maximum of 5 elements.

Problem in Linear Queue When REAR Reaches Last Index When REAR reaches the last index of a linear queue, insertion may not be possible even if there are empty positions at the beginning. This problem is called False Overflow. For example:

[ ] [ ] [30] [40] [50] The first two positions are empty, but because REAR is already at the last position, a new element cannot normally be inserted without shifting elements. Circular Queue Solution

A circular queue allows REAR to wrap around and use those empty positions. Thus, it avoids unnecessary wastage of memory.
