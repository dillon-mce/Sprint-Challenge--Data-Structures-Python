Add your answers to the questions below.

1. What is the runtime complexity of your ring buffer's `append` method?

**O(1)** It will always take the same four steps.

2. What is the space complexity of your ring buffer's `append` function?

**O(Capacity)** Technically it is O(capacity + 3). It will always use as much space as the capacity is set to, plus three helper variables.

3. What is the runtime complexity of your ring buffer's `get` method?

**O(1)** Once the buffer is full. Before the buffer is full, it takes **O(k)**, where k is the number of elements in the buffer, to get the slice.

4. What is the space complexity of your ring buffer's `get` method?

**O(Capacity-1)** Before the buffer is full, it returns a copy of the list, so needs as much space as that copy will take. After the buffer is full, it just returns the list, so it uses no extra space.

5. What is the runtime complexity of the provided code in `names.py`?

**O(n^2)** Or I guess it is actually **O(n1 * n2)** where n1 is the length of the first list and n2 is the length of the second.

6. What is the space complexity of the provided code in `names.py`?

**O(2n)), simplifies to O(n)** Where n is the total number of names in both lists. If they are all duplicates you will end up with a group of two lists that have all the names and a separate list that also has all the names.

7. What is the runtime complexity of your optimized code in `names.py`?

**O(min(n1, n2))** As far as I can tell, the intersection of two sets takes **O(n)** where n is the smaller of the two sets. The code runs in about 0.0035 seconds on my computer, compared to 6.5 seconds for the version that was given to us.

8. What is the space complexity of your optimized code in `names.py`?
**O(2n)), simplifies to O(n)**  Same as the space complexity of the code tht was given to us. Only held in sets, not lists.
