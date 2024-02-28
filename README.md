# PyPool implementation for running non-blocking tasks

PyPool is a pyo3 based implementation for running non-blocking tasks in a pool of threads. It is designed to be used in a similar way to the `ThreadPool` from the `concurrent.futures` module in the standard library, but with the added benefit of being able to run non-blocking tasks.

## Why PyPool?

GIL (Global Interpreter Lock) is a mutex that protects access to Python objects, preventing multiple threads from executing Python bytecodes at once. This means that Python threads are not suitable for CPU-bound tasks, as they will not be able to take advantage of multiple cores. However, Python threads are still useful for I/O-bound tasks, as they can be used to perform non-blocking I/O operations.

PyPool is designed to be used in a similar way to the `ThreadPool` from the `concurrent.futures` module in the standard library, but with the added benefit of being able to run non-blocking tasks. This makes it suitable for running I/O-bound tasks in a pool of threads, without the need to use the `asyncio` module.
