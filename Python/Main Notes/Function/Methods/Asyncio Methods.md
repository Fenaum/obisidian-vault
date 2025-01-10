### Tags: 
### References: [[Method]], [[Async Function]]

## Notes:

**a. asyncio.sleep(seconds)**
Simulates non-blocking delays.

**b. asyncio.gather(*coroutines)**
Runs multiple coroutines concurrently and waits for all of them to complete.

**c. asyncio.create_task(coroutine)**
Schedules a coroutine to run in the background.

Example:
```python
import asyncio

async def background_task():
    await asyncio.sleep(2)
    print("Background task completed")

async def main():
    task = asyncio.create_task(background_task())
    print("Main task running")
    await task  # Waits for the background task to complete

asyncio.run(main())
```