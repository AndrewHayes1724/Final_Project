# The Set
## I. What is a set?
A set is an unordered collection of unique elements. In python sets are written with curly braces '{}'. 

Basically any time we need to store multiple items in a single variable a set can be used. The nuance of a set however is that it is unordered, and unindexed. Meaning we cannot loop through a set like we could with an array.

Example Image of Set
![here is an example image](https://www.w3resource.com/w3r_images/python-sets-image-exercise-15.svg)

We can see in this image that the numbers in this set are not indexed. But we are able to get a length of the set itself. 

### a. An example of a set in real life
An example of a set in real life would be like a dresser full of clothes. Or more specifically, one drawer. One drawer, or Set, has only shirts, no particular order and its not like each shirt is indexed with a number on it. It just has your shirt. So anytime you need a shirt, you can go get one from that drawer. 

## Unions and Intersections
The union and intersection of sets is a common reason why sets are implemented in python and other programming languages. Your problem later on will be based on these. 

### a. Union
A union of 2 sets is when we take the contents of one set, and combine it with the contents of another set, creating a final set with all of the contents with no duplicate values. 

So for example if we were given a set with {1,2} and another set with {2,3} then the union of these 2 sets would yield us a set with {1,2,3}. 

We could create an implementation where the duplicate value would be stored but for this example and for the sake of learning how unions are most traditionally implemented we will delete the duplicate value.

### b. Intersection
An intersection of 2 sets is when we take the contents of 2 sets and yield only the contents that are present in **both** sets. For example if we are given 2 sets with {1,2} and {2,3} like the previous example, then the output of the intersection would yield us a set with just the number 2, {2}. This is because only the number 2 is present in both sets.

### c. Difference
The difference of 2 sets is taking the contents of 2 sets that are not in either set. For example if we had the 2 sets A = {1,2} and B = {2,3} once again, the difference of A - B would be {1}. Where as the difference of B - A would be {3} This is useful if we need to compare 2 sets. This may be useful later on.

## II. Implementing a Set in python.
In python as stated before a set has curly braces {}. A union in python uses the " | | operator and the intersection uses the " & " operator. 

Example code can be found below:

```
# sets A and B
A = {0, 2, 4, 6, 8};
B = {1, 2, 3, 4, 5};
  
# union
print("Union :", A | B)
# Output = ('Union :', set([0, 1, 2, 3, 4, 5, 6, 8]))

# intersection
print("Intersection :", A & B)
# Output = ('Intersection :', set([2, 4]))

# difference
print("Difference :", A - B)
# Output = ('Difference :', set([8, 0, 6]))
```
From this example we are able to complete the union, the intersection and the difference of these 2 sets. 

## III. Example Problem

- Take 3 lists and find all common elements using Sets
- Output will be [80, 20]

```

# This program will take 3 lists and find all the common elements
# using Sets
  
def IntersecOfSets(arr1, arr2, arr3):
    # Converting the arrays into sets
    s1 = set(arr1)
    s2 = set(arr2)
    s3 = set(arr3)
      
    # Calculates intersection of 
    # sets on s1 and s2
    set1 = s1.intersection(s2)         #[80, 20, 100]
      
    # Calculates intersection of sets
    # on set1 and s3
    result_set = set1.intersection(s3)
      
    # Converts resulting set to list
    final_list = list(result_set)
    print(final_list)
  
# Driver Code
if __name__ == '__main__' :
      
    # Elements in Array1
    arr1 = [1, 5, 10, 20, 40, 80, 100]
      
    # Elements in Array2
    arr2 = [6, 7, 20, 80, 100]
      
    # Elements in Array3
    arr3 = [3, 4, 15, 20, 30, 70, 80, 120]
      
    # Calling Function
    IntersecOfSets(arr1, arr2, arr3)
```

In this example problem we see that the Set is used to solve a problem with lists. Typically this will be the use of sets, and not the actual storage of information long term. Sets are most commonly used as a means to perform common math like operations on collection such is a list in this case.

## IV. Problem to Solve

This program will be taking 3 sets, and finding the difference between all 3.
```
For example if 
a = {1,2,3}
b = {2,4,5}
c = {3,2,6}

d = functionthatdoesstuff(a,b,c)

print(d)

output = {1,3,4,5,6}

```

[Link to Solution](setsolution.md)

## [Return to Welcome Page here](welcome.md)