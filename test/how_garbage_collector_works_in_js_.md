### How Garbage Collector works in JS?

- In JS garbage collector automatically frees up memory that is no longer being used by the program
- There are different algorithms for garbage collectors, but **Mark and Sweep** is the most popular
  - Mark: GC marks all objects that are still being used in App. It's starts with root objects which are usually global. The GC then traverses the object graph, marking all objects that are reacheble from the root objects.
  - Sweep: After all live objects are marked, the GC sweeps throuth the memory and frees up all the objects that are not marked as live
  - Compact: Move all the live objects together to create blocks of memory, which can help improve perfomance

Tips to avoid memory leaks:

- Avoid global variables
- Minimise usage of closures