# Functional Programming Exercise Session 2

 1. Rewrite your list-reversing function `myReverse` from last week so that it
    doesn't use append `(++)`, but instead uses only conses `(::)`.  This
    will be more efficient because each append must traverse the entire
    list, whereas cons is a constant time operation.
    ``` idris
    rev [1,2,3] == [3,2,1]
    ```
    Hint: use a local function with signature: `rev' : (xs : List ty) ->
    (acc : List ty) -> List ty` where the second argument is an
    accumulator, storing the reversal of the list prefix seen so far.
    That way when you reach the case for the empty list the accumulator
    will hold the reversal of the whole list.

 2. Write a function producing the sum of the squares of the first n natural numbers
    ``` idris
    sumsqares 0 == 0
    sumsqares 1 == 0
    sumsqares 2 == 1
    sumsqares 3 == 5
    sumsqares 4 == 14
    ```
    Hint: use the `map` and `sum` functions, and the `[m .. n]` syntactic sugar for lists.

 3. Interactively add the user's input using the repl function.
    ``` bash
    *idris> :exec interactive_addition
    space-separated numbers to add:
    0
    space-separated numbers to add: 1 2 3
    6
    space-separated numbers to add: 5 5 5
    15
    space-separated numbers to add: -2 4 
    2
    ^D
    ```
    Hint: read the documentation for `sum`.

 4. Write a function returning the list of all divisors of n.
    ``` idris
    divisors 24 == [1, 2, 3, 4, 6, 8, 12, 24]
    divisors 15 == [1, 3, 5, 15]
    divisors 1 == [1]
    ```
    Hint: k is a divisor of n iff `mod k n == 0`.

 5. Use your divisors function to define a primality predicate.
    ``` idris
    is_prime 4 == False
    is_prime 5 == True
    is_prime 29 == True
    is_prime 57 == False
    ```
    Hint: a prime number has exactly two divisors.
