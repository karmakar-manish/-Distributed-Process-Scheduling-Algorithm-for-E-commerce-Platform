# Priority-Based Process Scheduling for Distributed E-Commerce Platforms

## Project Overview

This project involves designing and implementing a priority-based process scheduling algorithm for a distributed e-commerce platform. The system handles millions of transactions daily across multiple servers, each dedicated to specific transaction types. The algorithm optimizes resource allocation among worker threads, prioritizes processing requests based on thread priority levels, and accommodates varying resource demands for different transaction types.

## System Architecture

- **Multiple Servers**: Each server manages a specific type of transaction (e.g., payment processing, order handling).
- **Worker Threads**: Each server has a pool of worker threads, each characterized by:
  - **Priority Level**: Dictates the order in which threads are scheduled.
  - **Resources**: Defines the number of requests a thread can handle concurrently.

## Request Handling

1. **Request Queueing**: Incoming requests are initially queued and directed to the appropriate service.
2. **Thread Assignment**: Requests are further queued and assigned to worker threads based on priority levels.

## Algorithm Design

The algorithm is designed to:

- **Efficient Resource Allocation**: Allocate resources to worker threads efficiently for request processing.
- **Priority Consideration**: Prioritize higher-priority threads for resource allocation. If no higher-priority threads are available, the algorithm falls back to lower-priority threads.
- **Transaction Type Awareness**: Consider varying resource demands for different transaction types (e.g., payment processing vs. order processing).

## Input Specifications

The input consists of:

1. **Number of Services (n)**: Total number of services in the system.
2. **Number of Worker Threads per Service (m)**: Number of worker threads for each service.
3. **Thread Information**: For each worker thread, provide:
   - `priority_level resources`
4. **Request Information**: For each request, provide:
   - `transaction_type resources_required`

## Output Specifications

The output includes:

1. **Order of Processed Requests**: Sequence in which requests were processed.
2. **Average Waiting Time**: Average time requests waited before being processed.
3. **Average Turnaround Time**: Average time taken to process each request from arrival to completion.
4. **Number of Requests Rejected**: Requests rejected due to insufficient resources.

## High Traffic Handling

During peak traffic periods, the output will also include:

1. **Number of Requests Delayed**: Requests delayed due to resource shortages.
2. **Number of Requests Blocked**: Requests blocked when all worker threads are occupied.

## Usage

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/priority-process-scheduling.git
