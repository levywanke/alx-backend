# Queuing System in JS

## Curriculum
This project is part of a short specialization in Back-end development. It covers the following technologies and concepts:
- JavaScript (ES6)
- Redis
- NodeJS
- ExpressJS
- Kue

**Project Duration:**  

## Resources
Before you begin, you should read or watch the following:
- [Redis quick start](https://redis.io/docs/getting-started/)
- [Redis client interface](https://redis.io/docs/manual/clients/)
- [Redis client for Node JS](https://github.com/NodeRedis/node-redis)
- [Kue deprecated but still used in the industry](https://github.com/Automattic/kue)

## Learning Objectives
By the end of this project, you should be able to:
1. Run a Redis server on your machine.
2. Perform basic operations with the Redis client.
3. Use a Redis client with Node JS for basic operations.
4. Store hash values in Redis.
5. Handle asynchronous operations with Redis.
6. Use Kue as a queue system.
7. Build a basic Express app interacting with a Redis server.
8. Build an Express app that interacts with both a Redis server and a queue.

## Requirements
- Your code will be compiled/interpreted on Ubuntu 18.04 with Node 12.x and Redis 5.0.7.
- All files should end with a new line.
- A `README.md` file at the root of the project folder is mandatory.
- Use the `.js` file extension for your JavaScript code.

## Required Files for the Project
- `package.json`
- `.babelrc`

Don't forget to run `$ npm install` after setting up your `package.json` file.

## Tasks

### 0. Install a Redis Instance
**Objective:**  
Install and run a Redis server on your machine.

**Commands:**
```sh
$ wget http://download.redis.io/releases/redis-6.0.10.tar.gz
$ tar xzf redis-6.0.10.tar.gz
$ cd redis-6.0.10
$ make
$ src/redis-server &
$ src/redis-cli ping
PONG
```
### 1. Node Redis Client
**Objective:**  
Connect to the Redis server using a Node JS client.

**Requirements:**
- Log successful or failed connection messages to the console.

### 2. Node Redis Client and Basic Operations
**Objective:**  
Create a script that performs basic operations in Redis.

**Functions:**
- `setNewSchool(schoolName, value)`
- `displaySchoolValue(schoolName)`

### 3. Node Redis Client and Async Operations
**Objective:**  
Use ES6 `async/await` to handle asynchronous operations in Redis.

### 4. Node Redis Client and Advanced Operations
**Objective:**  
Store and retrieve hash values in Redis.

### 5. Node Redis Client Publisher and Subscriber
**Objective:**  
Create a basic queuing system using Redis channels.

### 6. Create the Job Creator
**Objective:**  
Use Kue to create jobs and push them into a queue.

### 7. Create the Job Processor
**Objective:**  
Process jobs from a Kue queue.

### 8. Track Progress and Errors with Kue: Job Creator
**Objective:**  
Create a series of jobs and track their progress and errors using Kue.

### 9. Track Progress and Errors with Kue: Job Processor
**Objective:**  
Process jobs while handling blacklisted numbers and tracking job progress.