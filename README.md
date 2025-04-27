# Multithreaded Web Server

This repository contains an implementation of a multithreaded web server in Rust.

## Overview

The server demonstrates Rust's concurrency capabilities by handling multiple connections simultaneously using a thread pool architecture. This implementation showcases key Rust concepts such as:

- Thread management
- Thread pools
- MPSC (Multiple Producer, Single Consumer) channels
- Safe concurrency patterns
- Error handling

## Features

- Configurable thread pool for handling concurrent connections
- Graceful request handling and response generation
- Basic HTTP request parsing
- Static file serving capabilities
- Clean shutdown mechanism

## Implementation Details

The server uses a thread pool to manage a predefined number of worker threads. When a new connection arrives, it's passed to an available worker thread for processing rather than spawning a new thread for each connection, which provides better resource utilization and performance.

## Usage

To run the server:

```
cargo run
```

The server will start listening on `127.0.0.1:7878` by default.

## Testing

You can test the server by opening a web browser and navigating to:
```
http://127.0.0.1:7878
```
