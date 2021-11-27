---
title: "How decorators function"
---

[00:00:21](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=21)

@ - above functions in python - decorators

[00:00:30](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=30)

wrap additional code around existing definitions

[00:01:14](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=74)

decorator is just another function

[00:01:20](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=80)

it takes in a function as a argument

[00:02:12](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=132)

Example:
```python
def traces(func):
    def wrapper():
        print("entering")
        func()
        print("exiting")
    return wrapper

@tracer
def hello_world():
    print("Hello world")
```

[00:02:20](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=140)

Whenever the decorator is called, it will get replaced by the wrapper function, which runs

[00:02:38](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=158)

decorators wrap functions around functions

[00:03:12](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=192)

in python functions are just objects, we are passing functions into functions

[00:03:15](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=195)

we can
- pass functions as arguments
- define new functions inside fintions
- return functions

[00:03:23](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=203)



[00:04:57](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=297)

aspect oriented programming - code can be inserted before or after the execution

[00:05:33](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=333)

Decorators change identity of a function to the returned function of the decorator

[00:05:44](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=344)

Solution:
```python
import functools
...
@functools.wraps(func
def wrapper():
...
```

[00:06:51](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=411)

Arguments handling:
```python
...
def wrapper(*args, **kwargs):
...
answer = func(*args, **kwargs)
...
return answer
...
```

[00:07:48](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=468)

example - run function twice (1st run, 2nd return from decorator to run)

[00:08:32](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=512)

decorator nesting - use more decorators on one function

[00:08:47](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=527)

order of decorators - from the closest to the inner function

[00:09:22](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=562)

example - scrubbing and validating inputs

[00:10:13](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=613)

e.g. always converting inputs to integers

[00:11:22](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=682)

decorators with arguments:
```python
def repeat(count):
    def repeat_decorator(func):
        @functools.wraps(func)
        def wrapper(*args, **kwargs):
            for_ in range(count):
                func(*args, **kwargs)
        return wrapper
    return repeat_decorator

@repeat(5)
def hello_world():
    print("hello world")
```

[00:12:35](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=755)

associating som evalue to the wrapper function (like wrapper.count) is shared for every execution and can store some state if needed

[00:13:24](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=804)

decorators can be applied on methods and classes (on constructor)

[00:14:28](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=868)

testing decorators

[00:15:39](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=939)

- separate tests for decorator and decorated function
- apply decorator to fake testing function
- conver all possible ways the decorator can be used (decorator parameters, function args, return, id, ...)

[00:18:12](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=1092)

Python decorators available

[00:18:19](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=1099)

- @classmethod
- @staticmethod
- @property (getters, settters)
- @app.route (flask)
- @pytest.mark.parametrize

[00:18:55](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=1135)

@classmethod - chagens to class method from a class instance method
```python
class Greeter:
    @classmethod
    def hello(cls):
        ...

Greeter.hello()
```

cls - reference to the class it was called from

[00:19:38](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=1178)

@staticmethod - same as classmethod but it does not pass reference to the class

[00:20:44](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=1244)

```python
@property
def count(self):
    return self._count
```
count will work as argument, instead of a method

[00:21:14](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=1274)

```python
@count.setter
def count(self, value):
    if value < 0:
        raise ValueError
    self._count = value
```

[00:25:54](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=1554)

Use cases for decorators:
- logging
- profiling
- input validation
- retries
- registries

[00:26:32](https://www.youtube.com/watch?v=vtoXyxcfmUo&t=1592)

Bad examples:
- main behaviors
- complicated logic
- heavy conditional logic
- avoiding the wrapped function

[source](https://www.youtube.com/watch?v=vtoXyxcfmUo)
