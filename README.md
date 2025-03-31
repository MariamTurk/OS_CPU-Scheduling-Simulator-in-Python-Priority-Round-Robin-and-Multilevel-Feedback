# CPU Scheduling Simulator in Python

This project implements and visualizes three core CPU scheduling algorithms:
1. **Non-Preemptive Priority Scheduling with Round Robin**
2. **Preemptive Priority Scheduling with Aging**
3. **Multilevel Feedback Queue Scheduling**

The simulation uses Python and Matplotlib to visualize process execution with Gantt charts and calculate performance metrics such as **Average Waiting Time (AWT)** and **Average Turnaround Time (ATAT)**.

---



## 🧠 Features

- Simulates three major CPU scheduling algorithms
- Uses realistic input with arrival time, burst time, priority, and comeback time
- Calculates:
  - Average Waiting Time
  - Average Turnaround Time
- Visualizes scheduling with Gantt charts using Matplotlib
- Well-commented and structured for learning and extension

---

## 🔧 Algorithms Implemented

### 1. Non-Preemptive Priority + Round Robin
- Uses priority to sort ready queue
- Processes execute in time slices (`q=2`)
- After each slice, processes wait for a defined **comeback time** before re-entering the ready queue

### 2. Preemptive Priority + Aging
- Higher-priority process preempts current process
- Aging mechanism reduces priority number (increases priority) every 5 time units to prevent starvation

### 3. Multilevel Feedback Queue
- Three-level queues with increasing time quantum (8, 16, 32)
- Processes drop to lower-priority queue if not completed
- Encourages fair CPU usage and responsiveness

---

## 📊 Example Input

```python
processes = [
    Process("P1", 0, 15, 3, 5),
    Process("P2", 1, 23, 2, 14),
    Process("P3", 3, 14, 3, 6),
    Process("P4", 4, 16, 1, 15),
    Process("P5", 6, 10, 0, 13),
    Process("P6", 7, 22, 1, 4),
    Process("P7", 8, 28, 2, 10),
]

---

## 📈 Output
For each algorithm:

Gantt chart visualizing process execution over time

Printed metrics:

Average Waiting Time: XX.XX
Average Turnaround Time: XX.XX
