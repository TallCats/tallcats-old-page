# Functional Programming Exercise Session 2

 1. Rewrite your list-reversing function from last week so that it
    doesn't use append `(++)`, but instead uses only conses `(::)`.  This
    will be more efficient because each append must traverse the entire
    list, whereas cons is a constant time operation.
 
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

 3. Write a function returning the list of all divisors of n.
    Hint: k is a divisor of n iff `mod k n == 0`.

 4. Use your divisors function to define a primality predicate.
    Hint: a prime number has exactly two divisors.
