# Priority-Scheduled File Compression Daemon

## Video Demo
[![Click to watch the video](https://youtube.com)](https://www.youtube.com/watch?v=E5eqq-vW-Gs)

## Short Introduction
Welcome to the **Compression Daemon**! This project is a robust, high-performance background service that hooks into OS-level interrupts to automatically monitor directories and compress files on the fly. By transitioning from a naive FIFO queue to a 12-core thread pool powered by an **SRPT (Shortest Remaining Processing Time)** scheduler, it effectively solves real-world challenges like Head-of-Line blocking and memory bloat.

## Skills Highlight
Building this daemon required a deep dive into low-level systems programming. Here is what this project demonstrates about my technical skillset:

* **Advanced Multithreading & Concurrency:** Engineered a 12-core thread pool and implemented custom synchronization Monitors from scratch to eliminate race conditions.
* **Modern C++17:** Wrote clean, optimized, and modern C++ code to manage complex state and resource lifetimes.
* **Algorithmic Problem-Solving:** Designed and deployed a Min-Heap priority queue to bring the theoretical SRPT CPU scheduling algorithm into application-level file I/O.
* **Direct OS API Interaction:** Interfaced directly with OS-level APIs (POSIX, `mmap` for zero-copy memory mapping, and thread affinity) to squeeze out every drop of hardware performance and maintain a minimal memory footprint.
