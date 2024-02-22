# Speed Optimization Challenge for Message-Distribution Systems
### Theme: Infrastructure
### Prize: $1,000

## Objective   
To develop the most efficient message-distribution implementation that ensures minimal latency and variance in message delivery across different scenarios, involving both one-to-many and many-to-many publisher and subscriber connections.

### Product Milestones:

- **Implementation Design:**  
  Create a scalable and efficient architecture capable of handling one-to-many and many-to-many connections with the least possible latency.
- **Technology Selection:**  
  Choose between gRPC or web sockets for message distribution, considering the trade-offs in terms of speed, reliability, and ease of implementation.
- **Optimization:**  
  Apply advanced programming techniques and algorithms to reduce both total latency and latency variance in message distribution.
- **Benchmarking:**  
  Conduct thorough testing against the specified benchmarks to measure and refine the system's performance.
- **Documentation:**  
  Prepare comprehensive documentation detailing the architecture, choice of technology, and optimization strategies employed.

### Key Milestones for Hackathon (MVP Expectations):

- **Prototype Development:**  
  Develop a functional prototype capable of efficiently managing one-to-many and many-to-many message distribution with an emphasis on low latency.
- **Performance Optimization:**  
  Fine-tune the prototype to optimize for both total latency and latency variance across all benchmark tests.
- **Benchmark Testing:**  
  Execute the benchmark tests to gather performance data, identifying areas for improvement.
- **Presentation and Documentation:**  
  Present the prototype, including a demonstration of benchmark tests, architectural choices, and future scalability plans.

### Benchmarks for Evaluation:

1. **One-to-Many, Total Latency:**  
   Test the system with one publisher and 1000 subscribers, measuring the total latency to distribute a message.
2. **One-to-Many, Latency Variance:**  
   Measure the latency difference between the first and last receiver in a one-to-many distribution scenario.

### Benchmarks for Evaluation (Bonus):

1. **Many-to-Many, Total Latency:**  
   In a scenario with 1000 publishers and 1000 subscribers messaging simultaneously, measure the average total latency.
2. **Many-to-Many, Latency Variance:**  
   Assess the average latency difference among all publishers in a many-to-many context.

### Scoring System:

- For each benchmark, the position of the team's implementation in terms of latency (POS) will determine their score, awarded as (5 - POS) points.
- The team with the highest total points across all benchmarks will be declared the winner.

### Starter Code: 
- See [sockets sample](https://github.com/synoptic-com/bounty-infra/tree/main/sockets)
- See [grpc sample](https://github.com/synoptic-com/bounty-infra/tree/main/grpc)

### **Infrastructure and Technical Specifications:**

- **Protocol:**  
  Teams can choose between gRPC and web sockets for their implementations.
    - For sockets, the message format should be
    
    ```jsx
    {
    	author: int // author id
    	data: str // 1 kB of data
    }
    ```
    
    - If you choose gRPC, use the following proto definition.
    
    ```jsx
    syntax = "proto3";
    
    message Message {
      int32 author = 1;
      string data = 2;
    }
    ```
    
- **Cloud Instance Specification:**  
  All benchmarks will be performed on an AWS t3.2xlarge instance, equipped with 8 CPUs and 32 GB RAM, running Ubuntu 22.04 LTS. This standardized environment ensures a fair comparison of the performance across all participating teams.
- Sample implementations with GO + gRPC and Bun.js + sockets can be found in our GitHub repository [here](https://github.com/synoptic-com/bounty-infra). Please read the README files for implementation details.
