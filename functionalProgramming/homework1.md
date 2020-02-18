Submission instructions: email your solutions in a single file called Solutions.idr, together with a file called statement.txt that says "I **your_name** certify that the solutions submitted are my own" to pawel@cs.ioc.ee. Deadline 12:00 19/02/2020.

# Functional Programming Assignment 1

 1. Given a list of integers, construct the list of their successive differences
    ``` idris
    differences [] == []
    differences [5] == []
    differences [5, 7, 12, 20] == [2, 5, 8]
    ```

 2. Uppercase the first character of each word in a string
    ``` idris
    titlecase "hello" == "Hello"
    titlecase "it was the best of times" == "It Was The Best Of Times"
    ```
    Hints: recall `pack` and `unpack` from last week, and read the
    documentation for `words` and `unwords`. The function `toUpper`
    will also be useful.

 3. Interactively titlecase the user's input using the repl function.
    ``` bash
    *idris> :exec interactive_titlecase
    string> it was the best of times
    It Was The Best Of Times
    ^D
    ```
 4. Return the average number of vowels in the words of a string,
    where a vowel is an element of ['a', 'e', 'i', 'o', 'u'], in
    either upper- or lowercase.
    ``` idris
    avg_vowels "a e i o u"
    1.0
    avg_vowels "it was the best of times"
    1.1666666666666667
    avg_vowels "aAa EeE iIi xXx"
    2.25
    ```
    Hints:
     * write a local function `is_vowel : Char -> Bool`, using elem,
     * write a local function `average : List Nat -> Double`, using cast and arithmetic.
     * use `map unpack . words` to get a list of lists of characters to analyze.

 5. Find all elements in both of two lists that satisfy a given predicate with
    a function `satInBoth : (Eq t) => (t -> Bool) -> List t -> List t -> List t`.
    ``` idris
    sat_in_both (< 5) [2,4,6,5] [3,4,6] == [4]
    sat_in_both (==0) [1..10]   [0..1]  == []
    satInBoth ((==5) . length) ["hello","world"] ["hello","bye"] == ["hello"]
    ```
    Hint: use `Data.List.intersect` by importing `Data.List`.

 6. Write the [Ackermann function](https://en.wikipedia.org/wiki/Ackermann_function)
    `ack : Nat -> Nat -> Nat`.
    ```
    ack 1 1 == 3
    ack 1 2 == 4
    ack 3 2 == 29
    ack 4 0 == 13
    ```

 7. Write a function that takes a list of integers and a default
    integer and returns a pair of the least and greatest elements of
    the list, or two copies of the default if the list is empty.
    ``` idris
    least_greatest 5 [2,3,8,4,7] == (2,8)
    least_greatest 0 [6..1]      == (0,6)
    ```
    Hints: Write a local function with the following signature:
    `min_max' : List Integer -> (Integer , Integer) -> (Integer ,
    Integer)` where the second argument is an accumulator consisting
    of the least and greatest numbers seen so far in the list.  Note
    that you can pattern match on both the list and the pair.  Use the
    `min` and `max` functions from the standard library

 8. Write a function producing the sum of first n even natural numbers.
    ``` idris
    sumevens 0 == 0
    sumevens 1 == 0
    sumevens 2 == 2
    sumevens 3 == 6
    sumevens 4 == 12
    ```

 9. Write a function that sums all the prime numbers that are less
    than or equal to a given number.
    ``` idris
    sum_primes 5 == 10
    sum_primes 10 == 17
    sum_primes 100 == 1060
    sum_primes 1000 == 76127
    ``` 






