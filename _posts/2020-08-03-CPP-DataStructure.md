---
title: "CPP STL Container Comparison with Time Complexity"
tags: CPP
date: 2021-08-03 01:57:28 -0400
categories: blogging
---

# Comparing CPP STL Container with time complexity

## Sequenced Containers
- Contains elements in sequenced

### 1. Vector
- Elements are saved as sequenced in memory. Internally, array like structure.
- REMEMBER:  Vector Creates 2*n space when it creates a vector. So it can push back with O(1) time complexity normally. But when its space is full, it creates another double size vector and copy elements to it. In that case its time to push back element is O(n). So we say vector's push back time complexity is `amortized O(1)`.
- Random Access: 
  - O(1)
  - `[]`, `at`
- Search:
  - O(n)
  - `find`
- Insert or delete element at last: 
  - amortized O(1)
  - `push_back`, `pop_back`
- Insert or delete at index: 
  - O(n)
  - `insert`, `erase` 
  - Need to copy elements for insert

### 2. Deque
- Double Ended QUEue.
- Different from Queue that the Deque is available to insert and erase from both front and end.
- The way to use Deque is very similar with Vector. Vector is fast when it calls `push_back` or `pop_back`, but Deque is also fast when it calls `push_front` or `pop_front`. But except that case, Vector is normally faster and smaller then Deque.
- Different from Vector that the Deque doesn't save elements in sequenced memory. Each node has its own memory.
- It is more easy to extend than Vector
- Random Access: 
  - O(1)
  - `at` 
- Search:
  - O(n)
  - `find`
- Insert or delete element at lst: 
  - amortized O(1)
  - `push_back`, `push_front`, `pop_back`, `pop_front`
- Insert at index: 
  - O(n)
  - `insert`, `erase`

### 3. List
- Basically, List is consisted with doubly-linked-list.
- It is not available to random access.
- The advantage of the List is that its insertion by index cost is O(1) for the reason that it only needs to modify link of 2 elements at before and after of the index.
- Random Access: 
  - Not Available
- Search:
  - O(n)
  - `find`
- Insert or delete element
  - O(1)
  - `push_back`, `push_front`, `pop_back`, `pop_front`
- Insert or delete at index:
  - O(n)
  - `insert(iterator, k)`, `erase(iterator)`


## Associate Containers

### 1. Set
- Set is consisted with Red-Black tree structure (Balanced Binary Search Tree).
- Set doesn't have meaning for its element sequence.
- Set is sorted automatically when element is inserted.
- Set doesn't allow duplicated Key. It contains 1 value per Key. Key is unique for  a set.
- Since Set is using Red-Black tree structure, its time complexity is same with Red-Black tree. Plus that, it gurantees the search, insert and delete time complexity to O(log(n)).
- +) From C+11, unorded_set is available to use which is unordered set. It is consisted with Hash table structure.
- Random Access:
  - Not Available
- Search:
  - O(log(n))
  - `find`
- Insert or delete element
  - O(log(n))
  - `insert`, `erase`

### 2.map
- Map is also consisted with Red-Black tree structure as same with the Set.
- Map is consisted with Key and Value, and and they are saved as pair object.
- Since Map is also using Red-Black tree structure, its time complexity is same with the Set.
- Random Access:
  - Not Available
- Search:
  - O(log(n))
  - `find`
- Insert or delete element
  - O(log(n))
  - `insert`, `erase`

### FYI) Difference between Map and Set
- Map is consisted with `pair<key, value>` object and it is sorted by key
- Set is sorted by key but it does not have specific value
