### Event Loop
#### Stack
Function calls form a stack of frames.
#### Heap
Objects are allocated in a heap which is just a name to denote a large mostly unstructured region of memory.
#### Queue
- A JavaScript runtime uses a message queue, which is a list of messages to be processed. Each message has an associated function which gets called in order to handle the message.
- The processing of functions continues until the stack is once again empty; then the event loop will process the next message in the queue (if there is one).
- Each message is processed completely before any other message is processed.
#### Adding Microtasks
- `process.nextTick`/`Promise`/`MutationObserver`
- Microtasks are processed when the **current** macrotask ends and the microtask queue is cleared **before** the next macrotask cycle.
- Microtasks can enqueue other microtasks. All are executed before the next macrotask.
- UI rendering is run after all microtasks execution.
#### Adding Messages(Macrotasks)
- In web browsers, messages are added anytime an event occurs and there is an event listener attached to it.
- `setTimeout`/`setIntervel`/`setImmediate`

---
Reference:
[Concurrency model and Event Loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/EventLoop)