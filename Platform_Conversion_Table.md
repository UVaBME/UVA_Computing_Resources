# Converting between Python, R, and Matlab

Cheat sheet for converting between syntax of different languages. For similar resources, see the following links
- [TowardsDataScience: Python Dataframe to R Dataframe](https://towardsdatascience.com/cheat-sheet-for-python-dataframe-r-dataframe-syntax-conversions-450f656b44ca)
- [MIT Data Manipulation in Python and R](https://www.mit.edu/~amidi/teaching/data-science-tools/conversion-guide/r-python-data-manipulation/)

## Initializing variables and data structures

| Task | Python | R | Matlab |
|------|--------|---|--------|
| Initialize a variable | `x = 5` | `x <- 5` or `x = 5`| `x = 5;` |
| Initialize a list/vector/array | `x = [1,2,3]` | `x <- c(1,2,3)` | `x = [1,2,3];` or `x=1:3` |
| Initialize a matrix (2D array) | `x = [[1,2],[3,4]]` | `x <- matrix(c(1,2,3,4), nrow=2, ncol=2)` | `x = [1,2;3,4];` |
| Initialize a dataframe | <pre>` import pandas as pd`<br> `x = pd.DataFrame({'a':[1,2], 'b':[3,4]})` </pre> | `x <- data.frame(a=c(1,2), b=c(3,4))`  | - |


## Coding structures

| Task | Python | R | Matlab |
|------|--------|---|--------|
| If statement | <pre>` if x > 10:` <br>    `print(x)`</pre> |<pre>`if (x > 10){` <br>    `print(x)`<br>`}`</pre>  | <pre>`if x > 10` <br>    `disp(x)`<br>`end`</pre> |
| If-else statement | <pre>`if x > 10:` <br>    `print(x)`<br>`else:`<br>    `print("less than 10")`</pre> |<pre>`if (x > 10){` <br>    `print(x)`<br>`}else{`<br>    `print("less than 10")`<br>`}`</pre>  | <pre>`if x > 10` <br>    `disp(x)`<br>else<br>    `disp("less than 10")`<br>`end`</pre> |
| If-elif-else statement | <pre>`if x > 10:` <br>    `print(x)`<br>`elif x > 5:`<br>    `print("between 5 and 10")`<br>`else`:<br>    `print("less than 5")`</pre> |<pre>`if (x > 10){` <br>    `print(x)`<br>`}else if{`<br>    `print("between 5 and 10")`<br>`}else{`<br>    `print("less than 5")`<br>`}`</pre>  | <pre>`if x > 10` <br>    `disp(x)`<br>elseif<br>    `disp("between 5 and 10")`<br>`else`<br>    `disp("less than 5")`<br>`end`</pre>|
| For loop (iterate N times) | <pre>`for i in range(N):` <br>    `print(i)`</pre> | <pre> `for (i in 1:N){` <br>    `print(i)` <br> `}`</pre>| <pre> `for i = 1:N` <br>    `disp(i)` <br> `end` </pre> |
| For loop (iterate over list/vector) |  <pre>`for item in list:` <br>    `print(item)`</pre> |  <pre><code> `for (item in list){` <br>    `print(item)` <br> `}`| <pre> `for i = 1:length(list)` <br>    `disp(list(i))` <br> `end` </pre> |
| While loop |  <pre>`x = 0` <br>`while x < 10:` <br>    `x = x + 1` <br>    `print(x)` </pre> |  <pre>`x <- 0` <br>`while (x < 10){` <br>    `x <- x + 1`<br>    `print(x)` <br>`}`</pre>| <pre>`x = 0;` <br>`while x < 10` <br>    `x = x + 1;`<br>    `disp(x)` <br>`end`</pre> |
| Function definition |  <pre>`def add5(x):` <br>    `return x + 5`</pre> | <pre>`add5 <- function(x){` <br>    `x + 5`<br>`}`</pre> | <pre>`function [output] = add5(x)` <br>    `output = x + 5`<br>`end`</pre> |
| Function call |  <pre>`x = 5` <br>`y = add5(x)`</pre> |<pre>`x <- 5` <br>`y <- add5(x)`</pre>  | <pre>`x = 5;` <br>`y = add5(x);`</pre> |
| Class definition | <pre>`class ExampleClass:` <br>    `def __init__(self, x, y):`<br>        `self.x = x`<br>        `self.y` = y</pre> | | |
| Initializing a Class | <pre>`x = 5` <br>`y = 3`<br>`class_instance = ExampleClass(x, y)`</pre> | | |
