---
title: "Useful Data Structures in Python"
tags: Python
date: 2021-06-30 23:57:28 -0400
categories: blogging
---

# Useful Data Structures in Python collections module

## 1. OrderedDict
- As you could guess from its name, it is very similar with Dictionary. But it stores the inserted order of the items.
- Since it stores inserted order, it is generally used when programmer needs sorted dictionary
- Documentaion link: [OrederedDict in Python3.8](https://docs.python.org/3.8/library/collections.html#collections.OrderedDict)


## 2. namedtuple
- As you could guess from its name, it is `named` tuple, that can acess value with `key`, differently with default Tuple.
- `namedtuple` is specially designed to make your code more Pythonic when you’re working with tuples
- you can create immutable sequence types that allow you to access their values using descriptive field names and the dot notation instead of unclear integer indices.
- Documentation link: [namedtuple in Python3.8](https://docs.python.org/3.8/library/collections.html#collections.namedtuple)

## 3. Deque
- Deque is short for 'double-ended-queue'
- Deques are a generalization of stacks and queues
- Though list objects support similar operations, they are optimized for fast fixed-length operations and incur O(n) memory movement costs for pop(0) and insert(0, v) operations which change both the size and position of the underlying data representation.
- If maxlen is not specified or is None, deques may grow to an arbitrary length. Otherwise, the deque is bounded to the specified maximum length. Once a bounded length deque is full, when new items are added, a corresponding number of items are discarded from the opposite end. Bounded length deques provide functionality similar to the tail filter in Unix. They are also useful for tracking transactions and other pools of data where only the most recent activity is of interest.
- Documentation link: [Deque in Python3.8](https://docs.python.org/3.8/library/collections.html#collections.deque)

## 4. Counter
- A Counter is a dict subclass for counting hashable objects.
- Documenetation link [Counter in Python3.8](https://docs.python.org/3.8/library/collections.html#collections.Counter)

## 5. defaultdict
- Returns a new dictionary-like object. defaultdict is a subclass of the built-in dict class. 
- It overrides one method and adds one writable instance variable. The remaining functionality is the same as for the dict class and is not documented here.

## 6. ChainMap
- Updated from Python3.3
- ToBeUpdated...

