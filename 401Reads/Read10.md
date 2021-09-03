# Read 10

## Stacks and Queues

- What is a Stack? <br />
    A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.<br />

    Common terminology for a stack is

    1. Push - Nodes or items that are put into the stack are pushed. <br />
    2. Pop - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.<br />
    3. Top - This is the top of the stack.<br />
    4. Peek - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.<br />
    5. IsEmpty - returns true when stack is empty otherwise returns false.<br />

- Stack Visualization
    Here’s an example of what a stack looks like. As you can see, the topmost item is denoted as the top. When you push something to the stack, it becomes the new top. When you pop something from the stack, you pop the current top and set the next top as top.next. <br />

    <img src="https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/stack1.PNG"
     alt="code-challenge-2 whiteBoard"
     style="float: left; margin-right: 10px;" />

- What is a Queue? <br />
    Common terminology for a queue is

    1. Enqueue - Nodes or items that are added to the queue. <br />
    2. Dequeue - Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.<br />
    3. Front - This is the front/first Node of the queue.<br />
    4. Rear - This is the rear/last Node of the queue.<br />
    5. Peek - When you peek you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raised.<br />
    6. IsEmpty - returns true when queue is empty otherwise returns false.<br />

    - Queue Visualization <br />

      <img src="https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Queue.PNG"
     alt="code-challenge-2 whiteBoard"
     style="float: left; margin-right: 10px;" />

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)
