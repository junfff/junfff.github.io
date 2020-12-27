---
title: Rust::Channels
date: 2020-12-27 23:46:22 +/-TTTT
categories: [Rust]
tags: [Rust]
---

# Flavors:
  - Synchronous channels: Channel where send() can block. Limited capacity.
   -- Mutex + Condvar + VecDeque
   -- Atomic VecDeque (atomic queue) + thread::pack + thread::Thread::notify
  - Asynchronous channels: Channel where send() cannot block. Unbounded.
   -- Mutex + Condvar + VecDeque
   -- Mutex + Condvar + LinkedList
   -- AtomicLinkedList or Atomic Queue
   -- Atomic linked list, linked list of T
   -- Atomic block linked list, linked of atomic VecDeque<T>
  - Rendezvous channels: Synchronous with capacity = 0. Used for thread synchronization.
  - Oneshot channels: Any capacity. In practice, only one call to send().
