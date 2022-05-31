# Scope

- [Algorithms](#algorithms)



# Algorithms

- **Linked Lists**: The implementation uses a structure called List, where it is filled with list_init() according to the parameters passed. To insert a new element, make the element preceding the new element point to the new element (which is pointing to the next element). To insert at the head of the list, make the new element point to the actual element at the head of the list, then update the Head pointer in the List structure. The opposite is valid for removing elements from the list. \
\
A linked list is a good way to manage frames because frame allocation involves frequent insertions and deletions, simply calling list_ins_next and list_rem_next, which are both O(1) operations. 
