# Scope

- [Algorithms](#algorithms)


# Algorithms

- **Description of Stacks**: The stack retrieves and stores data in a LIFO (Last-in, first-out) manner, that is, the last element placed on the stack is the first to be removed.

- **Traversing stacks**: Suppose we want to traverse the elements of a stack, perhaps so we can display them or determine whether a specific element resides in the stack. We can implement linked lists to simplify this process. To do this, we get the element at the head of the list using list_head and traverse the list using list_next. \
\
Using only stack operations, we would have to pop the elements one at a time, inspect them, and push them onto another stack temporarily. Then, after accessing all of the elements, we would need to rebuild the original stack by popping the elements off the temporary stack and pushing them back onto the original one.

- **Description of Queues**: A queue stores and retrieves data in a FIFO (first-in, first-out) manner, that is, the first element placed in the queue is the first to be removed. \
\
In computing, to place an element at the tail of a queue, we enqueue it, to remove an element from the head, we dequeue it. Sometimes it is useful to inspect the element at the head of a queue without actually removing it, in which case we peek it. \
\
![day29-algorithms-1](day29-algorithms-1.png)
