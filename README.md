# Functions

## Learning Goals

- Explain functions.
- Call or invoke functions.
- Define your own functions.

## Introduction

A function is a construct for creating reusable instructions. We have been using
various built-in functions such as `print` and `type`.

## Call or Invoke Functions

When a function name is followed by `()` we say that the function is being
called or invoked. This means we are instructing the computer to run the
instructions stored inside the function.

```python
print()
```

This line displays an empty line in the console.

We can pass inputs to a function in the `()`. An argument is the input value
that is passed to a function when calling or invoking it.

```python
print("Hello!")
```

In the above line, `"Hello!"` is an argument that is being passed to the
function `print`.

Functions can take in multiple arguments. The `print` function is capable of
doing this:

```python
print("Hello", "World", "!")
```

Output:

```python
Hello World !
```

## Function Output and Side Effects

A function can produce an output and/or cause a side effect.

![Untitled](https://curriculum-content.s3.amazonaws.com/intro-to-coding-python/functions/01.png)

The `print` function has been displaying values in the console. This is called a
side effect because the function is not producing any output.

![Untitled](https://curriculum-content.s3.amazonaws.com/intro-to-coding-python/functions/02.png)

```python
print_output = print("Hello")
print(print_output)
```

```python
Hello
None
```

Note that `None` is a special data type that represents the absence of a value
in Python. Whenever a function produces `None`, we say that the function doesn’t
have an output.

Now let’s look at a function that produces an output. The `int` function takes a
`str` as an argument, converts it into an `int`, and produces the converted
value.

![Untitled](https://curriculum-content.s3.amazonaws.com/intro-to-coding-python/functions/03.png)

```python
year_str = "2000"
year_int = int(year_str)
print(year_int)
```

## Declaring Your Own Function

Python provides the `def` keyword for defining our own functions. Here’s the
general structure:

```python
def function_name(parameter):
	# function body
```

A parameter is a variable label for the argument that is passed into the
function when calling or invoking it. We will look at an example later in this
lesson and explore this idea further.

Let’s look at a few examples:

- Function with no parameters.
- Function with one parameter.
- Function with multiple parameters.

### No Parameter

```python
def greet():
  print("Hello!")

greet()
```

- The function name is `greet`.
- This function has no parameters.
- We can call other functions inside a function body. In this case, we are
  calling the `print` function.
- The function is causing a side effect by calling the `print` function inside
  of it.

### One Parameter

```python
def greet_person(name):
	print("Hello " + name + "!")

greet_person('Al') # Hello Al!
```

- The function name is `greet_person`.
- It has a single parameter called `name`.
- We call or invoke the `greet_person` function with the argument `'Al'`.
- After the function is called, the argument value `Al` is assigned to the
  parameter label `name`. We can think of `name` as a variable which points to
  the value `Al`.
- The expression argument passed to the `print` function is evaluated to
  `"Hello " + "Al" + "!"` which is then evaluated to `"Hello Al!"`.
- Finally, `print("Hello Al!")` is executed.

### Multiple Parameter

```python
def add(num1, num2):
  total = num1 + num2
  print(total)

add(3, 2)
```

- The function name is `add`.
- It has two parameters: `num1` and `num2`.
- We call the function with the arguments `3` and `2`.
- `num1` is assigned the value of `3` and `num2` is assigned the value of `2`.
- The `num1 + num2` expression gets evaluated to `3 + 2` which produces a final
  value of `5`.
- The final value of `5` is assigned to the `total` variable.
- The `print` function is called with the argument `total` (`5`).
- This displays the value `5` in the console.

You should use the
[PythonTutor](https://pythontutor.com/python-debugger.html#mode=edit) tool to
visualize the execution of the different functions.

## Declare a Function that Returns a Value

We said earlier that a function can either produce an output or cause side
effects. So far, we have been declaring functions that produce a side effect.
Python provides the `return` keyword to produce a value from a function.

```python
def add(num1, num2):
  total = num1 + num2
  return total

add_output = add(3, 2)
print(add_output)
```

![Untitled](https://curriculum-content.s3.amazonaws.com/intro-to-coding-python/functions/04.png)

- The function name is `add`.
- It has two parameters: `num1` and `num2`.
- We call the function with the arguments `3` and `2`.
- `num1` is assigned the value of `3` and `num2` is assigned the value of `2`.
- The `num1 + num2` expression gets evaluated to `3 + 2` which produces a final
  value of `5`.
- The final value of `5` is assigned to the `total` variable.
- The `return total` line produces the value `5` as an output.
- The output from the `add` function is assigned to the `add_output` variable.
- The `print` function is called with the argument `add_output` (`5`).
- This displays the value `5` in the console.

Note that the `return` statement can only produce a single value.

## Conclusion

We have learned several new concepts in this lesson. Since we can create
reusable instructions, we can significantly simplify how we write our programs!
Functions are one of the most powerful abstractions in programming!
