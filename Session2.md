# Session 2

## Presentation Tips
- While preparing, only fully understanding algorithm can let you know how to code.
- After algorithm is well expained, coding along presenting can be practiced.

## Stack & Queue

### Stack? What is it?

1. Imagine anything you may say "a stack of ...". \
Congrats, you have a stack.
2. Basic operations: push(), pop(), peek()/top(), isEmpty()... run in O(1); independent from number of elements in the stack.
3. Fist in, Last out.

### Queue? What is it?

1. Imagine when you loyally wait in a queue and never jump around/quit.\
Congrats, you have a queue.
2. Basic operations: enqueue(), dequeue(), isEmpty()... run in O(1); independent from number of elements in the queue.
3. Fist in, Fist out. (Thank god)

### Implement Stack by Queue (Warm up)

**Algorithm in text will be updated after the session.**

-By one queue:
```java
/** Have our queue ready. */

queue = new Queue;

/** Push element x onto stack. */
push(x) {
    n = queue.size();
    queue.enqueue(x);
    for (int i = 0; i < n; i++) {
        queue.enqueue(queue.dequeue());
    }
}

/** Removes the element on top of the stack and returns that element. */
pop() {
    return queue.dequeue();
}

/** Get the top element. */
top() {
    return queue.peek();
}

/** Returns whether the stack is empty. */
boolean empty() {
    return queue.isEmpty();
}

```

-By two queues:

```java
/*first have two queues ready*/
queue1 = new Queue;
queue2 = new Queue;

/** Push element x onto stack. */
push(int x) {
    queue2.enqueue(x);
    while (!queue1.isEmpty()) {
        queue2.enqueue(queue1.dequeue());
    }
    Queue temp = queue1;
    queue1 = queue2;
    queue2 = temp;
}

/** Removes the element on top of the stack and returns that element. */
pop() {
    return queue1.dequeue();
}

/** Get the top element. */
top() {
    return queue1.top();
}

/** Returns whether the stack is empty. */
boolean empty() {
    return queue1.isEmpty();
}

```

### Implement Queue by Stack (Q19)
**Solution can't be shared by us, sorry**

*Hint: use one for input, and the other for output*

### Properties of data structure in application (Q20)
**Solution can't be shared by us, sorry**

*Hint: think how can queue and/or stack track the search*

### Any Question you may have in this part (Q&A)

## Linked List
### Linked List? Linked?

1. A points to B, B points to C -- singly linked list;\
A points to B and vice versa, B points to C vice versa -- doubly linked list
2. Remember you only get the data through pointer: well, it'd better have some one that refers to itself, and luckly it does.
3. **Strong** object property. (Sea of pointers)

### Properties of Linked List (Object) (Q14)

**Solution can't be shared by us, sorry**

*Hint: use pointers/references to keep track the object!! use a lot (but of course essential ones)*