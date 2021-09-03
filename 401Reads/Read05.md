# Read 05

## Linked List

- What is a Linked List? <br />
    A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link.<br />

    Terminology:
    1. Linked List - A data structure that contains nodes that links/points to the next node in the list. <br />
    2. Singly - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list. <br />
    3. Doubly - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.<br />
    4. Node - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link. <br />
    5. Next - Each node contains a property called Next. This property contains the reference to the next node.<br />
    6. Head - The Head is a reference of type Node to the first node in a linked list. <br />
    7. Current - The Current is a reference of type Node to the node that is currently being looked at. When traversing, you create a new Current variable at the Head to guarantee you are starting from the beginning of the linked list. <br />

    <img src="https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/images/LinkedList1.PNG"
     alt="code-challenge-2 whiteBoard"
     style="float: left; margin-right: 10px;" />

    - Traversal
        When traversing a linked list, you are not able to use a foreach or for loop. We depend on the Next value in each node to guide us where the next reference is pointing. The Next property is exceptionally important because it will lead us where the next node is and allow us to extract the data appropriately. <br />

        When traversing through a linked list, the Current variable will tell us where exactly in the linked list we are and will allow us to move/traverse forward until we hit the end.<br />

    - Adding a Node

        <img src="https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/images/LinkedList2.PNG"
     alt="code-challenge-2 whiteBoard"
     style="float: left; margin-right: 10px;" />

    Regardless of the number of Nodes that this linked list has, it will always be a O(1) time and space because it takes the same amount of time to add a new node to the beginning of the list, and no additional resources are being used. <br />

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)