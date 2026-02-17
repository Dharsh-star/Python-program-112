# Python-program-112
EXERCISE BY IMPLEMENTING SINGLY LINKED LIST AND HASH TABLE
class Node:def __init__(self, key, val, next=None):
self.key, self.val, self.next = key, val, nextclas HashTable:
def __init__(self, size):
self.size = sizeself.table = [None] * sizedef put(self, k, v):idx = hash(k) % self.sizeself.table[idx] = Node(k, v, self.table[idx])
def get(self, k):curr = self.table[hash(k) % self.size]while curr:if curr.key == k: return curr.valcurr = curr.nextreturn Noneht = HashTable(5)ht.put("ID_1", "Alice")print(ht.get("ID_1"))

Output:Alice
