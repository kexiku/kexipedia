![[Node.js-Architecture-Chart.jpg]]

As stated in the [specification](https://tc39.github.io/ecma262/#sec-jobs-and-job-queues):

- The queue is first-in-first-out (FIFO): tasks enqueued first are run first.
- Execution of a task is initiated only when nothing else is running.

When the JavaScript engine becomes free from the current code, it takes a task from the queue and executes it.

Promise handlers _always_ go through this internal queue.

The general algorithm:

1. Dequeue and run the oldest task from the _macrotask_ queue.
2. Execute all _microtasks:_
    - While the microtask queue is not empty:
        - Dequeue and run the oldest microtask.
3. Render changes if any.
4. If the macrotask queue is empty, wait till a macrotask appears.
5. Go to step 1.

![[Screenshot 2024-10-20 194125.png]]

Two more details:

1. Rendering never happens while the engine executes a task. It doesn’t matter if the task takes a long time. Changes to the DOM are painted only after the task is complete.
2. If a task takes too long, the browser can’t do other tasks, such as processing user events. So after some time, it raises an alert like “Page Unresponsive”, suggesting killing the task with the whole page.

## 🐘 Macrotasks

To schedule a new macrotask:

- Use zero delayed `setTimeout(f)`.

That may be used to split a big calculation-heavy task into pieces, for the browser to be able to react to user events and show progress between them

![[Screenshot 2024-10-20 190325.png]]

## 🐛 Microtasks

Microtasks are usually created by promises.

They are used “under the cover” of `await` as well, as it’s another form of promise handling.

> **Immediately after every _macrotask_, the engine executes all tasks from _microtask_ queue, prior to running any other macrotasks or rendering or anything else.**

To schedule a new _microtask_

- Use `queueMicrotask(f)`
    
    OR
    
- Use promise handlers






[^1]: Sources:
	[https://www.educative.io/answers/what-is-the-event-driven-non-blocking-i-o-model-in-node-js](https://www.educative.io/answers/what-is-the-event-driven-non-blocking-i-o-model-in-node-js)
	[https://javascript.info/microtask-queue](https://javascript.info/microtask-queue)
	[https://javascript.info/event-loop](https://javascript.info/event-loop)
	[https://www.builder.io/blog/visual-guide-to-nodejs-event-loop](https://www.builder.io/blog/visual-guide-to-nodejs-event-loop)
	[https://litslink.com/blog/node-js-architecture-from-a-to-z](https://litslink.com/blog/node-js-architecture-from-a-to-z)
