---
title: The Little Schemer - Daniel P. Friedman & Matthias Felleisen
date: 2016-08-15 16:18:35
tags: book-review
---

{% img /images/the-little-schemer.png %}

### Motivation
Aiming at changing my perspectives about programming, I decided to start learning Lisp, the very first functional language. 'The Little Schemer', all references I've found highly suggested this as the starter book. And this is great for learning the functional way of thinking about computing.

### What's Good
Very delightful and light-weighted, in both the writing style and the length of the book. The entire book is organized as dialogues. With authors motivating active thinking in every single step, the very complicated ideas are unveiled. To my opinion this is the most effective way of learning, as it gives readers the illusion of inventing Lisp themselves. This work is also extremely short 200 pages, considering Lisp/Scheme is such a vast language. Authors managed to deliver the power fundamentals of s-expressions and lists.

### The Five Rules
- The primitive car is defined only for non-empty lists.
- The primitive cdr is defined only for non- empty lists. The cdr of any non-empty list is always another list.
- The primitive cons takes two arguments. The second argument to cons must be a list. The result is a list.
- The primitive null? is defined only for lists.
- The primitive eq'l takes two arguments. Each must be a non-numeric atom.

### Follow-up Thoughts
Though Lisp is currently very much a research language, and of little production use. The real value it provides is a way of thinking about computing. And the recursive nature of s-exp is the very best descriptor of recursive data structure and algorithms.

The beauty of Lisp is that it can be entirely derived from a tiny, compact core of a short list of axioms:

