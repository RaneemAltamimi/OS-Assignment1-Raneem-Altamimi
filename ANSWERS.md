# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:A process is a stand-alone program that is running and has its own memory and system resources. Every process functions independently and necessitates the creation and management of additional overhead.

A thread, on the other hand, shares memory and resources with other threads and is a smaller unit of operation within the same process. As a result, creating and switching between threads is quicker and lighter.

Because the simulation necessitates frequent context switching and shared access to the ready queue, threads were utilized in this assignment rather than processes. Because they lower overhead and enable quicker task-to-task communication, threads are more effective for this use.**

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:In Round-Robin scheduling, if a process does not complete within its assigned time quantum, it is paused and moved to the end of the ready queue. This ensures all processes get a fair chance to execute.**

[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output:
P1 executing quantum [4000ms]
Remaining time: 656ms
P1 yields CPU for context switch
P1 added to ready queue │ Burst time: 4656ms


**Explanation of example:In this instance, process P1 had 656 ms left after failing to complete its first time quantum (4000 ms). As can be seen in the output, where P1 appears at the end of the queue after P13, it yields the CPU and is put back into the ready queue. It is scheduled for its remaining 656 ms later. This clearly illustrates the program's Round-Robin behavior.**
[Explain what's happening in the output snippet you pasted]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]
1. New:
P1 is in the New state when it is first created using the Process constructor before the thread is started.

2. Runnable:
After calling start(), P1 moves to the Runnable state and waits in the ready queue to be scheduled by the CPU.

3. Running:
P1 enters the Running state when it is selected from the queue and begins executing the run() method.

4. Waiting:
P1 enters the Waiting state when Thread.sleep() is called during execution, which simulates processing time and temporarily pauses the thread.

5. Terminated:
P1 reaches the Terminated state when its remaining time becomes zero, meaning it has finished execution and will not be scheduled again.


---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Web Server Handling Requests]

**Description**: 
Multiple client requests are handled concurrently by a web server, and each request may be handled as a different thread.

**Why Round-Robin works well here**: 
By allocating a defined time slice to each request, Round-Robin assures fairness. This enhances responsiveness and keeps additional requests from being blocked by a single request.

### Example 2: [Operating System Task Scheduling]

**Description**: 
[Operating systems use threads to manage several background activities and applications.]

**Why Round-Robin works well here**: 
It guarantees that every job advances and avoids hunger by allowing each task to run for a set amount of time.
---

## Summary

**Key concepts I understood through these questions:**
1. The distinction between processes and threads
2. How Round-Robin scheduling guarantees equity
3. A thread's life cycle and states

**Concepts I need to study more:**
1. Thread synchronization and race conditions
2. Sophisticated algorithms for scheduling 
