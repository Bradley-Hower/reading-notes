# *Course 401 Python, Entry 5: Linked List*

A **Linked List** is a series of linnearly connected nodes.

There are **Singly** linked lists and **Doubly** linked lists. Singly is a one-way pointer, pointing to the next node. Doubly is a two-way pointer, next and previous nodes. There is also **circular** linked lists, which can be singly or doubly.

**Head** is a special reference node which points to the first node in a linked list.

**Current** is a reference node which notes the node currently being looked at.

![Linked Lists](assets/LinkedList1.png)

## Traversal

To traverse a linked list, a while loop is use, checking if the current node is the node we are searching for. The loop will continue until reach a null reference.

## Big O

Linked List Big O:

**Time** - O(n)

**Space** - O(1)

## Node Add

## Add

Adding at the beginning of a linked list is as simple as taking a new node, listing its next as the node that is the name of the current node and head node (same one). The new head and current node is now the new node. This is a simple process and can not be simplified past O(1).

## AddBefore and AddAfter

The `AddBefore` and `AddAfter` methods are the same process, expect when the next node is labeled. In `AddBefore`, the next node for the new node is named before the node precede it is attached. In `AddAfter`, the next node is named after the preceding node has its next node changed to this new node. The Big O is O(n) for time for this process, while space stays the same at O(1).

## Arrays vs Linked Lists

Arrays - the **Good**:

+ Searsh is fast.
+ Binary search is an option due to contiguous memory.

Arrays - the **Bad**:

+ Inserting and deleting can be slow.
+ Static in size. Not easy to shrink and grow.
+ Memory is allocated when created. This big chunk could be a waste of resources, or too small.

Linked Lists - the **Good**:

+ Inserting and deleting can be fast.
+ Dynamic in size, can shrink and grow easily.
+ Only allocated resources as needed, in non-contigiuous chunks.

Linked Lists - the **Bad**:

+ Search is slow.
+ Can not use binary search.

Summary:

Arrays are good if you know the size of the list, accessng is random or want to iterate the fastest.

Linked lists are good if you don't know the size needed, and want to remove things quickly without random access.

