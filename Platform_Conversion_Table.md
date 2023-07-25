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
| Initialize a dataframe | <pre><code>`import pandas as pd`<br>`x = pd.DataFrame({'a':[1,2], 'b':[3,4]})` </code></pre> | `x <- data.frame(a=c(1,2), b=c(3,4))`  | - |


## Coding structures

| Task | Python | R | Matlab |
|------|--------|---|--------|
| If statement | <pre><code>`if x > 10:` <br>    `print(x)`</code></pre> |<pre><code>`if (x > 10){` <br>    `print(x)`<br>`}`</code></pre>  | <pre><code>`if x > 10` <br>    `disp(x)`<br>`end`</code></pre> |
| If-else statement | <pre><code>`if x > 10:` <br>    `print(x)`<br>`else:`<br>    `print("less than 10")`</code></pre> |<pre><code>`if (x > 10){` <br>    `print(x)`<br>`}else{`<br>    `print("less than 10")`<br>`}`</code></pre>  | <pre><code>`if x > 10` <br>    `disp(x)`<br>else<br>    `disp("less than 10")`<br>`end`</code></pre> |
| If-elif-else statement | <pre><code>`if x > 10:` <br>    `print(x)`<br>`elif x > 5:`<br>    `print("between 5 and 10")`<br>`else`:<br>    `print("less than 5")`</code></pre> |<pre><code>`if (x > 10){` <br>    `print(x)`<br>`}else if{`<br>    `print("between 5 and 10")`<br>`}else{`<br>    `print("less than 5")`<br>`}`</code></pre>  | <pre><code>`if x > 10` <br>    `disp(x)`<br>elseif<br>    `disp("between 5 and 10")`<br>`else`<br>    `disp("less than 5")`<br>`end`</code></pre>|
| For loop (iterate N times) | <pre><code> `for i in range(N):` <br>    `print(i)`</code></pre> | <pre><code> `for (i in 1:N){` <br>    `print(i)` <br> `}`| <pre><code> `for i = 1:N` <br>    `disp(i)` <br> `end` </code></pre> |
| For loop (iterate over list/vector) |  <pre><code> `for item in list:` <br>    `print(item)`</code></pre> |  <pre><code> `for (item in list){` <br>    `print(item)` <br> `}`| <pre><code> `for i = 1:length(list)` <br>    `disp(list(i))` <br> `end` </code></pre> |
| While loop |  <pre><code>`x = 0` <br>`while x < 10:` <br>    `x = x + 1` <br>    `print(x)` </code></pre> |  <pre><code>`x <- 0` <br>`while (x < 10){` <br>    `x <- x + 1`<br>    `print(x)` <br>`}`| <pre><code>`x = 0;` <br>`while x < 10` <br>    `x = x + 1;`<br>    `disp(x)` <br>`end` |
| Function definition |  <pre><code>`def add5(x):` <br>    `return x + 5`</code></pre> | <pre><code>`add5 <- function(x){` <br>    `x + 5`<br>`}`</code></pre> | <pre><code>`function [output] = add5(x)` <br>    `output = x + 5`<br>`end`</code></pre> |
| Function call |  <pre><code>`x = 5` <br>`y = add5(x)`</code></pre> |<pre><code>`x <- 5` <br>`y <- add5(x)`</code></pre>  | <pre><code>`x = 5;` <br>`y = add5(x);`</code></pre> |
| Class definition | <pre><code>`class ExampleClass:` <br>    `def __init__(self, x, y):`<br>        `self.x = x`<br>        `self.y` = y</code></pre> | | |
| Initializing a Class | <pre><code>`x = 5` <br>`y = 3`<br>`class_instance = ExampleClass(x, y)`</code></pre> | | |