---
tags:
  - Notes
links: "[[OD Lecture 8]]"
creation date: 2024-11-22 15:31
modification date: Friday 22nd November 2024 15:31:14
semester: 3
year: 2024
---


---
# [[OD Lecture 8 Notes]]

---

## Memory Management

### Introduction to Memory Management in Operating Systems

The memory management subsystem plays a crucial role in the operating system as it enables the effective use of system memory which often exceeds physical memory limits. The key innovation in memory management is virtual memory, which creates an illusion of a larger memory space by sharing memory among processes. This not only increases the usability of physical memory but also encompasses several critical features like large address spaces, process protection, and efficient memory allocation strategies. Virtual memory is fundamental not just for memory efficiency but also for enhancing system security by isolating processes from one another.

### Key Features and Concepts of Memory Management

Virtual memory provides various essential functionalities: 1. **Large Address Spaces**: Operating systems can present a larger memory environment to applications than physically present in the system. 2. **Protection**: Each process operates within its own virtual address space, ensuring that the memory and processes do not interfere with one another. For example, memory protection allows the system to prevent rogue applications from modifying memory spaces that belong to different processes.

### Understanding Virtual Memory: An Abstract Model  


Virtual memory operates through the conversion of virtual addresses to physical addresses. The abstraction model breaks memory into standardized units known as pages. Each virtual address comprises a virtual page number and an offset, which together guide the processor to the correct physical memory through page tables.

  

### Demand Paging and Page Faults  

Demand paging is a strategic approach where the system loads pages into memory only when required by a running process. If a process accesses a virtual address not currently in memory, a page fault occurs, prompting the operating system to fetch the necessary page from disk. The operating system distinguishes between valid address accesses and invalid addresses, managing each accordingly.

  

### Swapping and Memory Strategies 

When physical memory is exhausted, the system employs a swapping mechanism where less-used pages are swapped out to make space for more critical pages. It's essential for the operating system to maintain efficiency during this process by avoiding excessive swapping, commonly referred to as thrashing.

  

### Access Control and Security 

The page tables not only track physical address mappings but also impose access controls to ensure that processes operate securely within their allocated memory regions. Access control rules ascertain what kind of operations (read, write, execute) can be performed on specific memory pages.

  

### Memory Caches and Efficiency  

To enhance performance, Linux maintains various caches including: - **Buffer Cache**: Used for block devices, it accelerates read/write operations by buffering data. - **Page Cache**: Facilitates faster access to file data. - **Swap Cache**: Prevents unnecessary writes to swap files for pages that have not changed.

  

### Page Tables and Memory Management Structures  

Linux operates with a multi-level page table structure (usually three levels), allowing efficient navigation through virtual to physical address mapping. These tables facilitate not only the address translation but also maintain the age and count of physical pages to manage allocation and deallocation effectively.

  
### Memory Mapping and Executables  

When programs or libraries are run, they are memory-mapped into the virtual address space, allowing portions to be loaded on demand. The operations associated with these memory mappings are crucial in managing the overall efficiency of process execution in Unix-like systems.

  

### Handling Page Swaps and Caching

The kernel swap daemon plays a critical role in managing the recycling of physical memory pages. It ensures that sufficient free pages are maintained, which may involve reducing the size of caches or actively swapping out shared memory pages. This intelligent management keeps the system responsive under varying workloads.

## The Linux Command Line Ch. 10

## Thread Pool Pattern

### Understanding Threads

- A thread is defined as the smallest unit of processing that can be performed by an operating system and is characterized as a lightweight process.
- In Java, a process functions as a self-contained execution environment with its own memory space and resources, while threads allow for multiple lightweight processes to execute independently or concurrently.

### Overview of Multithreading
- Multithreading enables a CPU to perform multiple processes or threads at the same time.
- This concept can be illustrated with the analogy of a one-way street converting into a four-lane highway, which allows many vehicles to travel simultaneously instead of waiting in line.


### Thread Pool Pattern

- The Thread Pool Pattern is an effective method for managing concurrent requests by efficiently handling multiple requests within resource limits.
- It reduces the overhead associated with thread creation and destruction while providing stability and performance improvements.
- In this pattern, tasks are queued and placed into a defined number of thread slots in the pool.
- For instance, with a fully utilized pool, six threads may process tasks at the same time.

## Docker Engine API

## IPC

### Inter-Process Communication (IPC) Overview

- IPC is essential for allowing processes and threads to exchange data and coordinate actions, contributing to the effectiveness, modularity, and simplicity of software systems.
- There are two main types of IPC methods: shared memory and message passing. Each has different characteristics and implementation strategies.
- A distinction is made between independent processes (unaffected by others) and cooperating processes (which can be influenced by other processes), impacting execution efficiency.

### Shared Memory Communication

- Shared memory methods involve processes sharing a common variable, which allows direct information exchange. An example involves a Producer and Consumer where they share a buffer.
- The Producer-Consumer problem demonstrates two versions: unbounded (where the producer continues without limit) and bounded (where production is restricted based on buffer size).
- Pseudo-code shows how shared memory tracks indices for produced and consumed items, implementing synchronization mechanisms such as atomic classes and mutexes to protect shared resources


### Message Passing Communication
- Message passing allows processes to communicate without shared memory, utilizing a link for message transmission that can be direct or indirect.
- Messages can vary in size (fixed or variable) and contain headers for meta-information such as message type, IDs, and control information, typically sent in a FIFO manner.
- Practical challenges include establishing communication links, managing capacities (zero, bounded, or unbounded), and determining synchronization methods (blocking or non-blocking).

### Conclusion on IPC Significance  

- Mastery of IPC mechanisms is vital for understanding modern operating systems and preparing for exams like GATE, where such topics are crucial.
- Effective synchronization ensures data consistency and resolves issues linked to concurrent processes, including race conditions.
- Overall, IPC enhances system capabilities, adaptability, and efficiency, despite its inherent complexity and potential security concerns.


## Garbage Collection

## Anatomy of a Program in Memory

## Transactions in Microservices

