---
layout: post
title: On Counting
---

#On counting#

I've wanted to write about this for a while but never really got the chance. One of the coolest things about modern mathematics is infinity: we have found all sorts of ways to study and classify different notions of "size" and "number" that can result in the most counterintuitive results imaginable. I want to look at a few examples, starting today.


##Counting##

Let's begin with the natural numbers, the set 

\\[\mathbb{N} = \\{1, 2, 3, ... \\}\\]

This is "clearly" an <span style="font-variant:small-caps;">infinite</span> set, as indicated by the ellipsis. 
What does "infinite" mean in this case? 
Now we know that we can add natural numbers together to produce natural numbers; more simply, we can add the number $$1$$ to a natural number \\(n\\) to produce a new natural number $$$n + 1$$$. $$\mathbb{N}$$ is infinite in the sense that there is simply no "end" to it, at least in one direction (because there is such a thing as the smallest natural number, which is $$$1$$$). To rephrase that, there is simply no way to list every single element of $$$\mathbb{N}$$$, whereas for any finite set, no matter how large it may be, you can eventually list out every element.


Before we go any further, let's actually get a handle of what counting means. In real life, when we have to count out a bunch of things, we essentially point at each item once (and only once) and call out the natural numbers in order. We are in effect uniquely indexing every item with one (and only one) of the natural numbers. There is nothing twisted or weird about this; this is the most "natural" (pardon the pun) way of counting things.

What this definition of counting allows us to do is to compare the size of different sets: we can know that a sack of three potatoes is the same numerical size as a sack of three apples because we can index both of them with the set $$$\\{1, 2, 3\\}$$$. (It should be clear that it does not matter
which potato we're pointing to when we call out a particular number; all
that matters that we point to each potato only once and we call out the
numbers in order only once.) Now so far this sounds like a ridiculously
overdone way of stating the utterly obvious (and I've not even pulled
out real mathematical terminology or notation!), but the utility of such
abstraction will become more and more evident as we journey along.

###Counting Finite Sets###

Take a finite subset of $$$\mathbb{N}$$$, say $$$X = \\{1, 2, ..., 100\\}$$$. We know that all natural numbers are either even or odd, so we can divide the
set $$$X$$$ into two halves ("partition" it into two), say $$$A = \\{1, 3,
5, ..., 99\\}$$$ and $$$B = \\{2, 4, ..., 100\\}$$$. 

Furthermore, we know that
these two sets are both the same size because they contain $$$50$$$ elements
each; in other words, we can go through the elements of $$$A$$$ saying
"one", "two", "three", and so on, and we'll eventually hit the number
"fifty", and the same is true for $$$B$$$ too. More formally, we can write
$$$A = \\{2k - 1 : k \in \\{1, 2, ..., 50\\} \\}$$$ and $$$B = \\{2k :
k \in \\{1, 2, ..., 50\\} \\}$$$, and then it's pretty clear that the two sets
are the same size as each other. And most importantly, we can also see
that $$$A$$$ and $$$B$$$ are each exactly *half* the size of $$$X$$$, which
also makes complete sense.



 Now let's take $$$C = \\{3, 6, 9, …, 99\\}$$$, $$$D = \\{2, 5, 8, …, 98\\}$$$,
and $$$E = \\{1, 4, 7, …, 97, 100\\}$$$. They are not all the same size,
because $$$C$$$ and $$$D$$$ both have $$$33$$$ elements while $$$E$$$ has $$$34$$$ elements, but it is true that they form a partition of $$$X$$$ and that
the total number of elements in them adds up to $$$100$$$, as should be the
case.



###Counting Infinite Sets###

Nothing new or exciting so far, so let's try something fancier. What
about the whole set of even numbers? (Lets call it $$$2\mathbb{N}$$$, for a reason that will soon become clear.) Clearly $$$2\mathbb{N}$$$ is a subset of $$$\mathbb{N}$$$.
Similarly,  the set of all odd numbers (let's call it $$$2\mathbb{N} - 1$$$, but let's not actually think of that as some sort of subtraction) is a
subset of $$$\mathbb{N}$$$. 

Clearly, there is no number that $$$2\mathbb{N}$$$ and $$$2\mathbb{N} - 1$$$ both have in common. What's more, $$$2\mathbb{N}$$$ and $$$2\mathbb{N} - 1$$$ together account for all the natural numbers. In other words, it seems intuitive to say that $$$\mathbb{N}$$$ is exactly "twice" as large as $$$2\mathbb{N}$$$, right? After all, that's exactly what we saw with $$$X$$$ and $$$A$$$ and $$$B$$$ above.

Wrong. 

####Multiples of $$$2$$$###
In fact, $$$2\mathbb{N}$$$ is exactly the same size as $$$\mathbb{N}$$$, and $$$2\mathbb{N} - 1$$$ is exactly the same size as $$$\mathbb{N}$$$ as well. How on earth can this be true? This simply makes no sense! If this result doesn't shock you, it should. To paraphrase [Niels Bohr's remark about quantum
mechanics](http://en.wikiquote.org/wiki/Quantum_mechanics), "those who
are not shocked when they first come across infinity cannot possibly
have understood it." 


Let's go back to our definition of counting. If we go through the list
of even numbers, we can uniquely assign to each and every even number
one and exactly one natural number; similarly, if we go through the list
of natural numbers, we can uniquely assign to each and every natural
number one and exactly one natural number. (How do we do this? We can
index every even number $$$x$$$ using the natural number $$$\frac{x}{2}$$$; we can also index every natural number $$$n$$$ using the even number 2$$$n$$$.) But if there exists a unique element of one set that uniquely corresponds to a
unique element of the second set (in other words, if there exists a
bijection between the set of even numbers and the set of natural
numbers), then it is clear that the two sets *are the same size*. Even
though there are natural numbers that are clearly not even numbers!


It is important to note that it is precisely the fact that we are
considering the set of *all* even numbers that allows for this
possibility to happen. If you take any finite subset of even numbers,
then there is no way to uniquely map every natural number to that set.
It is only when we take the infinite set of even numbers that it becomes
possible to uniquely map every even number to a natural number, and vice
versa. There is something crazy about infinity that allows an infinite
set to contain an infinite subset that is just as large as itself ...

####Multiples of $$$3$$$###
But wait, it gets worse. Take the set of multiples of $$$3$$$ and call it
$$$3\mathbb{N}$$$ (perhaps you can now see where I'm going with this?). It's clear that there is a bijection between $$$3\mathbb{N}$$$ and $$$\mathbb{N}$$$, which means there are as many multiples of $$$3$$$ as there are of $$$2$$$ (which, on the face of it, is also perfectly reasonable). So now we have five subsets of $$$\mathbb{N}$$$ ($$$2\mathbb{N}$$$, $$$2\mathbb{N} - 1$$$, $$$3\mathbb{N}$$$, $$$3\mathbb{N} - 1$$$, and $$$3\mathbb{N} - 2$$$) that are
all the same size as $$$\mathbb{N}$$$. Aaargh!


And of course, there is no reason why we should be restricting
ourselves to just 2 and 3. This property applies to every single natural
number. In fact, it's clear that for every natural number $$$n$$$, there
exist $$$n$$$ wholly different subsets of $$$\mathbb{N}$$$ (call them
$$$n\mathbb{N}$$$, $$$n\mathbb{N} - 1$$$, $$$n\mathbb{N} - 2$$$, $$$n\mathbb{N} - 3$$$, $$$\ldots$$$, $$$n\mathbb{N} - (n - 1))$$$ which are all the same size as $$$\mathbb{N}$$$. To put it differently:

>$$$\mathbb{N}$$$ contains at least as many subsets that are as large as itself as there are elements in $$$\mathbb{N}$$$.

###To Infinity and Beyond!###

Since all of these insanely counterintuitive results follow from our
definition of counting, let us call a set <span style="font-variant:small-caps;">countable</span> if it has as many elements as a
subset of $$$\mathbb{N}$$$. Thus, all finite sets are countable (which clearly makes sense!). So are sets like the set $$$2\mathbb{N}$$$ of even numbers, and even something like the set of all numbers divisible by numbers of the form $$$p^{p}$$$, where $$$p$$$ is some prime number. 


Does that mean there are such things are uncountable sets? We will have
to wait and see!



