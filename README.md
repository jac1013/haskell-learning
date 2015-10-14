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
