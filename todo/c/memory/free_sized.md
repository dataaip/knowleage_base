# free_sized

From cppreference.com
< c‎ | memory
 C

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Language | | | | |
| Headers | | | | |
| Type support | | | | |
| Program utilities | | | | |
| Variadic function support | | | | |
| Error handling | | | | |
| Dynamic memory management | | | | |
| Strings library | | | | |
| Algorithms | | | | |
| Numerics | | | | |
| Date and time utilities | | | | |
| Input/output support | | | | |
| Localization support | | | | |
| Concurrency support (C11) | | | | |
| Technical Specifications | | | | |
| Symbol index | | | | |

 Dynamic memory management

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| malloc | | | | |
| calloc | | | | |
| realloc | | | | |
| free | | | | |
| ****free_sized****(C23) | | | | |
| free_aligned_sized(C23) | | | | |
| aligned_alloc(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdlib.h>` |  |  |
| void free_sized( void\* ptr, size_t size ); |  | (since C23) |
|  |  |  |

Deallocates the space previously allocated by malloc(), calloc(), or realloc() (but not aligned_alloc()).

|  |  |
| --- | --- |
|  | This section is incomplete Reason: share wording among `free_\*` family |

`free_sized` is thread-safe: it behaves as though only accessing the memory locations visible through its argument, and not any static storage.

A call to `free_sized` that deallocates a region of memory **synchronizes-with** a call to any subsequent allocation function that allocates the same or a part of the same region of memory. This synchronization occurs after any access to the memory by the deallocating function and before any access to the memory by the allocation function. There is a single total order of all allocation and deallocation functions operating on each particular region of memory.

### Parameters

|  |  |  |
| --- | --- | --- |
| ptr | - | pointer to the memory to deallocate |
| size | - | size of memory previously passed to an allocation function |

### Return value

(none)

### Notes

|  |  |
| --- | --- |
|  | This section is incomplete |

### Possible implementation

```
void free_sized(void* ptr, size_t /*size*/)
{
    free(ptr);
}

```

### Example

Run this code

```
#include <stddef.h>
#include <stdio.h>
#include <stdlib.h>
 
typedef struct
{
    size_t size;     // current number of elements
    size_t capacity; // reserved number of elements
    void** data;
} PtrVector;
 
PtrVector vector_create(size_t initial_capacity)
{
    PtrVector ret =
    {
        .capacity = initial_capacity,
        .data = (void**) malloc(initial_capacity * sizeof(void*))
    };
    return ret;
}
 
void vector_delete(PtrVector* self)
{
    free_sized(self->data, self->capacity * sizeof(void*));
}
 
void vector_push_back(PtrVector* self, void* value)
{
    if (self->size == self->capacity)
    {
        self->capacity *= 2;
        self->data = (void**) realloc(self->data, self->capacity * sizeof(void*));
    }
    self->data[self->size++] = value;
}
 
int main()
{
    int data = 42;
    float pi = 3.141592f;
    PtrVector v = vector_create(8);
    vector_push_back(&v, &data);
    vector_push_back(&v, &pi);
    printf("data[0] = %i\n", *(int*)v.data[0]);
    printf("data[1] = %f\n", *(float*)v.data[1]);
    vector_delete(&v);
}

```

Output:

```
data[0] = 42
data[1] = 3.141592

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.24.3.4 The free_sized function (p: 365-366)

### See also

|  |  |
| --- | --- |
| free | deallocates previously allocated memory   (function) |
| free_aligned_sized(C23) | deallocates previously allocated sized and aligned memory   (function) |
| malloc | allocates memory   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/memory/free_sized&oldid=175229>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 August 2024, at 19:51.