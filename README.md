# Introduction to NodeJS

**Node.js is an open-source, cross platform JavaScript runtime environment that lets you run JavaScript code outsite of a web browser**. Node.js enables developers to build server-side and network applications.

## Node.js based on non-blocking and event-driven architecture

The non-blocking and event driven architecture is a core feature of Node.js that enables it to handle multiple tasks simultaneously without waiting for any one task to complete.

### Non-blocking architecture

In a non-blocking architecture, the program initiates and operation (e.g reading a file) and immediately moves on the other task without waiting for it to finish. Once the operation is complete it notifies the program (via a callback or an event).

### Event-driven architecture

Node.js uses an event loop to handle asynchronous operations. Instead of using multiple threads to manage tasks, the single-threaded event loop continuously checks for events and processes them. When an asynchronous operation is initiated (e.g., reading a file), Node.js offloads the task to the underlying system (e.g., the OS or a worker thread). Meanwhile, Node.js continues processing other tasks in the event loop. When the operation is complete, a notification is sent to the event loop, which executes the associated callback function.

**Illustration of Non-blocking, Event-driven Flow**

Let’s say you’re running a Node.js server that processes multiple HTTP requests:

1. Request 1 asks to fetch data from a database.
2. Node.js sends the query to the database and moves on to Request 2.
3. Request 2 asks for a static file. Node.js sends the file reading task to the file system and moves on to Request 3.
4. As the database or file system completes tasks, they notify the event loop, which then executes the callbacks for Request 1 and Request 2.

This allows the server to handle many requests simultaneously, without getting stuck on any single operation.

## Other key features of Node.js

**JavaScript Everywhere:**

Node.js uses JavaScript as its programming language, allowing developers to use single language for both client and server side development.

**NPM (Node Package Manager):**

Node.js comes with NPM, the world’s largest software registry, providing a vast collection of libraries and tools to speed up development.

**Cross-platform:**

Node.js applications can run on various operating systems like Windows, macOS, and Linux, making it highly versatile.

**Scalability:**

Its non-blocking I/O and event-driven model make Node.js suitable for applications requiring high scalability, such as real-time chat applications, streaming services, and APIs.

## Common use cases of Node.js

**Web servers:**

Node.js is used to build scalable web servers capable of handling multiple requests simultaneously.

**Real-time Applications:**

Applications like chat apps, online gaming, and collaborative tools benefit from Node.js’s low-latency and event-driven nature.

**RESTful APIs:**

Node.js simplifies creating and managing APIs for web and mobile applications.

**Microservices:**

It is widely used in building microservices due to its lightweight nature.
