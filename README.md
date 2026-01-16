# 🚀 Scalable Leaderboard System (Spring Boot)

A **pluggable, time-window–based leaderboard system** built using **Spring Boot**, designed to support **multiple Top-K ranking strategies** while following **SOLID principles** and clean architecture practices.

This project focuses on **system design, scalability, and extensibility**, rather than just CRUD functionality.

---

## ✨ Features

- ✅ Supports **Daily / Weekly / Monthly** leaderboards
- ✅ **Pluggable Top-K strategies** using Strategy + Factory patterns
- ✅ Runtime selection of ranking algorithms
- ✅ Designed for scalability and maintainability
- ✅ Clean separation of concerns (API, Service, Strategy, Windowing)

---

## 🧠 Supported Top-K Strategies

| Strategy | Description | Use Case |
|--------|-------------|----------|
| **Redis Sorted Set** | Uses Redis ZSET for exact Top-K | Real-time, large-scale leaderboards |
| **In-Memory Heap** | PriorityQueue-based Top-K | Small datasets, testing |
| **Approximate Top-K** | Count-Min Sketch | High-throughput, memory-efficient ranking |

> All strategies implement a common `TopKStrategy` interface and can be swapped without changing business logic.

---
