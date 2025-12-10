<p align="center">
<b>Pinwheel Scheduling with Penalties</b><br>
<b>MSc Dissertation Project – University of Liverpool</b><br>
<b>Supervisor: Prof. Leszek Gasieniec</b>
</p>



##  Overview
This project extends the classic **Pinwheel Scheduling** problem by introducing **penalties** for missed deadlines, transforming it from a binary feasibility question into a realistic **optimisation** problem.  

The objective is no longer “Is a perfect schedule possible?”, but:  
**What is the minimum-penalty schedule we can produce under real constraints?**  

This makes the system more aligned with practical scenarios, where resources are limited and occasional deadline violations are inevitable.



##  Core Problem Principles
The scheduling problem is defined by six key principles:

1. **Non-Preemption** : Once a task starts, it must finish.  
2. **Dynamic Deadlines** : Each task's next deadline = last execution time + frequency.  
3. **Penalty Costs** : Missing a deadline adds its penalty to the total cost.  
4. **Single-Slot Execution** : Only one task executes per time unit.  
5. **Density & Schedulability** : Schedulability is linked to total system density.  
6. **Conjecture** : Instances with density ≤ 5/6 are schedulable (verified for *n* ≤ 12).


##  Project Contributions  

### **1. Penalty-Based Reformulation**  
Transformed the classical feasibility problem into a **cost minimisation framework**, where each missed deadline incurs a penalty.  

### **2. Implementation**
The project includes a full suite of algorithms:

#### **Penalty-Aware EDF**
- Prioritises earliest deadlines  
- Breaks ties by **highest penalty**  

#### **Custom Greedy Algorithm**
- Balances **high-frequency** vs **high-penalty** tasks  
- Uses a custom priority score to prevent domination by one type of task  

#### **Optimal Dynamic Programming**
- Explores the full state space to compute the **optimal schedule**  
- Uses **state pruning** and **memoisation**  
- Serves as the **benchmark** for comparisons  
