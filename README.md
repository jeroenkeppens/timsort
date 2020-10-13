# Git debugging exercise

## Summary

This repository contains an implementation of timsort taken [Realpython](https://realpython.com) and adjusted to introduce a number of errors.  The purpose of the exercise is to practice employing past versions of a repository with a view to find a bug in the code.

## Requirements

To run this software, you need a *NIX command-line terminal with access to a Python interpreter.

## Instruction

To run the software, open a Python interpreter using either:

```
$ python3
```

or

```
$ python
```

Within the Python interpreter, load the `timsort.py` module:

```python
>>> import timsort as t
```

You can now call the timsort method as follows

```python
>>> t.timsort([2,1,3])
[1, 2, 3]
>>> t.timsort([4,5,2,3,1])
[1, 2, 3, 4, 5]
>>> t.timsort([6,5,4,3,2,1])
[1, 2, 3, 4, 5, 6]
>>> t.timsort([1,2])
[1, 2]
>>> t.timsort([1])
[1]
>>> t.timsort([])
[]
```


## Additional advice

You will find that some versions of this application do not produce correct results.  For example, in the latest version: 

```python
>>> t.timsort([2,3,1,0])
[0, 2, 2, 3]
```

Clearly, this should have produced [0, 1, 2, 3] instead.  At some point in development, a bug was introduced.  Your task is to find the error.

Use `git log` to see the commits.  Review older commits and attempt to run the code in these older commits until you find a version that is not buggy.
