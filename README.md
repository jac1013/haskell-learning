# haskell-learning
##Just some notes about Haskell.

* Don't use Tabs for _layout_ method.
* ``:t`` will return the type of whatever you pass to it:
```
Prelude> :t True
True :: Bool
```
* The Numeric Types are: ``Int, Integer, Float, Double, Rational``
* ``()`` it's the same as ``void``.
* ``[]`` __Lists__ holds a collection of item of the same type:
```
Prelude> [1,2,3] 
[1,2,3]
```
```
Prelude> ['H', 'e', 'l','l','o'] 
"Hello"
```
* ``:`` operator appends an item to the beggining of a list:
```
Prelude> 1 : [2..10]
[1,2,3,4,5,6,7,8,9,10]
```
* __Tuples__ ``()`` hold a fixed number of items of different types:
```
Prelude> (1, True, "Hello", ['h','i'])
(1,True,"Hello","hi")
```
* ``map`` function applied to a list in action:
```
Prelude> map (+ 5) [1 .. 5]
[6,7,8,9,10]

```
* ``filter`` function applied to a list in action:
```
Prelude> filter (> 998) [1 .. 1000]
[999,1000]
```
* We have Booleans True / False
* there is ``&&``, ``||`` (these are shortciruit version), ``and``, ``or``, ``not``.
* ``and`` / ``or`` receive a list of Booleans and evaluate them.
* The expected ``if-then-else`` flow.
* Haskell doesn't accept different types in the expression inside an ``if-then-else`` statement
```
if true
then 1
else "Hi"
```
won't be accepted by the compiler neither the interpreter.
* ``==`` means equality and ``/=`` means inequality.
* To create projects use ``Cabal``
* Stanza are rules that goes after the Header ``Library`` or ``Executable``
* If we want an src folder we need to add a Stanza rule like this
```
hs-source-dirs : src 
-- Or whatever folder we want
```
* To create a module it must follow this Pattern ``A.B.C`` where A must be a folder, B too and C the file ``C.hs``, this must be inside your src folder
* To build the project we use ``cabal configure`` and ``cabal build``.
* The name of the functions must be _lowercase_ (this is not a convention, is a Haskell rule).
* The list of parameters should be separated by _spaces_ (and not by commas) also we don't need parenthesis.
* This is how we declare functions
```
nameOfFunction param1 param2 = bodyOfFunction
```
* How to declare the Type that a function can receive
```
(+++) :: [Integer] -> [Integer] -> [Integer] 
lst1 +++ lst2 = bodyOfFunction -- We are defining with infix notation)

sumChars :: [Char] -> [Char] -> [Char]
sumChars param1 param2 = bodyOfFunction
```
