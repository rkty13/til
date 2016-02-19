# Get List of Member Variables of a Class

You may find that you need to get all of the member variables of a class you've created. By using the `dir()` function, you can all attributes of the class, and you then need to do a little filtering to get a list of just the member variables.

Consider the following:

```
>>> class Foo(object):
...    x = 1
...    y = 2

>>> dir(Foo)
['__class__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__', '__le__', '__lt__', '__module__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', '__weakref__', 'x', 'y']
```

As you can see, there are a lot of built-in functions and other attributes of `Foo`. To get a list of just `x` and `y`, or any other member variables you have declared, you can use a list comprehension to filter out functions and any other attribute that may have been built-in.

```
>>> [memvar for memvar in dir(Foo) if not callable(memvar) and not memvar.startswith("__")]
['x', 'y']
```

[source](http://stackoverflow.com/questions/1398022/looping-over-all-member-variables-of-a-class-in-python)