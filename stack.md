# The Stack
## I. What is a stack?

A stack is a linear data structure which follows a specific order when operations are implemented

This specific order is that the last in is the first out, or the first in is the last out. So there is only one "exit point". 

![here is an example image](https://media.geeksforgeeks.org/wp-content/cdn-uploads/gq/2013/03/stack.png)

This image is from [Geeksforgeeks.com](https://www.geeksforgeeks.org/stack-in-python/)

In this image we can see that the insert function is typically implemented as .push, and the delete function is implemented as .pop in python which is our focus in this tutorial.

An example of a stack in real life would be like a box of tissues. The **first** tissue that will be taken from the box and used, was likely the **last** tissue to be added to the box. This example of a stack would follow the **First in Last out** order of a stack.

## II. Implementing a stack in python
Here is a pseudocode-esque example of how a stack works in python by using the list '[]'

```
stack = []          # create an empty stack
stack.append(‘a’)   # push 'a' to the stack
stack.append(‘b’)   # push 'b' to the stack
stack.append(‘c’)   # push 'c' to the stack
print(stack)
['a', 'b', 'c']
stack.pop()         #pop the last element
'c'
stack.pop()        #pop the last element
'b'
stack.pop()        #pop the last element
'a'
stack              #check the remaining stack
[]
```
From this example we are able to complete 3 operations. And using the stack.pop() function we can keep track of our 'history' so-to-speak. 

We can also see that the stack.append() function is used instead of stack.push(). This is because stack.append() lets us add to the top of the stack while the .push() would just add the element to the end of the stack. 
For this reason we will focus on stack.append() only.

**Note**: The stack.pop() function **removes** the item from the stack.

## III. Example Problem
In this example problem I will demonstrate how to reverse a string using a stack. 

- Take an input 'cats' 
- Output will be 'stac' 

```
def reverse(string)
    # checks if stack is empty
    if stack.empty:
        pass
    else
        n = len(stack)
        # This loop pushes all characters of string to the stack. 
        # So the first letter of the string, 'c' was added to the stack first. 
        # and the letter 's' was added last, putting it at the top of the stack and will be removed first.
        for i in range(0,n):
            stack.append(string[i])
        # empty the string now so we can create a new string and return it. 
        string = ''

        # This loop takes the letters in the stack and now adds it to the string
        # creating a reversed order string from the original input
        for i in range(0,n):
            string[i] += stack.pop
        return string


            

string = "cats"

string = reverse(string)
print(string)
# output = 'stac'
```

## IV. Problem to Solve

The problem we will be solving is taking a string, and if any duplicate letters are next to/adjacent to eachother, to simply remove one of the duplicate letters. 

Example:
```
string = 'aabcddc'
print(removeDuplicates(string))
# Output will be just 'abcdc'
```  

There will be 2 inputs in this problem

- aabcddc (output == abcdc)
- aaabcdccd (output == abcdcd)

The second output has a set of 3 duplicates, so we can't just remove one, but 2 of the letters.
Thus we need to create a program that can dynamically check for the resulting string and then call itself to remove remaining duplicates. Or we can just account for as many duplicates as we want, but the doing so without recursion will slow down run time with larger strings.

**Hint:** *recursive functions may be used, but possible without*

[Link to Solution](stacksolution.md)


## [Link Back to Welcome Page](Welcome.md)