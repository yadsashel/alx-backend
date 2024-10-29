# Caching Project - 0x01
This project focuses on implementing different caching strategies for a backend system in Python. The main objective is to create various cache replacement policies, which are used to manage memory effectively when dealing with limited resources. By the end of this project, you will gain practical knowledge about different caching algorithms, such as FIFO, LIFO, LRU, MRU, and LFU, and how they function in a real-world system.

---

## Learning Objectives
After completing this project, you will understand:
- **What a caching system is** and its purpose in backend systems.
- Various **cache replacement policies**:
  - **FIFO (First In, First Out)**
  - **LIFO (Last In, First Out)**
  - **LRU (Least Recently Used)**
  - **MRU (Most Recently Used)**
  - **LFU (Least Frequently Used)**
- **The limitations** of a caching system, particularly when managing finite memory resources.

---

## Project Structure

1. **BasicCache**: A caching system without any item limit, simply storing all data provided.
2. **FIFOCache**: Implements FIFO (First In, First Out) caching.
3. **LIFOCache**: Implements LIFO (Last In, First Out) caching.
4. **LRUCache**: Implements LRU (Least Recently Used) caching.
5. **MRUCache**: Implements MRU (Most Recently Used) caching.

---

## Requirements
- **Python Version**: This project requires Python 3.7, and all code should be compatible with Ubuntu 18.04 LTS.
- **Coding Style**: Follow `pycodestyle` (version 2.5) for code styling.
- **Documentation**: Ensure each module, class, and function has descriptive docstrings explaining its purpose and behavior.

### BaseCaching Class
All cache classes must inherit from `BaseCaching`, which provides:
- **Attributes**:
  - `MAX_ITEMS`: The maximum number of items allowed in the cache.
  - `cache_data`: A dictionary for storing cached items.
- **Methods**:
  - `put`: To add an item to the cache (to be implemented in each class).
  - `get`: To retrieve an item from the cache (to be implemented in each class).

---

## Tasks Overview

### Task 0: Basic Dictionary
- Implement a `BasicCache` class, a caching system with no item limit.
- **Methods**:
  - `put`: Adds items to the cache.
  - `get`: Retrieves items from the cache.

### Task 1: FIFO Caching
- Implement a `FIFOCache` class with a max item limit.
- **Behavior**: When the cache limit is reached, it discards the **oldest item** in the cache.
- **Methods**:
  - `put`: Adds items, discarding the oldest when full.
  - `get`: Retrieves items.

### Task 2: LIFO Caching
- Implement a `LIFOCache` class with a max item limit.
- **Behavior**: Discards the **most recently added item** when the limit is exceeded.
- **Methods**:
  - `put`: Adds items, discarding the newest when full.
  - `get`: Retrieves items.

### Task 3: LRU Caching
- Implement an `LRUCache` class with a max item limit.
- **Behavior**: Discards the **least recently used** item when the cache is full.
- **Methods**:
  - `put`: Adds items, discarding the least recently used when full.
  - `get`: Retrieves items and marks them as recently used.

### Task 4: MRU Caching
- Implement an `MRUCache` class with a max item limit.
- **Behavior**: Discards the **most recently used** item when the cache is full.
- **Methods**:
  - `put`: Adds items, discarding the most recently used when full.
  - `get`: Retrieves items.

---

## Repository
- **GitHub Repository**: `alx-backend`
- **Directory**: `0x01-caching`

---

## Getting Started
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/alx-backend.git
   cd alx-backend/0x01-caching
   ```
2. Run each module's main test file to check the behavior of the caching policies.

---

## Testing
Each caching algorithm has test files provided (e.g., `0-main.py`, `1-main.py`) that demonstrate the expected functionality of the caching strategies. Run these scripts to validate your implementation.
