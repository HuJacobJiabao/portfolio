---
type: "project"
title: "Weenix - Unix-like Operating System"
createTime: "2024-05-15T12:00:00.000Z"
description: "A comprehensive Unix-like operating system kernel implementation in C, featuring process management, virtual file system, and virtual memory with paging."
tags: ["C","Unix", "Operating Systems", "Kernel Development", "Ubuntu", "VirtualBox", "VFS", "Virtual Memory"]
category: "Kernel Programming"
coverImage: "/content/projects/weenix-operating-system/weenix_cover.svg"
---

# {{title}}


## 1. Project Overview

**Weenix** is a comprehensive Unix-like operating system kernel developed as part of USC's operating systems course (CSCI 402). This project involved implementing a complete, functional operating system kernel from scratch in C, capable of running user programs, managing system resources, and providing essential OS services including process management, file systems, and virtual memory.

The kernel implements core Unix-like functionality and demonstrates a deep understanding of operating system principles through hands-on implementation of fundamental kernel subsystems.

---

*Note: Due to academic integrity policies, the source code for this project cannot be publicly shared. This documentation provides an overview of the implementation approach and technical achievements.*

## 2. System Architecture and Achievements

### 2.1 Process Management and Threading

Our implementation provides a complete process management system with sophisticated threading capabilities:

**Process Control and Lifecycle Management**
- Implemented comprehensive Process Control Blocks (PCBs) that maintain process state, including process ID, parent-child relationships, memory mappings, and file descriptor tables
- Built a complete process lifecycle system supporting process creation, execution, termination, and cleanup
- Developed process hierarchy management with proper orphan process reparenting to the init process

**Kernel Threading System**
- Engineered a cooperative threading system supporting concurrent execution of multiple kernel threads
- Implemented low-level context switching using assembly language routines for efficient thread transitions
- Built thread scheduling infrastructure supporting runnable, sleeping, and terminated thread states
- Created thread synchronization primitives including mutexes and condition variables for coordinating access to shared resources

**Technical Implementation Details:**
- Context switching implemented in assembly language for minimal overhead
- Thread stacks allocated using kernel page allocator with guard pages for overflow detection
- Scheduler maintains separate queues for runnable and sleeping threads
- Process creation uses copy-on-write semantics for efficient memory usage

### 2.2 Virtual File System (VFS) Implementation

Developed a complete virtual file system layer providing a unified interface for file operations:

**VFS Abstraction Layer**
- Implemented a flexible VFS architecture supporting multiple filesystem types through a common interface
- Built VNode (virtual node) abstraction representing files and directories with unified operations
- Created a sophisticated pathname resolution system supporting absolute and relative paths, symbolic links, and special directory entries (. and ..)

**File Operations and Management**
- Implemented complete POSIX-style file operations including open, read, write, close, seek, and stat
- Built file descriptor management with per-process file descriptor tables and proper reference counting
- Developed directory operations supporting creation, deletion, and traversal
- Integrated with the S5FS (System V File System) for persistent storage capabilities

**Technical Implementation Details:**
- VNodes maintain reference counts for proper memory management and cleanup
- File descriptor tables use array-based allocation with efficient lookup
- Path resolution implements recursive descent parsing with cycle detection
- Integration with memory management system for file-backed memory mappings

### 2.3 Virtual Memory Management System

Implemented a sophisticated virtual memory management system with demand paging:

**Virtual Address Space Management**
- Built per-process virtual address spaces with complete isolation between processes
- Implemented Virtual Memory Areas (VMAs) representing contiguous memory regions with specific permissions and characteristics
- Created address space mapping infrastructure supporting file-backed and anonymous memory regions

**Demand Paging and Memory Protection**
- Developed a demand paging system that loads pages into memory only when accessed, reducing memory overhead
- Implemented page fault handling for both minor faults (page not in memory) and major faults (protection violations)
- Built copy-on-write semantics for efficient process creation and memory sharing
- Created memory protection mechanisms enforcing read, write, and execute permissions per page

**Memory Mapping and System Calls**
- Implemented mmap/munmap system calls supporting both file-backed and anonymous memory mappings
- Built brk() system call for dynamic heap management
- Integrated virtual memory system with the VFS layer for file-backed mappings

**Technical Implementation Details:**
- Page tables implemented using hardware MMU with 4KB page granularity
- Page fault handler distinguishes between legitimate faults and segmentation violations
- Copy-on-write implemented through page protection and fault handling
- Memory regions tracked using efficient data structures for fast lookup and manipulation

## 3. System Integration and Functionality

### 3.1 System Call Interface
- Implemented over 20 POSIX-compatible system calls providing the interface between user and kernel space
- Built system call dispatch mechanism with proper argument validation and error handling
- Integrated process management, file system, and memory management through coordinated system call implementation

### 3.2 Inter-Process Communication
- Developed basic IPC mechanisms including process signaling and shared memory regions
- Implemented process synchronization primitives accessible from user space
- Built process coordination mechanisms supporting parent-child communication through wait/exit paradigms

### 3.3 Kernel Infrastructure
- Created comprehensive kernel debugging and assertion framework for development and testing
- Built kernel memory management using slab allocators for efficient kernel object allocation
- Implemented kernel synchronization primitives ensuring thread-safe operation of kernel data structures

## 4. Technical Specifications

### 4.1 Performance Characteristics
- **Context Switch Latency**: Optimized assembly routines achieving minimal switching overhead
- **Memory Efficiency**: Copy-on-write and demand paging reduce memory footprint
- **Scalability**: System supports 100+ concurrent processes with efficient resource management
- **I/O Performance**: Streamlined VFS layer minimizes abstraction overhead

### 4.2 Code Metrics
- **Total Implementation**: Approximately 4,500 lines of C code across kernel subsystems
- **Files Modified**: 15+ kernel source files spanning process, file system, and memory management
- **System Calls**: 20+ POSIX-compatible system calls implemented
- **Test Coverage**: Comprehensive test suites validating functionality across all kernel modules

## 5. Development and Testing

### 5.1 Testing Framework
The kernel includes an extensive testing infrastructure:
- **Faber Test Suite**: Core functionality tests validating individual kernel components
- **Stress Testing**: Multi-process scenarios testing system behavior under load
- **Integration Testing**: Cross-subsystem tests ensuring proper interaction between kernel modules
- **Edge Case Testing**: Boundary condition and error handling validation

### 5.2 Development Environment
- **Build System**: Make-based compilation with modular kernel configuration
- **Debugging Tools**: GDB integration with kernel-aware debugging support
- **Emulation**: QEMU-based testing environment for safe kernel development
- **Version Control**: Git-based development with incremental feature implementation
