# Scope

- [Algorithms](#algorithms)


# Algorithms

- **Circular Lists**: A circular list can be singly-linked or doubly-linked, but its distinguishing feature is that it has no tail. In a circular list, the next pointer of the last element points back to its first element rather than NULL. In the case of doubly-linked lists, the prev pointer points to the last element as well. \
\
In practice, whether to make use of a singly-linked list circular list or one that is doubly-linked depends on the same reasoning presented earlier for choosing between singly-linked and doubly-linked lists that are not circular.

- **Side-Notes**: Interesting questions: \
\
_Some advantages of linked lists over arrays have already been mentioned. However, there are occasions when arrays have advantages over linked lists. When are arrays preferable?_ \
\
Linked lists present advantages over arrays when we expect to insert and remove elements frequently. However, arrays themselves offer some advantages when we expect the number of random accesses to overshadow the number of insertions and deletions. Arrays are strong in this case because their elements are arranged contiguously in memory. This contiguous arrangement allows any element to be accessed in O(1) time by using its index. Recall that to access an element of a linked list, we must have a pointer to the element itself. Getting a pointer to an element can be expensive if we do not know a great deal about the pattern in which the elements will be accessed. In practice, for many applications, we end up traversing at least part of the list. Arrays are also advantageous when storage is at a a premium because they do not require additional pointers to keep their elements "linked" together. \
\
_Why is no operation provided for singly-linked lists to remove the specified element itself, analogous to the dlist_remove operation for doubly- linked lists? (One can ask the same for the circular list implementation)._ \
\
In the singly-linked list and circular list implementations, each element does not have a pointer to the one preceding it. Therefore, we cannot set the preceding element’s next pointer to the element after the one being removed.
