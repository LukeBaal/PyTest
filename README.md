# Pest Control

A Python Unit Testing Library

## Usage

Test Functions:
- assertEquals(actual, expected, msg) - Test if actual = expected, if test fails, print out includes msg
- assertTrue(actual, msg) - Test if actual = True, if test fails, print out includes msg
- assertFalse(actual, msg) - Test if actual = False, if test fails, print out includes msg

### How to

Start by importing the library. Assuming file is in same directory as the PestControl library directory:
```python
from PestControl.pest_control import PestCase
```

Then make a class that extends PestCase to be the unit test class (class name can be anything, "BasicTestCase" is used here)
```python
class BasicTestCase(PestCase):
```

Then write one or more functions for the actual test. NOTE: "test" MUST be somewhere in the function name.
For example, add_test(), addTest(), addTesting(), add_Tester(), add_tester(), will all run, but add(), will not run.  
```python
class BasicTestCase(PestCase):
    def add_test(self):
        self.assertEquals(1+1, 2, "simple add test")
```

Now just add the main() funciton call
```python
if __name__ == "__main__":
    PestCase().main()
```

That's it! Your unit test will run and print to the console the results. Note: any errors that occur from a call to an assert function, ie errors caused by the code being tested, will be caught and logged as a failed test.

Full Example:
```python
from pest_control import PestCase
class BasicTestCase(PestCase):
    def add_test(self):
        self.assertEquals(1+1, 2, "simple add test")

if __name__ == "__main__":
    PestCase().main()
```
