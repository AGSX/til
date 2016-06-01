# Python Functions

**Date: June 1, 2016**

- You can assign functions to variables
```py
def function1():
  # do something
  
function2 = function1
```
- You can have a function with infinite arity. Just prepent an asterisk before the variable
```py
def function_name(*args):
  # do something
```

- There is no need to determine the return type of a function
```py
# You do not have to specify that you are going to return an integer
def add(addend1, addend2):
  return a + b
```

### References
- [Learn Python the Hard Way](http://learnpythonthehardway.org/book/)
