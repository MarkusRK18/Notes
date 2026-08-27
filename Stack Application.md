### Implements the stack using a linked list

Operation of Push, Pop, Peek,  Exit


```python
class Node:
	def __init__(self,data):
		self.data = data
		self.next = None
class Stack:
	def __init__(self,max_size):
		self.top = None
		self.max_size = max_size
		self.current_size = 0
	def is_empty(self):
		return self.top is None
	def is_full(self):
		return self.current_size >= self.max_size
	def push(self,data):
		if self.is_full():
			print("Stack overflow")
			return
		new_node = Node(data)
		new_node.next = self.top
		self.top = new_node
		self.current_size += 1
		print(f"PUSH {data} SUCCESSFUL")
	def pop(self):
		if self.is_empty():
			print("Stack underflow")
		pop_data = self.top.data
		self.top = self.top.next
		self.current_size -= 1
		print(f"POP {pop_data}")
	def peek(self):
		if self.is_empty():
			print("STACK EMPTY")
			return
		print(self.top.data)
def main():
	try:
		max_size = int(input())
		stack = Stack(max_size)
		
		while True:
			user_input = input().split()
			if not user_input:
				continue
			choice = int(user_input[0])
			if choice == 1:
				val = int(user_input[1])
				stack.push(val)
			elif choice == 2:
				stack.pop()
			elif choice == 3:
				stack.peek()
			elif choice == 4:
				break
	except (IOError, IndexError, valueError):
		pass
if __name__ == "__main__":
	main()
```

## String Containing 

```python

```

