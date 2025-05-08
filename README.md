[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/gW4p9-Fp)

# Scheduler Design Summary

## 1️⃣ First-Come, First-Serve (FCFS) Scheduler:
**Concept:**  
Threads are executed in the order they arrive (**FIFO**).

**Implementation:**  
- Uses a single **run queue** where threads are added to the **end**.
- Threads run until they **block, finish, or explicitly yield**.
- No **time slicing**; no preemption during execution.

---

## 2️⃣ Multi-Level Feedback Queue (MLFQ) Scheduler:
**Concept:**  
Uses multiple **priority queues** to manage threads.

**Implementation:**  
- Threads start in the **highest priority queue** and move down if they consume CPU time.
- On a **timer interrupt**, a running thread is **demoted** to a lower priority.
- Threads are always picked from the **highest non-empty queue**.
- **Optional:** Threads that wait too long can be **promoted** back up to prevent starvation.
