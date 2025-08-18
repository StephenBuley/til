Arrays.fill

In Java I mostly find myself working with `List`s of items, and have gotten used to using a lot of the APIs that come along with `ArrayList`s. However, a recent file I had to work on was using arrays instead. I needed to fill an array of length 30 with all the same double, and I discovered that array objects do not have many utility helper functions to work with them - they live in the static `Arrays` helper class. Specifically to fulfill my need I needed `Arrays.fill(object, val)`. This one liner fills the array with the specified value.

```java
double[] myDoubleArr = new double[30]; // initialize empty array of length 30
// I original trie to find something like this:
myDoubleArr.fill()? myDoubleArr.stream()? myDoubleArr.map()?
// nothing!
// Here is how you do it!
Arrays.fill(myDoubleArr, myValue);
```

Lots of other helpers in the Arrays class as well, I'm sure I will continue to discover more.
