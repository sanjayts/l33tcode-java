# LRU Cache

https://leetcode.com/problems/lru-cache/

There are at the very least three ways to solve this:

1. The simplest one would be to wrap the `LinkedHashMap` class and override the `removeEldestEntry` method to purge entries which are least accessed. https://stackoverflow.com/a/6400874/193906
2. The second simplest way is to use a combination of `HashMap` and `LinkedList` classes to keep track of key accesses and move them around in the doubly-linked list to ensure the tail always has the least accessed item. https://www.geeksforgeeks.org/lru-cache-implementation/
3. The most optimal solution would be to maintain your own doubly-linked list in such a way that you can get `O(1)` access to a specific node. More details at https://leetcode.com/problems/lru-cache/discuss/1046049/Clean-O(1)-solution-using-dummy-headtail-pointer-no-null-checking!!!
