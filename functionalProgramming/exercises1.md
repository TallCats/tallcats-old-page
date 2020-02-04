# Functional Programming Exercise Session 1

<ol style="padding:30;margin:10">
<li> Implement a function <pre>myReverse: List ty -&gt; List ty</pre> that reverses lists.
</li>
<li> Write a function <pre>revString: String -&gt; String</pre> that reverses strings.
You may find the Prelude functions <pre>unpack: String -&gt; List Char</pre> and its inverse <pre>pack</pre> useful.
</li>
<li> Implement a function <pre>palindrome: String -&gt; Bool</pre> that tests whether a string is a palindrome
</li>
<li>
Implement a function <pre>cycle: List ty -&gt; Nat -&gt; List ty</pre> that takes a list and repeats it the required number of times.
</li>
<li>
Write a function
<pre>deal: List ty -&gt; (List ty, List ty)</pre>
that splits a list into two lists, containing its even and odd elements.
You may find it useful to start by writing functions <pre>odds: List ty -&gt; List ty</pre> and <pre>evens: List ty -&gt; List ty</pre>
</li>
<li>
Write a function <pre>top_three : List a -&gt; List a</pre>
that outputs the three largest elements of a list. You may find the following predefined functions useful: <pre>take : Nat -&gt; List a -&gt; List a</pre>
and <pre>sort : Ord a =&gt; List a -&gt; List a</pre>. Check out the documentation (<pre>:doc</pre>) for the details.
</li>
<li>
Write a function
<pre>myUnzip: List (ty, ty&#39;) -&gt; (List ty, List ty&#39;)</pre>
that unzips a zipped list.
</li>
<li>
Idris has some nice syntax for updating elements of a record. Recall the <pre>Address</pre> record definition from the lectures. Type it out (and mind the typo, <pre> country </pre> should be type <pre>String</pre> not <pre>string</pre>.) Check the type of <pre>record {city = &quot;Tallinn&quot;}</pre> or <pre> record {city = &quot;Tallinn&quot;, postcode=10138}</pre>. Define a new record type called <pre>Street</pre> that has fields <pre>number: Int</pre> and <pre>street : String</pre>.
Write functions <pre>getStreet: Address -&gt; Street</pre>
and <pre>setStreet: Street -&gt; Address -&gt; Address</pre>.
</li>
</ol>
