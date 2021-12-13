# Solution
```
# The key is to subtract the intersection from the union

# ie. 
    
a = set([1, 2, 3])

b = set([2, 4, 5])

c = set([3, 2, 6])

d = (a | b | c) - (a & b & c)
print(d)

#output = {1, 3, 4, 5, 6}
```
