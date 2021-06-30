---
title: "Common Data Structures in Python"
tags: Python
date: 2020-06-30 23:57:28 -0400
categories: python
---

# Default Data Structures in Python

## 1. List
- The `List` data type has some more methods. Here are all of the methods of list objects.
- Sequenced structure like array in other languages.
- Official description: [List in python3.8 Doc](https://docs.python.org/3.8/tutorial/datastructures.html#more-on-lists).


## 2. Tuple
- `Tuple` is very similar with List, but it is <b>immutable</b>
- Tuple supports indexing, slicing and other common sequence operations, but doesn't support other built-in methods. (Disable to use append, remove, ...).
- Advantages of Tuple
  - The Implications of iterations are much faster in tuples.
  - Consumes less memory then List.
- Disadvantages of Tuple
  - Operations like insertion and deletion are better performed in List
  - List can utilize lots of built-in methods, though Tuple doesn't have.
- Official description: [Tuple in python3.8 Doc](https://docs.python.org/3.8/tutorial/datastructures.html#tuples-and-sequences)

## 3. Dictionary
- `Dictionary` is a data structure with 'key-value' concept design.
- Dictionaries are sometimes found in other languages as “associative memories” or “associative arrays”.
- The keys are unique within one dictionary.
- The key values can be `string`, `int`, and `float`
- Official description: [Dictionary in python3.8 Doc](https://docs.python.org/3.8/tutorial/datastructures.html#dictionaries)