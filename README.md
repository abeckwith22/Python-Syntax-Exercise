# 22.1 Python Exercises

My code for 22.1 Python Exercises

`any7.py`

```python
def any7(nums):
    """Are any of these numbers a 7? (True/False)"""

    # YOUR CODE HERE 
    return 7 in nums # see! This 'in' works!

print("should be true", any7([1, 2, 7, 4, 5]))
print("should be false", any7([1, 2, 4, 5]))
```

`convert.py`

```python
def convert_temp(unit_in, unit_out, temp):
    """Convert farenheit <-> celsius and return results.

    - unit_in: either "f" or "c" 
    - unit_out: either "f" or "c"
    - temp: temperature (in f or c, depending on unit_in)

    Return results of conversion, if any.

    If unit_in or unit_out are invalid, return "Invalid unit [UNIT_IN]".

    For example:

      convert_temp("c", "f", 0)  =>  32.0
      convert_temp("f", "c", 212) => 100.0
    """

    # YOUR CODE HERE
    if unit_in == 'c' and unit_out == 'f':
        return (temp * 1.8) + 32 # celcius to fahrenheit
    elif unit_in == 'f' and unit_out == 'c': # fahrenheit to celcius
        return ((5.0/9.0) * (temp-32))
    else:
        return 'invalid unit'

print("c", "f", 0, convert_temp("c", "f", 0), "should be 32.0")
print("f", "c", 212, convert_temp("f", "c", 212), "should be 100.0")
print("z", "f", 32, convert_temp("z", "f", 32), "should be Invalid unit z")
print("c", "z", 32, convert_temp("c", "z", 32), "should be Invalid unit z")
print("f", "f", 75.5, convert_temp("f", "f", 75.5), "should be 75.5")
```

`count_up.py`

```python
def count_up(start, stop):
    """Print all numbers from start up to and including stop.

    For example:

        count_up(5, 7)

   should print:

        5
        6
        7
    """

    # YOUR CODE HERE
    while (start <= stop):
        print(start)
        start+=1


count_up(5, 7)        

```

`in_range.py`

```python
def in_range(nums, lowest, highest):
    """Print numbers inside range.

    - nums: list of numbers
    - lowest: lowest number to print
    - highest: highest number to print

    For example:

      in_range([10, 20, 30, 40], 15, 30)

    should print:

      20 fits
      30 fits
    """

    # YOUR CODE HERE
    for num in nums:
        if num >= lowest and num <= highest:
            print(str(num) + ' fits')


in_range([10, 20, 30, 40, 50], 15, 30)            

```
