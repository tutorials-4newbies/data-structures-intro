class: center, middle

# Data Structures intro - 1
## In python

[live presentation](https://alonisser.github.io/data-structures-intro/#1) <br/>
[twitter](alonisser@twitter.com), [medium](https://medium.com/@alonisser/)

---

# What is a data structure

"A data structure is a particular way of organizing data in a computer so that it can be used effectively."

---

# List

A python **list** is a mutable, ordered sequence of items. As such, it can be indexed, sliced, and changed.
 Each element can be accessed using its position in the list. Each element or value that is inside of a list is called an **item**


---

# List

A python <span class='marker'>**list**</span> is a <span class='marker'>mutable</span>, <span class='marker'>ordered sequence</span> of items. As such, it can be indexed, sliced, and changed. 
Each element can be accessed using its <span class='marker'>position</span> in the list. Each element or value that is inside of a list is called an **item**


---
# Creating a list

```python
#with the list literal []
my_list = [74,75]

```

---
# Lists usage

```python
names = ['yoni', 'menashe', 'marxus']
stuff = [1, 4, 2, 'Dorong']
nested = [['ori','amit.y','palgi'],['amit.m','omer.s','yoni.y']]
things = [{'name':'alon', 'age':45}]
empty = []
```

---
# Using lists

```python
names = ['yoni', 'menashe', 'marxus']
names.append('alon')
print(names)
['yoni', 'menashe', 'marxus', 'alon']
len(names)
4
names[0]
'yoni'

names.append('alon')
len(names)
5
naems.count('alon')
2

```
--

```python
nums = [0,1, 5, 3, 7]
nums.sort()
print(nums)
nums.reverse()
print(nums)
bool(nums) == True
bool([]) == False
```
---
# Slicing and accessing by position
```python
names[0:1]
['yoni']
names[0:2]
['yoni', 'menashe']
```

---
# A dictionary

is a mutable, unordered set of key-value pairs where each key must be unique. To access a given element, we must refer to it by using its key,

---

# A dictionary

is a <span class='marker'>mutable</span>, <span class='marker'>unordered</span> set of <span class='marker'>key-value</span> pairs where each key must be <span class='marker'>unique</span>. To access a given element, 
we must refer to it by using its key,

---
# Creating a Dict

```python
#with the dict literal {}
my_dict = {"name":"alon","answer":42}
# Is the same as using the dict constructor
another_dict = dict(name='alon',answer=42)

```

---

# Using dictionaries

```python
person = {'name':'alon','age':45, 'is_here':True}
print(person)
person['name']
'alon'
len(person)
3
person.keys()
['name', 'age', 'is_here']
person.values(['alon', 45, True])
person['name'] = 'nisser'
person['nicknames'] = ['karpada']
print(person)
{'name': 'nisser', 'age': 45, 'is_here': True, 'nicknames': ['karpada']}

```
--
We can also update a dict (mutate it) with another dict
```python
jesse = {'username': 'JOctopus', 'online': False, 'points': 723}

jesse.update({'followers': 481})

print(jesse)
{'followers': 481, 'username': 'JOctopus', 'points': 723, 'online': False}

```
---

# Breaking dictionaries

How can we break a dictionary?

--
Missing keys
```python
person =  {'name':'alon','age':45, 'is_here':True}
person['surname']
# we'll get a KeyError
# Instead:
person.get('surname')
```
--
Mutable keys
```python
person =  {'name':'alon',[1,2]:'nisser'}
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: unhashable type: 'list'

```
Where does the unhashable come from?

---
# Peeking behind the curtain
[A hashing function](https://en.wikipedia.org/wiki/Hash_function) maps data to a consistent value

See [live example](https://passwordsgenerator.net/md5-hash-generator/) with the popular md5 hash

* Note: Hashing != cryptographic or secure
* Hashing != unique values

---
class: center, middle

# Let's play

---
# List comprehensions and iterations
Usually we need to iterate on lists
```python
names = ['alon','omer','alon','amit']

for item in names:
    print(item)

```
We can also filter lists
```python
nums = [0,1,2,3,4,5,6,7,8,9]
even_nums = [x for x in nums if x % 2 == 0]
print(even_nums)
[0, 2, 4, 6, 8]
```
We can also mutate the list this way
```python
nums = [0,1,2,3,4,5,6,7,8,9]
def square(num):
    return num * num
square_nums = [square(x) for x in nums]
print(square_nums)
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
# This also works
square_nums = [x*x for x in nums if x % 2 == 0]
print(square_nums)
[0, 4, 16, 36, 64]
```

---
# Dict comprehensions and iterations

```python
person = dict(name="alon", age=45)
for key, value in person.items():
    print(key, value)

```

For the reader - learn about filtering and mapping dict comprehensions
---
# Read some more

* [Beginners - how to code in python](https://www.digitalocean.com/community/books/digitalocean-ebook-how-to-code-in-python) 
* [Read more about lists](https://www.geeksforgeeks.org/python-list/)
* [Read more about dicts](https://www.geeksforgeeks.org/python-dictionary/)
* [Python docs data structures tutorial](https://docs.python.org/3/tutorial/datastructures.html)
---

# Homework

* [Do this tutorial](https://www.digitalocean.com/community/tutorials/how-to-make-a-simple-calculator-program-in-python-3)
* Read some more (see a previous slide)
* Write a python program that gets a value (n) between 2-4 from the user and 
prints the "n"elements from a predefined array  
---
#Open source rocks!

---

class: center, middle

#Thanks for listening!

---
