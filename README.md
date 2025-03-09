# Producer-Consumer Problem using Semaphores in C++

## **Overview**
This is a multithreaded C++ implementation of the classic **Producer-Consumer Problem** using **semaphores** for synchronization. 

- The **Producer** adds items to a shared queue (`buffer`).
- The **Consumer** removes items from the queue.
- Semaphores ensure proper coordination between producer and consumer threads to prevent race conditions and deadlocks.

---

## **How it Works**
- `empty_slots` **(Semaphore)** keeps track of available buffer slots.
- `filled_slots` **(Semaphore)** tracks items available for consumption.
- `std::mutex` ensures safe access to the shared buffer (`std::queue<int>`).
- Two threads (`producerThread`, `consumerThread`) run concurrently to add and remove items.

---

## **Prerequisites**
- C++ compiler supporting **C++11** or later.
- Threading library (`<thread>`, `<mutex>`, `<condition_variable>`).

---

## **Compilation & Execution**
### **Compile**
```sh
g++ -std=c++11 producer_consumer.cpp -o producer_consumer -lpthread
