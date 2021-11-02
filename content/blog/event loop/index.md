---
title: Asynchronous JavaScript with Node.js
date: "2021-10-29T22:12:03.284Z"
description: "event loop"
---


#### Asynchronous JavaScript with Node.js
> In server-side development, we often perform time-consuming tasks such as reading files or querying a database. Instead of halting the execution of our code to await these operations or using multiple threads like other back-end environments, Node was designed to use an event loop like the one used in browser-based JavaScript execution. The event-loop enables asynchronous actions to be handled in a non-blocking way.
>Node provides a number of APIs for performing asynchronous tasks which expect callback functions to be passed in as arguments. Under the hood, these APIs trigger the subscription to and emitting of events to signal the completion of the operation. When the operation completes, the callback function is added to a queue, or line, of tasks waiting for their turn to be executed. When the current stack, or list, or synchronous tasks finish executing, the operations on the queue will be performed.
>This means if synchronous tasks never end, operations waiting in the event-queue would never have the chance to run. Take a look at the following example code using the asynchronous Node setTimeout () API which asynchronously executes a provided callback function after a given delay:



#### Timers  


> In Node.js timers, or functions that execute callbacks after a set period of time, are provided by the core timers module. 
This module provides two global functions: setTimeout(), and setInterval(). These allow you to define code to execute after a period of time.

>Both functions take a callback function, and delay in milliseconds, as their arguments. 
Additional arguments can optionally be passed after the delay -- those arguments will be passed to the callback function.

>The timers phase is executed directly by the Event Loop. At the beginning of this phase the Event Loop updates its own time. 
>Then it checks a queue, or pool, of timers. This queue consists of all timers that are currently set.
 The Event Loop takes the timer with the shortest wait time and compares it with the Event Loop's current time. 
If the wait time has elapsed, then the timer's callback is queued to be called once the call stack is empty.

>Node.js has different types of timers: setTimeout() and setInterval(). 
The fundamental difference between them is that setInterval() has a repeat flag which places the timer back into the queue once its execution is finished. 
This is a how a process, like a server, can stay "alive" waiting for a request indefinitely.

>The nature of executing timer callbacks as part of the Event Loop explains the non-obvious feature that a timer's wait time is not an exact time 
in which the callback will be executed -- it is, in fact, a minimum time that will pass before the callback is queued for execution.

#### Event loop:->
>The event loop is the secret behind JavaScript’s asynchronous programming. JS executes all operations on a 
single thread, but using a few smart data structures, it gives us the illusion of multi-threading. Let’s take a look at what happens on the back-end.

>
>
>The call stack is responsible for keeping track of all the operations in line to be executed. 
Whenever a function is finished, it is popped from the stack.

>The event queue is responsible for sending new functions to the track for processing. It follows the 
queue data structure to maintain the correct sequence in which all operations should be sent for execution.
>
>
>Whenever an async function is called, it is sent to a browser API. These are APIs built into the browser. Based on the command received from the call stack, the API starts its own single-threaded operation.
>An example of this is the setTimeout method. When a setTimeout operation is processed in the stack, it is sent to the corresponding API which waits till the specified time to send this operation back in for processing.
>
>
>Where does it send the operation? The event queue. Hence, we have a cyclic system for running async operations in JavaScript. The language itself is single-threaded, but the browser APIs act as separate threads.
>
>The event loop facilitates this process; it constantly checks whether or not the call stack is empty. If it is empty, new functions are added from the event queue. If it is not, then the current function call is processed.



![Event loop](./1.png)

