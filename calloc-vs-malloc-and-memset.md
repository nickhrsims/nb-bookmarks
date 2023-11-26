# `calloc` vs `malloc` and `memset`

## Summary

The short version: Always use calloc() instead of malloc()+memset(). In most cases, they will be the same. In some cases, calloc() will do less work because it can skip memset() entirely. In other cases, calloc() can even cheat and not allocate any memory! However, malloc()+memset() will always do the full amount of work.

Understanding this requires a short tour of the memory system.

## More Reading

For a more in-depth explanaition:

https://stackoverflow.com/a/2688522
