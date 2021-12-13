# Stack Solution
### Here is an implementation of the problem to remove all adjacent duplicates.

```
def removeDupes(string) 
    list = []
    for i in string
        if list and i == list[-1]
            list.pop
        else
            list.append(i)
    return "".join(list)


string = 'aabcddc'
string = removeDupes(string)
print(string)
# Output = 'abcdc'
```