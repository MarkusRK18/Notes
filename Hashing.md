## Linear Probing Hashing Method

```python
class HashTable:
	def __init__(self,size):
		self.size = size
		self.table = [None] * size
	def insert(self,key):
		idx = key % self.size
		org_idx = key
		
		while self.table[idx] is not None:
			if idx == org_idx:
				return False
		self.table[idx] = key
		return True
	def print_res(self):
		for i in range(self.size):
			if self.table[i] is not None:
				print(f"index {i} value = {self.table[i]}")
n = int(input())
arr = list(map(int,input().split()))
hash_table = HashTable(n)
for num in arr:
	hash_table.insert(num)
hash_table.print_res()
```

