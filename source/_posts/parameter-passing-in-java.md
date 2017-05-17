---
title: 'Parameter passing in Java - by reference or by value?'
date: 2012-12-15 20:15:35
tags: career
---

Myth: "Objects are passed by reference, primitives are passed by value"
---
Some proponents of this then say, "Ah, except for immutable objects which are passed by value [etc]" which introduces loads of rules without really tackling how Java works. Fortunately the truth is much simpler:

> Truth #1: Everything in Java is passed by value. Objects, however, are never passed at all.

That needs some explanation - after all, if we can't pass objects, how can we do any work? The answer is that we pass references to objects. That sounds like it's getting dangerously close to the myth, until you look at truth #2:

> Truth #2: The values of variables are always primitives or references, never objects.

This is probably the single most important point in learning Java properly.
It's amazing how far you can actually get without knowing it, in fact - but vast numbers of things suddenly make sense when you grasp it.

Why is all this important?
---
When people hear the words "pass by reference", they may understand different things by the words. There are some pretty specific definitions of what it should mean, however. Dale King sometimes quotes this one: "The lvalue of the formal parameter is set to the lvalue of the actual parameter." (Dale's formal analysis of this whole question can be found at the bottom of this page.) This would mean that if you wrote the following code:

```
  Object x = null;
  giveMeAString(x);
  System.out.println(x);

  void giveMeAString(Object y) {
    y = "This is a string";
  }
```
the result (if Java used pass-by-reference semantics) would be

```
This is a string
```
instead of the actual result:
```
null
```

Explaining the two truths above eliminates all of this confusion.

So what does passing a reference by value actually mean?

> It means you can think of references how you think of primitives, to a large extent. 

For instance, the equivalent to the above bit of code using primitives would be:
```
  int x = 0;
  giveMeATen(x);
  System.out.println(x);

  void giveMeATen (int y) {
    y = 10;
  }
```

The balloon analogy
===
I imagine every object as a helium balloon, every reference as a piece of string, and every variable as something which can hold onto a piece of string. 

If the reference is a null reference, that's like having a piece of string without anything attached to the end. If it's a reference to a genuine object, it's a piece of string tied onto the balloon representing that object. When a reference is copied (either for variable assignment or as part of a method call) it's as if another piece of string is created attached to whatever the first piece of string is attached to. The actual piece of string the variable (if any) is holding onto doesn't go anywhere - it's only copied.

This analogy also explains garbage collection (apart from the java.lang.ref API, which does "odd" things :) - a balloon floats away unless it is tethered down to something. The balloons can have further holders on them (instance variables), but just because two balloons are holding onto each other doesn't stop them from floating away. (Cyclic references are collected.) Any balloon representing an object which is in the middle of having a method invoked is tethered to the JVM. (Apologies for not being able to phrase that more succinctly - all I mean is that anything in an active thread's stack isn't garbage collected.)
