# Pagination Project

## Curriculum

This project focuses on implementing pagination for datasets, including considerations for different types of pagination and ensuring the system is resilient to deletions.

### Short Specializations

- **Average Completion Rate**: 134.78%

### Project Timeline

- **Start Date**: Jul 18, 2024, 6:00 AM
- **End Date**: Jul 23, 2024, 6:00 AM
- **Checker Release Date**: Jul 19, 2024, 12:00 PM
- **Auto Review Launch**: At project deadline

## Learning Objectives

By the end of this project, you should be able to:

1. **Simple Pagination**: Explain how to paginate a dataset with `page` and `page_size` parameters.
2. **Hypermedia Metadata**: Explain how to paginate a dataset with hypermedia metadata.
3. **Deletion-Resilience**: Explain how to paginate in a deletion-resilient manner.

## Requirements

- Your files must be interpreted/compiled on **Ubuntu 18.04 LTS** using `python3` (version 3.7).
- All files should end with a new line.
- The first line of all files should be exactly `#!/usr/bin/env python3`.
- A `README.md` file at the root of the project folder is mandatory.
- Your code should adhere to the `pycodestyle` style (version 2.5.*).
- File length will be tested using `wc`.
- All modules must have documentation (`python3 -c 'print(__import__("my_module").__doc__)'`).
- All functions must have documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)'`).
- Documentation should be a real sentence explaining the purpose of the module, class, or method.
- All functions and coroutines must be type-annotated.

## Setup

The dataset for this project is provided in `Popular_Baby_Names.csv`. This file contains data about popular baby names and is used throughout the project to test pagination functionalities.

## Tasks

### 0. Simple Helper Function

**Objective**: Write a function named `index_range` to return a tuple of size two containing the start and end index for pagination.

**File**: `0-simple_helper_function.py`

**Example Usage**:
```python
index_range = __import__('0-simple_helper_function').index_range
print(index_range(1, 7))   # Output: (0, 7)
print(index_range(3, 15))  # Output: (30, 45)
```

### 1. Simple Pagination

**Objective**: Implement the `Server` class with a `get_page` method to paginate a dataset using the `index_range` function.

**File**: `1-simple_pagination.py`

**Example Usage**:
```python
Server = __import__('1-simple_pagination').Server
server = Server()

print(server.get_page(1, 3))   # Returns the first 3 items
print(server.get_page(3, 2))   # Returns items from index 2 to 3
print(server.get_page(3000, 100))  # Returns an empty list if out of range
```

### 2. Hypermedia Pagination

**Objective**: Implement the `get_hyper` method in the `Server` class to return a dictionary with pagination metadata.

**File**: `2-hypermedia_pagination.py`

**Example Usage**:
```python
Server = __import__('2-hypermedia_pagination').Server
server = Server()

print(server.get_hyper(1, 2))
print(server.get_hyper(2, 2))
print(server.get_hyper(100, 3))
```

### 3. Deletion-Resilient Hypermedia Pagination

**Objective**: Implement the `get_hyper_index` method in the `Server` class to handle pagination even if rows are deleted from the dataset.

**File**: `3-hypermedia_del_pagination.py`

**Example Usage**:
```python
Server = __import__('3-hypermedia_del_pagination').Server
server = Server()

server.indexed_dataset()

print(server.get_hyper_index(3, 2))  # Returns the current page of items
print(server.get_hyper_index(10, 10))  # Handles deletion-resilient pagination
```

## Notes

- Ensure that all your code is type-annotated and follows the provided coding standards.
- Test your implementations thoroughly to ensure correctness and resilience.