# 0x03. Queuing System in JavaScript

## Description

This project focuses on implementing a queuing system using **JavaScript** with **Redis** as the backend and **Kue** for queue management. You'll build applications that interact with a Redis server to manage data, queues, and publish/subscribe messaging.

---

## Learning Objectives

By the end of this project, you will learn how to:
- Run a Redis server and interact with it.
- Use the Redis Node.js client for basic and advanced operations.
- Manage hash values and asynchronous operations in Redis.
- Build an Express app integrated with Redis and Kue.
- Implement a publish/subscribe pattern with Redis.

---

## Technologies Used

- **Back-end:** Node.js, Express.js, Redis
- **Queue Management:** Kue
- **Language:** JavaScript (ES6)
- **Redis Version:** 6.0.10 or higher
- **Operating System:** Ubuntu 18.04
- **Package Management:** npm
- **Babel:** For ES6+ support

---

## Project Requirements

- Ensure Redis server version is 6.0.10 or higher.
- Use ES6 syntax with Babel for compatibility.
- Use asynchronous operations and callbacks where required.
- Ensure all files end with a new line.

---

## Setup Instructions

### 1. Install Redis
1. Download and install Redis:
    ```bash
    $ wget http://download.redis.io/releases/redis-6.0.10.tar.gz
    $ tar xzf redis-6.0.10.tar.gz
    $ cd redis-6.0.10
    $ make
    ```
2. Start the Redis server:
    ```bash
    $ src/redis-server &
    ```
3. Verify the installation:
    ```bash
    $ src/redis-cli ping
    PONG
    ```

### 2. Initialize the Project
1. Clone the repository:
    ```bash
    git clone https://github.com/<username>/alx-backend.git
    cd 0x03-queuing_system_in_js
    ```
2. Install dependencies:
    ```bash
    npm install
    ```

---

## Files Overview

### Redis Client Operations
1. **`0-redis_client.js`**  
   Establishes a Redis client connection and handles error logging.
2. **`1-redis_op.js`**  
   Implements basic Redis operations using callbacks.
3. **`2-redis_op_async.js`**  
   Demonstrates Redis operations with async/await using Promisify.
4. **`4-redis_advanced_op.js`**  
   Stores and retrieves hash values in Redis.

### Publisher and Subscriber
1. **`5-subscriber.js`**  
   Subscribes to a Redis channel and listens for messages.
2. **`5-publisher.js`**  
   Publishes messages to a Redis channel with a delay.

---

## Running the Application

### Redis Client Examples
Run individual scripts using:
```bash
npm run dev <filename>.js
```

### Publish/Subscribe Example
1. Open two terminals:
   - Terminal 1 (Subscriber):
     ```bash
     npm run dev 5-subscriber.js
     ```
   - Terminal 2 (Publisher):
     ```bash
     npm run dev 5-publisher.js
     ```

---

## Tasks Progress

### Completed Tasks
- Install and configure Redis.
- Set up Node.js Redis client.
- Implement Redis basic and advanced operations.
- Create hash operations in Redis.
- Develop publisher and subscriber scripts.

---
