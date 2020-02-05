# Functional Programming Exercise Session 1

 1. Implement a function `myReverse: List ty -> List ty` that reverses lists.

 2. Write a function `revString: String -> String` that reverses
    strings. You may find the Prelude functions `unpack: String ->
    List Char` and its inverse `pack` useful.

 3. Implement a function `palindrome: String -> Bool` that tests
    whether a string is a palindrome.

 4. Implement a function `cycle: List ty -> Nat -> List ty` that takes
    a list and repeats it the required number of times.

 5. Write a function `deal: List ty -> (List ty, List ty)` that
    splits a list into two lists, containing its even and odd
    elements. You may find it useful to start by writing functions `odds:
    List ty -> List ty` and `evens: List ty -> List ty`.

 6. Write a function `top_three : Ord a => List a -> List a` that outputs the
    three largest elements of a list. You may find the following
    predefined functions useful: `take : Nat -> List a -> List a` and
    `sort : Ord a => List a -> List a`. Check out the documentation
    (`:doc`) for the details.

 7. Write a function `myUnzip: List (ty, ty') -> (List ty, List ty')` that unzips a zipped list.

 8. Idris has some nice syntax for updating elements of a
    record. Recall the `Address` record definition from the lectures. Type
    it out (and mind the typo, `country` should be type `String` not
    `string`.) Check the type of `record {city = "Tallinn"}` or `record
    {city = "Tallinn", postcode=10138}`. Define a new record type called
    `Street` that has fields `number: Int` and `street : String`.  Write
    functions `getStreet: Address -> Street` and `setStreet: Street ->
    Address -> Address`.
