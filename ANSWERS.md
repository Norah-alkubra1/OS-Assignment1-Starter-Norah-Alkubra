# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:A process is an independent program that has its own memory space and system resources, while a thread is a smaller unit of execution that runs within the same process and shares the same memory. Processes are generally heavier and take more time to create because they require separate memory allocation and system resources. In contrast, threads are lightweight and faster to create and manage.
In this assignment, threads were used instead of processes because they are more efficient for simulating CPU scheduling. All the processes in the simulation run within the same program, so using threads allows faster context switching and better performance. Threads also make it easier to simulate concurrent execution without the overhead of managing multiple separate processes.**

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:In Round-Robin scheduling, if a process does not finish within its assigned time quantum, it is placed back at the end of the ready queue. This allows other processes to get a chance to execute, which ensures fairness in CPU usage.

[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output:

⏸ P1 completed quantum 4000ms │ Overall progress: 44%
Remaining time: 4405ms
↻ P1 yields CPU for context switch

➕ P1 added to ready queue │ Burst time: 8405ms**


**Explanation of example:**
[Explain what's happening in the output snippet you pasted]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:         **New:
P1 is in the New state when the thread is created using new Thread(process) before calling start().
Runnable:
After calling start(), the thread becomes Runnable and is ready to be scheduled by the CPU.
Running:
The thread enters the Running state when the CPU starts executing the run() method, which is shown in the output when P1 begins executing its quantum.
  ▶ P1 executing quantum [4000ms] 
  ⚡ Quantum progress: [███████████████] 100%
Waiting:
The thread enters the Waiting state when Thread.sleep() is called to simulate execution time.
Terminated:
The thread becomes Terminated when the process finishes execution and its remaining time reaches zero.
[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [When is P1 in New state?]

2. **Runnable**: [When does P1 become Runnable?]

3. **Running**: [When is P1 Running?]

4. **Waiting**: [When/why would P1 be Waiting?]

5. **Terminated**: [When is P1 Terminated?]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**
Example 1: Web Server
Description:
A web server handles multiple client requests at the same time using threads.
Why Round-Robin works well here:
Round-Robin scheduling ensures that each request gets a fair share of CPU time. This prevents any single request from blocking others and improves overall responsiveness for users.
Example 2: Operating System Scheduler
Description:
Operating systems use schedulers to manage multiple running programs.
Why Round-Robin works well here:
It provides fair CPU distribution among processes, which is important in time-sharing systems. It also ensures that all applications remain responsive, even when multiple programs are running simultaneously.




## Summary

**Key concepts I understood through these questions:**
1_Thread lifecycle and execution
2_Round-Robin scheduling behavior
3_Context switching
Concepts I need to study more:
Advanced scheduling algorithms
Thread synchronization
