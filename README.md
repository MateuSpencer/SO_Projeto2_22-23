# Operating Systems — Project 2

**Course:** Operating Systems (Sistemas Operativos) — IST, University of Lisbon
**Year:** 2022/2023
**Group:** 67 — Mateus Spencer & Guilherme Peixoto

## Description

Implementation of a **message broker** (mbroker) supporting a **publish-subscribe** messaging pattern over named pipes (FIFOs):

- **Publisher** sends messages to named topics
- **Subscriber** receives messages from subscribed topics
- **Manager** controls broker operations (create/remove boxes, list)
- **Producer-Consumer** queue with thread-safe synchronization

Built on top of the TécnicoFS in-memory file system from Project 1.

## Technologies

- **Language:** C
- **IPC:** Named Pipes (FIFOs)
- **Concurrency:** POSIX Threads, condition variables, mutexes
- **Build:** Makefile

## How to Run

```bash
make
./mbroker <pipename> <max_sessions>
./pub <pipe_path> <box_name>
./sub <pipe_path> <box_name>
./manager <pipe_path> <action> [box_name]
```

## Project Structure

```
mbroker/           # Message broker server
publisher/         # Publisher client
subscriber/        # Subscriber client
manager/           # Management client
producer-consumer/ # Thread-safe queue
protocol/          # Wire protocol definition
fs/                # TécnicoFS (in-memory file system)
```

## Course Link

[Project specification](https://github.com/tecnico-so/enunciado-proj-so-2022-23)
