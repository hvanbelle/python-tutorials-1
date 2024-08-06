# python-tutorials-1

## Links: decorators-tutorial
- https://realpython.com/primer-on-python-decorators/
- https://docs.python.org/3/library/timeit.html

## Commands: decorators-tutorial
- python -i greeters.py
- python
-   from hello_decorator import say_whee
-   say_whee()
```
>>> from decorators import timer

>>> @timer
... def waste_some_time(num_times):
...     for _ in range(num_times):
...         sum([number**2 for number in range(10_000)])
...

>>> waste_some_time(1)
Finished waste_some_time() in 0.0010 secs

>>> waste_some_time(999)
Finished waste_some_time() in 0.3260 secs
```
- python -m timeit "'-'.join(str(n) for n in range(100))"
- python -m timeit "'-'.join([str(n) for n in range(100)])"
- python -m timeit "'-'.join(map(str, range(100)))"
```
import timeit
timeit.timeit('"-".join(str(n) for n in range(100))', number=10000)

timeit.timeit('"-".join([str(n) for n in range(100)])', number=10000)

timeit.timeit('"-".join(map(str, range(100)))', number=10000)
```