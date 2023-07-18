## Linked list Cheat sheet 

Node: The basic unit of a linked list. Each node has a value and a reference to the next node.

Head: The first node in the list.

Tail: The last node in the list, which points to null as the next node.

Singly Linked List: A linked list where each node has a reference to the next node. It can only be traversed in one direction.

Doubly Linked List: A linked list where each node has a reference to both the next node and the previous node. It can be traversed in both directions.

Traversal: The process of going through or traversing the linked list from the head to the tail.

Insertion: The process of adding a new node to the list. It can be done at the beginning (updating the head), at the end (updating the tail), or at a specific position (updating the next reference of the previous node and the previous reference of the next node in case of doubly linked list).

Deletion: The process of removing a node from the list. Similar to insertion, it requires updating the references of the neighboring nodes.

Search: Checking if a certain value exists in the list. This requires traversal of the list until the node is found or the end of the list is reached.

Time Complexity: The efficiency of operations in a linked list. Searching or accessing an element is typically O(n) because in the worst case, you may have to traverse all the nodes. Insertion and deletion at a known position is O(1), but finding the position is O(n).

Space Complexity: The amount of memory used by the linked list. Each node requires space for the stored value and the reference(s). Thus, the space complexity is proportional to the length of the list, or O(n).

## Big O Notation analogy


Consider the task of finding a specific word in a book:

O(1) – Constant Time: This is like knowing the exact page, paragraph, and line where the word is found in the book. No matter how big the book is, you can flip directly to the information.

O(n) – Linear Time: This is like searching for the word by reading the book from start to end. In the worst-case scenario, the word could be on the last page or not there at all. The time it takes grows linearly with the size of the book - the bigger the book, the longer it might take.

O(n²) – Quadratic Time: Imagine you are looking for two words, but after finding the first word, you go back to the start of the book to find the second word. For each word, you look at every page in the book. This would take significantly more time and is less efficient.

O(log n) – Logarithmic Time: This is like finding a word in a dictionary. You wouldn't read the dictionary from start to end. Instead, you'd open it halfway, and if the word you're looking for is alphabetically less than the page you're on, you'd repeat the process with the first half of the book, otherwise, you'd do it with the second half. You'd continue halving the search space until you find the word. Even for a large dictionary, you'd find the word in a relatively short amount of time.

O(n log n) – Linear Logarithmic Time: This is like sorting the pages of a book. For each page, you need to find its place, which is a logarithmic operation - but you have to do this for all pages (n times). Algorithms like quicksort and mergesort fall into this category.