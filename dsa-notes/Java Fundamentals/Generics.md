### PECS (Producer Extends Consumer Super)

### Notes

From [Stack Overflow](https://stackoverflow.com/questions/2723397/what-is-pecs-producer-extends-consumer-super)

Suppose you have a method that takes as its parameter a collection of things, but you want it to be more flexible than just accepting a `Collection<Thing>`.

**Case 1: You want to go through the collection and do things with each item.**  
Then the list is a **producer**, so you should use a `Collection<? extends Thing>`.

The reasoning is that a `Collection<? extends Thing>` could hold any subtype of `Thing`, and thus each element will behave as a `Thing` when you perform your operation. (You actually cannot add anything (except null) to a `Collection<? extends Thing>`, because you cannot know at runtime which _specific_ subtype of `Thing` the collection holds.)

**Case 2: You want to add things to the collection.**  
Then the list is a **consumer**, so you should use a `Collection<? super Thing>`.

The reasoning here is that unlike `Collection<? extends Thing>`, `Collection<? super Thing>` can always hold a `Thing` no matter what the actual parameterized type is. Here you don't care what is already in the list as long as it will allow a `Thing` to be added; this is what `? super Thing` guarantees.

Another way to remember the producer/consumer distinction is to think of a method signature. If you have a method `doSomethingWithList(List list)`, you are _consuming_ the list and so will need covariance / extends (or an invariant List). On the other hand if your method is `List doSomethingProvidingList`, then you are _producing_ the List and will need contravariance / super (or an invariant List).