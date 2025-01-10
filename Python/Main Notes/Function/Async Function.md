### Tags: 
### References: [[Function]]

## Notes:

In Python, asynchronous programming enables you to write non-blocking code that performs tasks concurrently, such as handling multiple I/O-bound operations (e.g., network requests or file reads/writes) without waiting for one to finish before starting another. This is especially useful for applications like web servers, data processing, or anything involving multiple tasks running in parallel.

---
Asynchronous functions in Python are defined using the async def syntax. These functions return a special object called a **coroutine**, which can be awaited using the await keyword.

**a. async Keyword**
• Marks a function as asynchronous.
• The function doesn’t execute immediately but instead returns a coroutine object.

**b. await Keyword**
• Suspends the execution of the coroutine until the awaited operation is complete.
• Only works inside an async def function.
• Used with “awaitable objects” like coroutines or asynchronous I/O operations.

**c. Event Loop**
• The core of asynchronous programming.
• It manages and schedules the execution of coroutines.

---
```python
import asyncio  # Required for async operations

async def say_hello():
    print("Hello")
    await asyncio.sleep(1)  # Simulates a non-blocking delay
    print("World")

# Running the coroutine
asyncio.run(say_hello())
```
---
## Blocking Code Example
```python
import time

def main():
    print("Start")
    time.sleep(3)  # Blocks for 3 seconds
    print("End")

main()
```
This blocks the program for 3 seconds, preventing other tasks from running.

---
## Non-blocking Async Code
```python
import asyncio

async def main():
    print("Start")
    await asyncio.sleep(3)  # Non-blocking delay
    print("End")

asyncio.run(main())
```
This allows other tasks to run during the 3-second delay.

---
## Running Multiple Coroutines Concurrently

The true power of async programming is the ability to run tasks concurently
```python
import asyncio

async def task1():
    print("Task 1 started")
    await asyncio.sleep(2)
    print("Task 1 completed")

async def task2():
    print("Task 2 started")
    await asyncio.sleep(1)
    print("Task 2 completed")

async def main():
    await asyncio.gather(task1(), task2())  # Run both tasks concurrently

asyncio.run(main())
```

```Output
Task 1 started
Task 2 started
Task 2 completed
Task 1 completed
```

---
## Using Async with I/O Operations

Async programming shines with I/0-bound tasks like HTTP requests or file operations.

Example: Async HTTP Requests (with aiohttp)
```python
import aiohttp
import asyncio

async def fetch(url):
    async with aiohttp.ClientSession() as session:
        async with session.get(url) as response:
            return await response.text()

async def main():
    urls = ["https://example.com", "https://python.org"]
    results = await asyncio.gather(*(fetch(url) for url in urls))
    for result in results:
        print(result[:100])  # Print the first 100 characters

asyncio.run(main())
```
---
## Error Handling in Async Functions
```python
async def faulty_task():
    raise ValueError("An error occurred!")

async def main():
    try:
        await faulty_task()
    except ValueError as e:
        print(f"Caught an error: {e}")

asyncio.run(main())
```

```Output
Caught an error: An error occurred!
```

---
## [[Asyncio Methods]]

**a. asyncio.sleep(seconds)**
Simulates non-blocking delays.

**b. asyncio.gather(*coroutines)**
Runs multiple coroutines concurrently and waits for all of them to complete.

**c. asyncio.create_task(coroutine)**
Schedules a coroutine to run in the background.

---
**10. Best Practices for Async in Python**

1. **Use Async for I/O-Bound Tasks**:
• Examples: HTTP requests, database queries, file reads/writes.
• Avoid for CPU-bound tasks (use multiprocessing instead).

2. **Avoid Mixing Sync and Async Code**:
• Example: Avoid blocking calls like time.sleep() in async functions.

3. **Leverage** asyncio.gather():
• Use it to manage multiple coroutines concurrently.

4. **Gracefully Handle Exceptions**:
• Always wrap async code with try-except blocks where errors might occur.

5. **Test Async Code Thoroughly**:
• Async code can have subtle bugs due to its concurrent nature.

---

**Summary**

• **Async** enables non-blocking, concurrent operations in Python.
• Use async def and await to define and run coroutines.
• Async is best for I/O-bound tasks and works seamlessly with libraries like aiohttp.
• The asyncio module provides tools to manage coroutines and event loops.
• Python async resembles JavaScript’s async/await with some differences in event-loop handling and syntax.