# alula

Alula is a static, weakly typed programming languages that focuses on parallelism and simplicity through the standardized use of the colon.


### Features
* All variable declarations, function calls, and and conditional statements require a colon to designate the beginning
* Any arguments are separated with a comma directly after the colon
* Chained functions are separated by ->, designated another "step"
* Parenthesis are exclusively used for logic and arithmetic precedence

### Examples
Hello World
```
print: "Hello World"
```

##### Fibonacci Sequence
Iteratively finds fibonacci number at the nth index value
```
function fibonacci: position {
  result: 1
  for: i: 1, i < (position -> length), i++ {
    result +: result
  }
  return: result
}
```

##### Average
Finds the average of a list of numbers
```
function average: list {
  multipled: 1
  for: i:0, i < (list -> length), i++ {
    multiplied *: list[i]
  }
  return multiplied / (list -> length)
}
```

##### Closure
A basic closure that finds the previous x value and multiplies it by y
```
function closure: x, y {
  currentX: x
  return: function next: {
    currentX: x * y
    return: currentX
  }
}

closureVariable: closure: 3, 2    
closureVariable -> next
```
