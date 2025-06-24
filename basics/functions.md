# Functions

Functions in Bash scripting are a great way to **reuse and organize code**. Instead of repeating the same code blocks, we can define them once inside a function and call them whenever needed.

---

##  What Is a Function?

A function is like a mini-script inside your main Bash script. It performs a specific task and helps avoid repetition. we can call a function multiple times and pass data into it too.

### When to Use Functions:
- When a task is repeated more than once.
- To break complex scripts into readable chunks.
- To improve maintainability and reusability.

---

## How to Define a Function

Bash supports two syntaxes for writing functions:

```bash
# Method 1
function_name () {
  # your commands here
}

# Method 2
function function_name {
  # your commands here
}
```

![image](https://github.com/user-attachments/assets/a48eeb32-a2cd-492b-895d-b62c8a29719a)
![image](https://github.com/user-attachments/assets/80d41b45-4621-4c42-8f0f-4bf0191fac77)


## Variable Scope
By default, Bash variables are global—they can be accessed anywhere in the script. But you can make a variable local to a function using the local keyword.

```bash
#!/bin/bash

var_change () {
  local var1='local 1'
  echo "Inside function: var1=$var1, var2=$var2"
  var1='changed again'
  var2='2 changed again'
}

var1='global 1'
var2='global 2'

echo "Before: var1=$var1, var2=$var2"
var_change
echo "After: var1=$var1, var2=$var2"

```
```output
Before: var1=global 1, var2=global 2
Inside function: var1=local 1, var2=global 2
After: var1=global 1, var2=2 changed again
```
