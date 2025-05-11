CPU-SchedSim (CPU Scheduling Simulator)
🔗 [GitHub](https://github.com/anooragsingh07/CPU-SchedSim--CPU-Scheduling-Simulator-))  

**Overview**  
CPU-SchedSim is a C++-based CPU scheduling simulator designed to model and analyze various short-term CPU scheduling algorithms used in operating systems. It provides a controlled environment to evaluate scheduling strategies, measure performance, and understand process execution behavior.  

**Supported Scheduling Algorithms**  
The simulator includes five major CPU scheduling algorithms, with a configurable context switch time of 14 milliseconds:  

1. First-Come, First-Served (FCFS) – Non-preemptive scheduling where the first arriving process gets executed first.  
2. Shortest-Job-First (SJF) (Non-Preemptive) – Executes processes with the shortest burst time first.  
3. Preemptive Shortest-Job-First (SJF) – Allows interruption when a shorter job arrives.  
4. Round-Robin (RR) – Time-slice-based scheduling with an adjustable time quantum (default: 200ms).  
5. Preemptive Priority Scheduling – Assigns random priority levels (0-4) to processes; lower values indicate higher priority. Higher-priority processes preempt lower-priority ones. If priorities match, Round-Robin scheduling is applied.  

**Process Generation & Arrival Times**  
- Each process is randomly assigned an arrival time and CPU burst time between 500ms and 4000ms.  
- Exponential Distribution is used to generate arrival times, making the simulation more realistic by ensuring that 80% of processes do not start at time 0.  
- The number of processes (`num_processes`) is adjustable (default: 20).  

**Customizable Parameters**  
- Context switch time: 14 milliseconds (fixed).  
- Time slice for Round-Robin and Priority Scheduling: Can be modified by updating `int timeslice` in the code.  

**Key Features**  
- Simulates multi-algorithm CPU scheduling in a controlled environment.  
- Allows detailed analysis of process execution order and turnaround times.  
- Supports modifications for different scheduling policies and configurations.  
- Implements realistic workload patterns using Exponential Distribution.  
- Provides insights into process preemption, waiting times, and response times.  

**Note:**  
No actual processes are forked. This is a pure simulation of CPU scheduling in an OS.  

**Installation**  
1. Clone the repository:  
   `git clone https://github.com/anooragsingh07/process_simulator.git`  
2. Navigate to the project directory:  
   `cd process_simulator`  
3. Compile the program using g++:  
   `g++ -o process_simulator process_simulator.cpp`  
4. Run the simulator:  
   `./process_simulator`  

**Usage**  
- The number of processes (`num_processes`) is default: 20, but can be modified in the code.  
- The time slice for Round-Robin and Priority Scheduling can be adjusted:  
  `int timeslice = 200; // Change this value as needed`  

**Future Improvements**  
- Add Gantt chart visualization for scheduling algorithms.  
- Implement custom process input support.  
- Improve statistical analysis of scheduling efficiency.  

**Author**  
Anoorag Singh  
📧 anooragsingh0007@gmail.com  
🔗 [GitHub](https://github.com/anooragsingh07)  
