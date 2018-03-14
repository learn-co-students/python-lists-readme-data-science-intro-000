
# Introduction to lists

So far we have worked with individual pieces of data like the string `hello`, then with variables we saw how to give this data a name with variables.  Well in this lesson, we'll see how we can group data together with lists.  

### Creating a list 

A list is our first form of a collection.  A collection is just a way of grouping data together, and lists certainly accomplish this.  For example, let's consider the top cities to travel to according to Travel and Leisure.  We'll see it below, but we must stay focused on Python and data! 

#### Travel Locations
1. Solta
2. Greenville
3. Buenos Aires
4. Los Cabos
5. Walla Walla Valley
6. Marakesh
7. Albuquerque
8. Archipelago Sea
9. Iguazu Falls
10. Salina Island
11. Toronto
12. Pyeongchang

Ok, and this is how we express this in Python.


```python
['Solta', 'Greenville', 'Buenos Aires', 'Los Cabos', 'Walla Walla Valley', 'Marakesh', 'Albuquerque', 'Archipelago Sea', 'Iguazu Falls', 'Salina Island', 'Toronto', 'Pyeongchang']
```




    ['Solta',
     'Greenville',
     'Buenos Aires',
     'Los Cabos',
     'Walla Walla Valley',
     'Marakesh',
     'Albuquerque',
     'Archipelago Sea',
     'Iguazu Falls',
     'Salina Island',
     'Toronto',
     'Pyeongchang']



So we indicate that we are initializing a `list` by placing a bracket, `[` (located above of the return key), and end the list with a closing bracket `']'`.  To separate each item in the list, called an element, we place a comma.


```python
['Croatia', 'USA', 'Argentina', 'Mexico', 'USA', 'Morocco', 'New Mexico', 'Finland', 'Argentina', 'Italy', 'Canada', 'South Korea']
```




    ['Croatia',
     'USA',
     'Argentina',
     'Mexico',
     'USA',
     'Morocco',
     'New Mexico',
     'Finland',
     'Argentina',
     'Italy',
     'Canada',
     'South Korea']



And of course, we can set each list equal to variable so that we can name each list.


```python
top_travel_cities = ['Solta', 'Greenville', 'Buenos Aires', 'Los Cabos', 'Walla Walla Valley', 'Marakesh', 'Albuquerque', 'Archipelago Sea', 'Iguazu Falls', 'Salina Island', 'Toronto', 'Pyeongchang']
```


```python
top_travel_cities
```




    ['Solta',
     'Greenville',
     'Buenos Aires',
     'Los Cabos',
     'Walla Walla Valley',
     'Marakesh',
     'Albuquerque',
     'Archipelago Sea',
     'Iguazu Falls',
     'Salina Island',
     'Toronto',
     'Pyeongchang']




```python
countries_of_top_cities = ['Croatia', 'USA', 'Argentina', 'Mexico', 'USA', 'Morocco', 'New Mexico', 'Finland', 'Argentina', 'Italy', 'Canada', 'South Korea']
```

### Accessing Elements of Lists

Now our `top_travel_cities` list is contains multiple elements.  And just like we numbered the elements of a list with text:

1. Solta
2. Greenville
3. Buenos Aires

A list in Python also assigns a number to each element.


```python
top_travel_cities
```




    ['Solta',
     'Greenville',
     'Buenos Aires',
     'Los Cabos',
     'Walla Walla Valley',
     'Marakesh',
     'Albuquerque',
     'Archipelago Sea',
     'Iguazu Falls',
     'Salina Island',
     'Toronto',
     'Pyeongchang']




```python
top_travel_cities[0]
```




    'Solta'



In the above line we are referencing a list and then using the brackets to access specific elements of our list.  We access elements in a list with the `index`, and there is a separate index for each element in the list.  It begins at the number zero, increases for every element thereafter.

So to access the second element we write `top_travel_cities[1]`, and the third element is `top_travel_cities[2]`:


```python
top_travel_cities[2]
```




    'Buenos Aires'



How would we access the last element, well we could count all of the elements in the list, and `Pyeongchang` would just be one less than that.  Or we can ask Python to start from the back in move back one.


```python
top_travel_cities[-1]
```




    'Pyeongchang'



And we can move back as many as we want.


```python
top_travel_cities[-2]
```




    'Toronto'



Each element in our list is a string, so we can always set an element of our string equal to a variable.


```python
top_canadian_city = top_travel_cities[-2]
top_canadian_city
```




    'Toronto'




```python
type(top_canadian_city)
```




    str



So now we have a variable of `top_canadian_city`, equal to the string 'toronto', and a variable of `top_travel_cities` equal to the list of cities.  


```python
top_travel_cities
```




    ['Solta',
     'Greenville',
     'Buenos Aires',
     'Los Cabos',
     'Walla Walla Valley',
     'Marakesh',
     'Albuquerque',
     'Archipelago Sea',
     'Iguazu Falls',
     'Salina Island',
     'Toronto',
     'Pyeongchang']




```python
type(top_travel_cities)
```




    list



### Accessing Multiple Elements

Now imagine that we don't want to access just one element of a list, but multiple elements at once.  Python allows us to do that as well.


```python
top_travel_cities[0:2]
```




    ['Solta', 'Greenville']



Ok, now to access elements of a list, inside of our brackets we are placing two numbers separated by a colon.  The first number indicates the index of the first element we want returned.  

The second number could represent the number of elements we want returned back, or maybe it represents the stopping index of the elements that we are retrieving.  Looking at our `top_travel_cities` it could be either.


```python
top_travel_cities
```




    ['Solta',
     'Greenville',
     'Buenos Aires',
     'Los Cabos',
     'Walla Walla Valley',
     'Marakesh',
     'Albuquerque',
     'Archipelago Sea',
     'Iguazu Falls',
     'Salina Island',
     'Toronto',
     'Pyeongchang']



So let's try a different experiment to answer our question.


```python
top_travel_cities[4:5]
```




    ['Walla Walla Valley']



Ok, so that second number is not representing the number of elements we want returned.  Instead it must be used to indicate the index of the first element not selected.  


```python
top_travel_cities[4:6]
```




    ['Walla Walla Valley', 'Marakesh']



This operation is called the `slice`.  So we can say we are `slicing` the elements with indices 4 and 5 in the line above.  Note that even though we are `slicing` elements, our list remains in tact.


```python
top_travel_cities
```




    ['Solta',
     'Greenville',
     'Buenos Aires',
     'Los Cabos',
     'Walla Walla Valley',
     'Marakesh',
     'Albuquerque',
     'Archipelago Sea',
     'Iguazu Falls',
     'Salina Island',
     'Toronto',
     'Pyeongchang']



In programming terms, we would say that slicing elements is non-destructive, because it does not change the underlying data structure.  We can do it as many times as we like, and our `top_travel_cities` array remains unchanged.  If we wish to store that slice of elements, we can store it in another variable.


```python
top_two = top_travel_cities[0:2]
top_two
```




    ['Solta', 'Greenville']



So now we have another variable called `top_two` that points to an array which contains an array of elements equal to the first two elements of `top_travel_cities`.

### Changing elements with destructive methods

Now that we read and select certain elements from lists, let's work on changing these lists.  To add a new element to a list, we can use the `append` method.


```python
top_travel_cities.append('San Antonio')
```

Now let's take another look at `top_travel_cities`.


```python
top_travel_cities
```




    ['Solta',
     'Greenville',
     'Buenos Aires',
     'Los Cabos',
     'Walla Walla Valley',
     'Marakesh',
     'Albuquerque',
     'Archipelago Sea',
     'Iguazu Falls',
     'Salina Island',
     'Toronto',
     'Pyeongchang',
     'San Antonio']



You will see 'San Antonio' included in the list.  So note that unlike slice, `append` is destructive.  That is, it changes our underlying data structure.  Every time we execute the `append` method, another element is added to our list.   Now what if we accidentally add 'San Antonio' a second time to our list.


```python
top_travel_cities.append('San Antonio')
top_travel_cities
```




    ['Solta',
     'Greenville',
     'Buenos Aires',
     'Los Cabos',
     'Walla Walla Valley',
     'Marakesh',
     'Albuquerque',
     'Archipelago Sea',
     'Iguazu Falls',
     'Salina Island',
     'Toronto',
     'Pyeongchang',
     'San Antonio',
     'San Antonio']




```python
top_travel_cities.pop()
```




    'San Antonio'



Now if we want to change an element from the middle of the list, we can access and then reassign that element.  So for example, let's change 'Walla Walla Valley' to the number 4.


```python
top_travel_cities[4]
```




    'Walla Walla Valley'




```python
top_travel_cities[4] = 4
```


```python
top_travel_cities
```




    ['Solta',
     'Greenville',
     'Buenos Aires',
     'Los Cabos',
     4,
     'Marakesh',
     'Albuquerque',
     'Archipelago Sea',
     'Iguazu Falls',
     'Salina Island',
     'Toronto',
     'Pyeongchang',
     'San Antonio']



And our list is now changed.  It's not a sensible list right now, so let's change it back.


```python
top_travel_cities[4] = 'Walla Walla Valley'
```

And our list is alright.


```python
top_travel_cities
```




    ['Solta',
     'Greenville',
     'Buenos Aires',
     'Los Cabos',
     'Walla Walla Valley',
     'Marakesh',
     'Albuquerque',
     'Archipelago Sea',
     'Iguazu Falls',
     'Salina Island',
     'Toronto',
     'Pyeongchang',
     'San Antonio']



### Finding Unique elements and length of lists

If we are not sure if there are repeated elements, we can use Python to get a unique list.


```python
top_travel_cities.append('Solta')
```

For example, now that we have added Solta to the end of our list, Solta appears twice.

Well to see a unique list of the elements, we can call the `set` function. The set function is non-destructive on our list.


```python
unique_travel_cities = set(top_travel_cities)
unique_travel_cities
```




    {'Albuquerque',
     'Archipelago Sea',
     'Buenos Aires',
     'Greenville',
     'Iguazu Falls',
     'Los Cabos',
     'Marakesh',
     'Pyeongchang',
     'Salina Island',
     'San Antonio',
     'Solta',
     'Toronto',
     'Walla Walla Valley'}



The set function initializes a new set in Python.  A set is a different type collection in Python.  


```python
set()
```




    set()



A set is just like a list, except elements do not have order and each element appears just once.


```python
unique_travel_cities[1]
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-106-8d1dfec3493a> in <module>()
    ----> 1 unique_travel_cities[1]
    

    TypeError: 'set' object does not support indexing


 So here, when we convert our list into a set, our set just consists of the unique elements.  But unfortunately this structure is a set, not a list.


```python
type(unique_travel_cities)
```




    set



So let's convert this set, which has a unique list of our travel cities, into a list.


```python
unique_travel_cities = list(unique_travel_cities)
```


```python
type(unique_travel_cities)
```




    list



So the array of `unique_travel_cities` is a unique list.


```python
unique_travel_cities
```




    ['Archipelago Sea',
     'Iguazu Falls',
     'Solta',
     'Los Cabos',
     'Walla Walla Valley',
     'Greenville',
     'Marakesh',
     'Toronto',
     'San Antonio',
     'Buenos Aires',
     'Salina Island',
     'Albuquerque',
     'Pyeongchang']



And you can see quickly that it differs from the list of top travel cities by checking the length.


```python
len(unique_travel_cities)
```




    13




```python
len(top_travel_cities)
```




    14




```python
top_travel_cities
```




    ['Solta',
     'Greenville',
     'Buenos Aires',
     'Los Cabos',
     'Walla Walla Valley',
     'Marakesh',
     'Albuquerque',
     'Archipelago Sea',
     'Iguazu Falls',
     'Salina Island',
     'Toronto',
     'Pyeongchang',
     'San Antonio',
     'Solta']



### Summary

In this section we saw how to associate data together in a collection, called a list.  A list is similar to a list in the real world - it implies the data has some connection, and that it has an order to it.  We initialize a list with the brackets, `[]`, and separate each element by a comma.  To access elements from a list, we use the bracket accessor followed by the index of the element we want to retrieve.  And our indices began at zero and increase from there.  To add a new element to the end of the list we use the `append` method, and to remove an element from the end of a list we use `pop`.  We can change elements anywhere between by first accessing the elements and then reassigning them.
