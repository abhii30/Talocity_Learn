# Memory Leak

## 3 Tools to find memory leak

1.  Chrome task manager
2.  memory panel
3.  performance panel

## Leak 1 - Too many DOM nodes

## Leak 2 - Detached DOM nodes

# Memory Panel

## Heap memory

- ### Shallow size The actual size of a thing
- ### Retained size - memory that can be freed if the thing is deleted

## Allocation memory

- ### Memory allocated over a period of time

## Allocation Sampling

<br>

- ### **Memory in Performance tab** - the graph should all go back down unless there is no garbage collection
- ### When rendering many things then it should atleast go up and then flat (not continuous climbing)
