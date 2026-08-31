## Selection sorting

```python 

n = int(input())

arr = list(map(int,input().split()))

for i in range(n):
	mid = i
	
	for j in range(i+1,n):
		if arr[j] < arr[mid]:
			mid = j
	arr[i], arr[mid] = arr[mid], arr[1]
	print(*arr)
```



## Insertion Sorting

```python

n = int(input())
arr = list(map(int,input().split())

for i in range(n):
	key = arr[i]
	j = j - 1
	while j >= 0  and key < arr[j]:
		arr[j+1] = key
		j = j-1
	arr[j+1] = key
	print(*arr)

```


## Bubble Sorting

```python
n = int(input())
arr = list(map(int,input().split()))

for i in range(n):
	for j in range(n-1):
		if arr[j] > arr[j+1]:
			arr[j],arr[j+1] = arr[j+1],arr[j]
	print(*arr)	
```
