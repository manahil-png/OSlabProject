
markdown
# Process Scheduling Algorithms
This project implements various CPU scheduling algorithms in C++ to manage process execution. The implemented algorithms are:
1. First Come First Serve (FCFS)
2. Shortest Job First (SJF)
3. Round Robin (RR)
4. Priority Scheduling (Preemptive)
5. Non-preemptive Priority Scheduling

## How to Run
1. **Clone the repository**:
    sh
    git clone <repository-link>
    cd <repository-directory>
    
2. **Compile the code**:
    sh
    g++ scheduling_algorithms.cpp -o scheduling_algorithms
    
3. **Run the executable**:
    sh
    ./scheduling_algorithms
    
4. **Follow the prompts**:
    - Enter the number of processes.
    - Enter the arrival time and burst time for each process.
    - Choose the desired scheduling algorithm.
    - For Priority Scheduling, also enter the priority for each process.
    - For Round Robin, enter the time quantum.

## Code Explanation

The code consists of the following main sections:

1. **Struct Definition**:
    cpp
    struct process {
        int pid;
        int arrival_time;
        int burst_time;
        int start_time;
        int completion_time;
        int turnaround_time;
        int waiting_time;
        int response_time;
        int priority;
    };
    
    This structure stores information about each process.

2. **Function Prototypes**:
    cpp
    void firstComeFirstServe(process p[], int n);
    void shortestJobFirst(process p[], int n);
    void roundRobin(process p[], int n, int tq);
    void priorityScheduling(process p[], int n);
    void nonpre_pri(process p[], int n);
    

3. **Comparison Functions**:
    Functions to compare processes based on various criteria like arrival time, process ID, priority, and burst time.

4. **Main Function**:
    The main function initializes processes, takes user input for process details, and invokes the selected scheduling algorithm.

5. **Scheduling Algorithm Implementations**:

    - **First Come First Serve (FCFS)**:
        cpp
        void firstComeFirstServe(process p[], int n) {
            // Implementation details
        }
        
        - Sorts processes by arrival time.
        - Computes start, completion, turnaround, waiting, and response times for each process.
        - Calculates and prints average turnaround time, waiting time, response time, CPU utilization, and throughput.

    - **Shortest Job First (SJF)**:
        cpp
        void shortestJobFirst(process p[], int n) {
            // Implementation details
        }
        
        - Sorts processes by arrival time and burst time.
        - Uses a while loop to select the shortest job available at the current time.
        - Computes and prints various metrics as in FCFS.

    - **Round Robin (RR)**:
        cpp
        void roundRobin(process p[], int n, int tq) {
            // Implementation details
        }
        
        - Uses a queue to manage processes based on the given time quantum.
        - Adjusts burst times and computes metrics.

    - **Priority Scheduling (Preemptive)**:
        cpp
        void priorityScheduling(process p[], int n) {
            // Implementation details
        }
        
        - Sorts processes by priority.
        - Manages process execution based on the highest priority available.
        - Computes and prints metrics.

    - **Non-preemptive Priority Scheduling**:
        cpp
        void nonpre_pri(process p[], int n) {
            // Implementation details
        }
        
        - Similar to priority scheduling but without preemption.
        - Sorts processes by priority and executes them to completion before moving to the next.
        - Computes and prints metrics.

## Output
The program prints a table with process details such as arrival time, burst time, start time, completion time, turnaround time, waiting time, and response time. It also displays average turnaround time, average waiting time, average response time, CPU utilization, and throughput for the selected scheduling algorithm.

## Example
After running the program, the output may look like:

#P   AT   BT   ST   CT   TAT   WT   RT
1    0    5    0    5    5     0    0
2    1    3    5    8    7     4    5
3    2    8    8    16   14    6    8

Average Turnaround Time = 8.67
Average Waiting Time = 3.33
Average Response Time = 4.33
CPU Utilization = 93.75%
Throughput = 0.27 process/unit time


5. Share your repository link: Once uploaded, share the repository link in Google Classroom.
