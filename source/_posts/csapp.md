---
title: 'Computer Systems A Programmer’s Perspective - Bryant & O’Hallaron'
date: 2015-12-13 16:18:35
tags: book-review
---

{% img /images/csapp.png %}

Overall
===
'Computer Systems A Programmer’s Perspective' (CSAPP) is a very practical book about computer architecture. Most books on computer architecture focus on particular areas, such as: compilers, processor architecture, or programming language principles.

This book strives to envelope a good part of everything, to give readers a big picture. The authors tailor to the needs of most developers who want to write performing and reliable code. And they achieved the goal precisely.

It took me a month to finish studying it, mostly b/c it's level of abstraction is very low. However I've never regretted this time investment. Though it's subtle whether this helps my day-to-day work directly, I optimistically predict I will come back to this book more and more. As my understanding of computer systems deepen.

Caching and the memory mountain
===
'Because of the cache hierarchy, the effective rate that a program can access memory locations is not characterized by a single number. Rather, it is a wildly varying function of program locality (what we have dubbed the memory mountain) that can vary by orders of magnitude.' - Chapter 6. 
The efficiency of memory access is graphed as a mountain, with 'ridges' of temporal locality, and 'slopes' of spacial locality. 

- Temporal locality: the same data objects are likely to be reused multiple times. Once a data object has been copied into the cache on the first miss, we can expect a number of subsequent hits on that object. 
- Spatial locality: blocks usually contain multiple data objects. Be- cause of spatial locality, we can expect that the cost of copying a block after a miss will be amortized by subsequent references to other objects within that block.
