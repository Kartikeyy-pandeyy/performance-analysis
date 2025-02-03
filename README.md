# 🚀 Performance Analysis of Docker Containers & Virtual Machines

<p align="center">
  <img src="https://img.shields.io/badge/Virtualization-Docker-blue?style=for-the-badge&logo=docker" alt="Docker">
  <img src="https://img.shields.io/badge/Virtualization-VM-red?style=for-the-badge&logo=vmware" alt="VM">
  <img src="https://img.shields.io/badge/Cloud-Computing-green?style=for-the-badge&logo=cloudflare" alt="Cloud">
  <img src="https://img.shields.io/badge/Database-PostgreSQL-blue?style=for-the-badge&logo=postgresql" alt="PostgreSQL">
</p>

---

## 📌 Abstract
> Virtualization plays a crucial role in cloud and DevOps environments. This research evaluates **Docker containers** and **Virtual Machines (VMs)** using four key performance metrics: **CPU processing, Disk I/O, Database operations, and Web server throughput**. Our study provides insights into the trade-offs between these technologies to help administrators make informed infrastructure decisions.

---

## 👨‍💻 Authors

| Name              | Institution & Email |
|------------------|----------------------|
| **Kartikey Pandey** | Bennett University, India <br> 📩 [kartikeyy.pandeyy@gmail.com](mailto:kartikeyy.pandeyy@gmail.com) |
| **Ritika Sharma** | Bennett University, India <br> 📩 [cheimonas31@gmail.com](mailto:cheimonas31@gmail.com) |
| **Lakshya Deewan** | Bennett University, India <br> 📩 [e22cseu1012@bennett.edu.in](mailto:e22cseu1012@bennett.edu.in) |
| **Aditya Bhardwaj** | Bennett University, India <br> 📩 [aditya.bhardwaj@bennett.edu.in](mailto:aditya.bhardwaj@bennett.edu.in) |

## Performance Benchmarks
This research compares Docker containers and Virtual Machines (VMs) in the context of several performance benchmarks across different categories. Below are the results for the benchmark metrics:

## Database Server

| Benchmark Category        | Metric                              | Docker    | VM (Ubuntu on VirtualBox) |
|---------------------------|-------------------------------------|-----------|---------------------------|
| **STREAM Benchmark**       | Copy (Rate MB/s)                   | 5808.3    | 5114.2                    |
|                           | Scale (Rate MB/s)                  | 5832.5    | 5151.8                    |
|                           | Add (Rate MB/s)                    | 6210.2    | 5698.4                    |
|                           | Triad (Rate MB/s)                  | 6114.1    | 5655.5                    |
|                           | Array Size                         | 15,00,000 | 15,00,000                 |
| **PostgreSQL Benchmark**   | Total Transactions                 | 2,00,000  | 2,00,000                  |
|                           | Successful Transactions            | 2,00,000  | 2,00,000                  |
|                           | Number of Clients                  | 20        | 20                        |
|                           | Transactions per Client            | 10,000    | 10,000                    |
|                           | Average Latency (ms)              | 9.068     | 12.168                    |
|                           | Initial Connection Time (ms)      | 76.645    | 87.6                      |
|                           | Transactions Per Second (TPS)     | 2205.45   | 1958.8                    |

## Disk I/O

| Benchmark Category        | Metric                              | Docker    | VM (Ubuntu on VirtualBox) |
|---------------------------|-------------------------------------|-----------|---------------------------|
| **Sysbench**               | Reads/s                             | 67.82     | 58.2                      |
|                           | Writes/s                            | 45.21     | 38.3                      |
|                           | Fsyncs/s                            | 144.78    | 125.9                     |
|                           | Throughput Read (MiB/s)            | 1085.13   | 920.1                     |
|                           | Throughput Written (MiB/s)         | 723.42    | 625.2                     |
|                           | Total Time (s)                     | 60.1579   | 66.5989                   |
|                           | Total Number of Events             | 15,382    | 14,800                    |
|                           | Latency (ms)                       | 3.9       | 4.8                       |
|                           | 95th Percentile Latency (ms)      | 8.9       | 10.7                      |
|                           | Events                              | 15,382    | 14,800                    |
|                           | Execution Time (s)                 | 59.9276   | 66.2                      |
| **Dbench**                 | NTCreateX                          | 2,39,09,380 | 2,15,00,000             |
|                           | Close                               | 1,75,63,945 | 1,60,00,000             |
|                           | Rename                              | 10,12,316  | 9,50,000                 |
|                           | Unlink                              | 48,27,949  | 43,00,000                |
|                           | Deltree                             | 600        | 570                      |
|                           | Mkdir                               | 300        | 285                      |
|                           | Qpathinfo                           | 2,16,71,417 | 1,95,00,000            |
|                           | Qfileinfo                           | 37,97,406  | 34,50,000                |
|                           | Qfsinfo                             | 39,73,078  | 37,00,000                |
|                           | Sfileinfo                           | 19,47,894  | 17,80,000                |
|                           | Find                                | 83,77,806  | 78,00,000                |
|                           | WriteX                              | 1,19,19,383 | 1,09,00,000             |
|                           | ReadX                               | 3,74,70,901 | 3,45,00,000             |
|                           | LockX                               | 77,804     | 72,000                   |
|                           | UnlockX                             | 77,804     | 72,000                   |
|                           | Flush                               | 16,75,838  | 15,00,000                |
|                           | Throughput (MB/s)                  | 1250.71   | 1050                      |

## Web Server

| Benchmark Category        | Metric                              | Docker    | VM (Ubuntu on VirtualBox) |
|---------------------------|-------------------------------------|-----------|---------------------------|
| **Apache**                 | Time taken for tests (s)           | 0.332     | 0.37                      |
|                           | Total transferred bytes            | 1,09,45,000 | 1,04,00,000              |
|                           | HTML transferred bytes             | 1,06,71,000 | 1,02,00,000             |
|                           | Requests per second                | 3010.97   | 2700                      |
|                           | Time per request (ms)             | 33.212    | 37.5                      |
|                           | Transfer rate (Kbytes/s)           | 32,182.67 | 29,500                    |
| **Nginx**                  | Time taken for tests (s)           | 0.201     | 0.23                      |
|                           | Total transferred bytes            | 1,09,16,000 | 1,03,00,000             |
|                           | HTML transferred bytes             | 1,06,71,000 | 1,02,00,000             |
|                           | Requests per second                | 4965.56   | 4500                      |
|                           | Time per request (ms)             | 20.139    | 22.5                      |
|                           | Transfer rate (Kbytes/s)           | 52,933.69 | 47,500                    |

## CPU Intensive

| Benchmark Category        | Metric                              | Docker    | VM (Ubuntu on VirtualBox) |
|---------------------------|-------------------------------------|-----------|---------------------------|
| **Geekbench**              | Execution Time (s)                 | 131.641   | 138                       |
|                           | CPU Usage (%)                      | 99.8      | 97.5                      |
|                           | Memory Usage (MB)                  | 863.5     | 940                       |
|                           | Threads Used                        | 5         | 5                         |
|                           | Single-Core Score                  | 1475      | 1410                      |
|                           | Multi-Core Score                   | 4708      | 4400                      |
| **Sysbench**               | Execution Time (s)                 | 10.0002   | 10.5                      |
|                           | CPU Usage (%)                      | 99.35     | 97.8                      |
|                           | Memory Usage (MB)                  | 317.64    | 380                       |
|                           | Threads Used                        | 1         | 1                         |
|                           | MiB                                | 6.457     | 6.2                       |
## Conclusion
This study provides a detailed comparison of Docker containers and Virtual Machines, highlighting their respective strengths and trade-offs. Docker containers offer faster performance for CPU and I/O-bound tasks, making them ideal for scalable cloud-native applications. On the other hand, Virtual Machines excel in resource isolation and stability under heavy workloads. Understanding these differences enables system administrators and engineers to choose the most suitable technology for their specific infrastructure needs, optimizing both performance and resource utilization.

