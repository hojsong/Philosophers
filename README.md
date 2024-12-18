# Philosophers

[한국어 버전](README.md.kr)

## Overview
Philosophers is a concurrency project that simulates the classic "Dining Philosophers Problem". This project helps in understanding threads, mutexes, and synchronization in C.

- **Objective:** Simulate a group of philosophers who alternate between eating, thinking, and sleeping, while avoiding deadlocks and data races.
- **Key Features:**
  - Thread-based simulation.
  - Safe synchronization using mutexes.
  - Deadlock prevention.

## Problem Description
- **The Dining Philosophers Problem:**
  - A group of philosophers sits at a round table.
  - Each philosopher alternates between thinking, eating, and sleeping.
  - To eat, a philosopher needs two forks (shared resources).
  - The challenge is to avoid deadlocks and ensure all philosophers eat without conflicts.

## Features
- **Thread Management:**
  - Each philosopher is a separate thread.
  - Threads run concurrently and share resources.
- **Synchronization:**
  - Use of mutexes to avoid race conditions and ensure safe resource sharing.
- **State Management:**
  - Philosophers' actions (thinking, eating, sleeping) are logged with timestamps.

## Requirements
- **Operating System:** Linux or macOS.
- **Dependencies:** None (standard C library and POSIX threads).

## Installation and Execution
### Clone the Repository
```bash
git clone [repository URL]
cd philosophers
```

### Build
```bash
make
```

### Run
```bash
./philo [number_of_philosophers] [time_to_die] [time_to_eat] [time_to_sleep] [number_of_meals (optional)]
```

### Example
```bash
./philo 5 800 200 200
```
- 5: Number of philosophers.
- 800: Time (in ms) a philosopher can live without eating.
- 200: Time (in ms) it takes to eat.
- 200: Time (in ms) it takes to sleep.


### File Structure
- `philo/`: multi-thread project.
- `philo_bonus/`: multi-process project.
- `*/srcs/`: Source code files.
- `*/includes/`: Header files.
- `*/Makefile`: Build script.

### How It Works
- Each philosopher thread alternates between thinking, eating, and sleeping.
- Forks (resources) are represented by mutexes.
- A philosopher can eat only if they acquire two forks.
- The program prevents deadlocks using resource allocation strategies.

### References
- Dining Philosophers Problem
- POSIX Threads