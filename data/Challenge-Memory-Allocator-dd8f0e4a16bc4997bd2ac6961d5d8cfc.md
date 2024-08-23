## ⭐ Goal

In this challenge, you will create a custom memory allocator. A memory allocator is a tool that helps manage memory in a computer program. Think of it as a system that decides where and how much memory your program should use when it needs to store data.

Your goal is to build a simple memory management system that does the following:

- **Allocate Memory**: Give out a chunk of memory when a part of your program asks for it.
- **Deallocate Memory**: Free up the memory when it is no longer needed.
- **Reallocate Memory**: Change the size of the memory chunk if needed.

This is similar to how `malloc()`, `free()`, and `realloc()` work in C programming, but you will create your own versions of these functions.

## 🚨 Requirements

1. Implement the following functions:
    - `void* allocate(size_t size)`
    - `void deallocate(void* ptr)`
    - `void* reallocate(void* ptr, size_t new_size)`
2. Your allocator should manage a predefined chunk of memory (e.g., 1MB)
3. Handle memory alignment properly
4. Implement a strategy to minimize fragmentation.

## 💼 Usage

```c
void* ptr1 = allocate(100);  // Allocate 100 bytes
void* ptr2 = allocate(200);  // Allocate 200 bytes
deallocate(ptr1);            // Free the first allocation
ptr1 = reallocate(ptr2, 300);
```

## 🧪 Testing

- **Different Sizes**: Test by allocating and freeing memory blocks of various sizes.
- **Memory Leaks**: Check if your program properly frees memory and doesn’t waste it.
- **Performance**: Compare how your allocator performs against standard library functions.

## 🍥 Bonus

- **Allocation Strategies**: Implement different ways to allocate memory, like first-fit (finding the first available block) or best-fit (finding the smallest suitable block).
- **Debugging Features**: Add features to track memory usage and find potential issues.
- **Ensure thread-safety**
