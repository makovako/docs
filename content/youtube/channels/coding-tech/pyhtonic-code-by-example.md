---
title: "Pythonic code, by example"
---

[00:00:33](https://www.youtube.com/watch?v=2-Ha3QXqfss&t=33)

writing code - think about other coworkers who will read it later

[00:01:23](https://www.youtube.com/watch?v=2-Ha3QXqfss&t=83)

pythonic - ways of writing code accepted by the comunity

[00:02:52](https://www.youtube.com/watch?v=2-Ha3QXqfss&t=172)

pythonic code
- 25 years of experience of many developers
- tuned for CPython
- easily read
- clean and simple

[00:06:58](https://www.youtube.com/watch?v=2-Ha3QXqfss&t=418)

use `.format` or f-strings for string formating

[00:07:18](https://www.youtube.com/watch?v=2-Ha3QXqfss&t=438)

you can give dictionary to format, keys in strings, values will be added `.format(**dictionaty)`

[00:09:49](https://www.youtube.com/watch?v=2-Ha3QXqfss&t=589)

merging dictionaries `m1 = {**m2, **m3, **m4, ...}`, most importand at the end, will override newer keys

[00:10:54](https://www.youtube.com/watch?v=2-Ha3QXqfss&t=654)

keyword arguments in function, to force the usegae when calling, put astreist as first argument
`def connect(*, user, server, ...)`

[00:12:45](https://www.youtube.com/watch?v=2-Ha3QXqfss&t=765)

on demand computation with yield - turn generating of infinite list of something into generator, like fibonaci numbers

[00:12:59](https://www.youtube.com/watch?v=2-Ha3QXqfss&t=779)

```python
def fibonacci_generator():
    current, nxt = 0,1
    while True:
       current, nxt = nxt, nxt + current
        yield current
```

[00:13:15](https://www.youtube.com/watch?v=2-Ha3QXqfss&t=795)

using yield when working with recursion

[00:14:41](https://www.youtube.com/watch?v=2-Ha3QXqfss&t=881)

counting iterables when i can't call len(), `count = sum(1 for _ in somehting)`

[00:15:43](https://www.youtube.com/watch?v=2-Ha3QXqfss&t=943)

slicing, e.g. `list[:5]`

[00:16:06](https://www.youtube.com/watch?v=2-Ha3QXqfss&t=966)

cannot slice generator

[00:16:20](https://www.youtube.com/watch?v=2-Ha3QXqfss&t=980)

slicing generator - `itertools.islice(generate(), 5)`

[00:16:49](https://www.youtube.com/watch?v=2-Ha3QXqfss&t=1009)

zen of python - `import this`

[00:21:37](https://www.youtube.com/watch?v=2-Ha3QXqfss&t=1297)

`__slots__ = ['a', 'b', 'c']`

[00:21:58](https://www.youtube.com/watch?v=2-Ha3QXqfss&t=1318)

"reserve" space for only things named in slots, so class will have only those properties, no new can be added (originaly class works like dictionary)

[00:25:44](https://www.youtube.com/watch?v=2-Ha3QXqfss&t=1544)

defining `__slots__` restricts values allowed in type but removes per instance dictionary backing store

[source](https://www.youtube.com/watch?v=2-Ha3QXqfss)
