# miniRSA
The first thing i realised in this file since the cyphertext is much smaller than N, then decoded text has to be an even smaller number, the key is very small, and after looking up i tried to cube root the given cypher text.

Found the code to get root of a number from https://stackoverflow.com/questions/55436001/cube-root-of-a-very-large-number-using-only-math-library 

```
def find_invpow(x,n):
    """Finds the integer component of the n'th root of x,
    an integer such that y ** n <= x < (y + 1) ** n.
    """
    high = 1
    while high ** n < x:
        high *= 2
    low = high/2
    while low < high:
        mid = (low + high) // 2
        if low < mid and mid**n < x:
            low = mid
        elif high > mid and mid**n > x:
            high = mid
        else:
            return mid
    return mid + 1
```
```
