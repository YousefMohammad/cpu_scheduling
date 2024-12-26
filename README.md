# CPU Scheduling Simulator

## Overview

The **CPU Scheduling Simulator** is a Python-based graphical user interface (GUI) application designed to simulate various CPU scheduling algorithms. It enables users to add processes with specific parameters and simulate the behavior of different scheduling algorithms to observe the results, including start time, completion time, turnaround time (TAT), and waiting time (WT).

## Features

- Add custom processes with:
  - Process ID
  - Arrival Time
  - Burst Time
  - Priority (optional)
- Simulate the following scheduling algorithms:
  - First Come First Serve (FCFS)
  - Non-Preemptive Shortest Job First (SJF)
  - Preemptive Shortest Job First (SJF)
  - Round Robin (RR) with user-defined quantum
  - Priority Scheduling
- View the results of each algorithm in a user-friendly text display.

## Installation

### Prerequisites

- Python 3.x
- Required libraries: `tkinter`, `ttk`

### Steps

1. Clone or download this repository.
2. Navigate to the directory containing the `cpu_scheduling_simulator.py` file.
3. Run the script using the command:
   ```bash
   python cpu_scheduling_simulator.py
   ```

## Usage

1. Launch the application.
2. Add processes:
   - Fill in the `Process ID`, `Arrival Time`, and `Burst Time` fields.
   - Optionally, provide a `Priority` (only needed for priority scheduling).
   - Click **Add Process** to save the process details.
3. Select an algorithm from the dropdown menu:
   - **FCFS**: First Come First Serve
   - **Non-Preemptive SJF**: Non-Preemptive Shortest Job First
   - **Preemptive SJF**: Preemptive Shortest Job First
   - **Round Robin**: Requires the `Quantum` field to be filled
   - **Priority Scheduling**: Requires process priorities
4. Click **Simulate** to run the selected algorithm and view the results.

## Algorithms

### 1. **First Come First Serve (FCFS)**
Processes are executed in the order of their arrival time.

### 2. **Non-Preemptive Shortest Job First (SJF)**
The process with the shortest burst time is selected for execution once it arrives.

### 3. **Preemptive Shortest Job First (SJF)**
Processes are scheduled dynamically based on the shortest remaining burst time.

### 4. **Round Robin (RR)**
Processes are executed in a cyclic manner with a user-defined quantum.

### 5. **Priority Scheduling**
Processes are scheduled based on their priority, with lower values indicating higher priority.

## GUI Overview

- **Input Fields**: Fields to add process details.
- **Algorithm Selection**: Dropdown menu to select a scheduling algorithm.
- **Quantum Input**: Field for specifying the quantum for Round Robin scheduling.
- **Results Display**: A text area to display the scheduling results.

## Example Output

After simulating a scheduling algorithm, results are displayed in the following format:

```
P1: Start: 0, Completion: 4, TAT: 4, WT: 0
P2: Start: 4, Completion: 9, TAT: 7, WT: 2
P3: Start: 9, Completion: 15, TAT: 10, WT: 3
```

- **Start**: Time when the process started execution.
- **Completion**: Time when the process completed execution.
- **TAT**: Turnaround Time (Completion Time - Arrival Time).
- **WT**: Waiting Time (TAT - Burst Time).

## Contributing

If you'd like to contribute, feel free to fork the repository and submit a pull request with improvements or additional features.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments

This project utilizes:
- `tkinter` for GUI development.
- Python's data structures and algorithms for scheduling logic.
