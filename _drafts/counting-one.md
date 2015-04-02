---
layout: post
title: On Counting
---

#On counting#

I've wanted to write about this for a while but never really got the chance. One of the coolest things about modern mathematics is infinity: we have found all sorts of ways to study and classify different notions of "size" and "number" that can result in the most counterintuitive results imaginable. I want to look at a few examples, starting today.


##Counting##

Let's begin with the natural numbers, the set $$\mathbb{N} = \{1, 2, 3, ... \}$$.

This is "clearly" an <span style="font-variant:small-caps;">infinite

 set, as indicated by the ellipsis. 
What does "infinite" mean in this case? 
Now we know that we can add natural numbers together to produce natural numbers; 
more simply, we can add the number $$1$$ to a natural number $$n$$ to produce a new natural number $$n + 1$$. $$\mathbb{N}$$ is infinite in the sense that there is simply no "end" to it, at least in one direction (because there is such a thing as the smallest natural number, which is $$1$$). To rephrase that, there is simply no way to list every single element of $$\mathbb{N}$$, whereas for any finite set, no matter how large it may be, you can eventually list out every element.


Before we go any further, let's actually get a handle of what counting means. In real life, when we have to count out a bunch of things, we essentially point at each item once (and only once) and call out the natural numbers in order. We are in effect uniquely indexing every item with one (and only one) of the natural numbers. There is nothing twisted or weird about this; this is the most "natural" (pardon the pun) way of counting things.

What this definition of counting allows us to do is to compare the size of different sets: we can know that a sack of three potatoes is the same numerical size as a sack of three apples because we can index both of them with the set $$\{1, 2, 3\}$$. (It should be clear that it does not matter
which potato we're pointing to when we call out a particular number; all
that matters that we point to each potato only once and we call out the
numbers in order only once.) Now so far this sounds like a ridiculously
overdone way of stating the utterly obvious (and I've not even pulled
out real mathematical terminology or notation!), but the utility of such
abstraction will become more and more evident as we journey along.

###Counting Finite Sets###

Take a finite subset of $$\mathbb{N}$$, say $$X = \{1, 2, ..., 100\}$$. We know that all natural numbers are either even or odd, so we can divide the
set $$X$$ into two halves ("partition" it into two), say $$A = \{1, 3,
5, ..., 99\}$$ and $$B = \{2, 4, ..., 100\}$$. 

Furthermore, we know that
these two sets are both the same size because they contain $$50$$ elements
each; in other words, we can go through the elements of $$A$$ saying
"one", "two", "three", and so on, and we'll eventually hit the number
"fifty", and the same is true for $$B$$ too. More formally, we can write
$$A = \{2k - 1 : k \in \{1, 2, ..., 50\} \}$$ and $$B = \{2k :
k \in \{1, 2, ..., 50\} \}$$, and then it's pretty clear that the two sets
are the same size as each other. And most importantly, we can also see
that $$A$$ and $$B$$ are each exactly *half* the size of $$X$$, which
also makes complete sense.



 Now let's take $$C = \{3, 6, 9, …, 99\}$$, $$D = \{2, 5, 8, …, 98\}$$,
and $$E = \{1, 4, 7, …, 97, 100\}$$. They are not all the same size,
because $$C$$ and $$D$$ both have $$33$$ elements while $$E$$ has $$34$$ elements, but it is true that they form a partition of $$X$$ and that
the total number of elements in them adds up to $$100$$, as should be the
case.



###Counting Infinite Sets###

Nothing new or exciting so far, so let's try something fancier. What
about the whole set of even numbers? (Lets call it $$2\mathbb{N}$$, for a reason that will soon become clear.) Clearly $$2\mathbb{N}$$ is a subset of $$\mathbb{N}$$.
Similarly,  the set of all odd numbers (let's call it $$2\mathbb{N} - 1$$, but let's not actually think of that as some sort of subtraction) is a
subset of $$\mathbb{N}$$. 

Clearly, there is no number that $$2\mathbb{N}$$ and $$2\mathbb{N} - 1$$ both have in common. What's more, $$2\mathbb{N}$$ and $$2\mathbb{N} - 1$$ together account for all the natural numbers. In other words, it seems intuitive to say that $$\mathbb{N}$$ is exactly "twice" as large as $$2\mathbb{N}$$, right? After all, that's exactly what we saw with $$X$$ and $$A$$ and $$B$$ above.

Wrong. 

####Multiples of $$2$$###
In fact, $$2\mathbb{N}$$ is exactly the same size as $$\mathbb{N}$$, and $$2\mathbb{N} - 1$$ is exactly the same size as $$\mathbb{N}$$ as well. How on earth can this be true? This simply makes no sense! If this result doesn't shock you, it should. To paraphrase [Niels Bohr's remark about quantum
mechanics](http://en.wikiquote.org/wiki/Quantum_mechanics), "those who
are not shocked when they first come across infinity cannot possibly
have understood it." 


Let's go back to our definition of counting. If we go through the list
of even numbers, we can uniquely assign to each and every even number
one and exactly one natural number; similarly, if we go through the list
of natural numbers, we can uniquely assign to each and every natural
number one and exactly one natural number. (How do we do this? We can
index every even number $$x$$ using the natural number $$\frac{x}{2}$$; we can also index every natural number $$n$$ using the even number 2$$n$$.) But if there exists a unique element of one set that uniquely corresponds to a
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

####Multiples of $$3$$###
But wait, it gets worse. Take the set of multiples of $$3$$ and call it
$$3\mathbb{N}$$ (perhaps you can now see where I'm going with this?). It's clear that there is a bijection between $$3\mathbb{N}$$ and $$\mathbb{N}$$, which means there are as many multiples of $$3$$ as there are of $$2$$ (which, on the face of it, is also perfectly reasonable). So now we have five subsets of $$\mathbb{N}$$ ($$2\mathbb{N}$$, $$2\mathbb{N} - 1$$, $$3\mathbb{N}$$, $$3\mathbb{N} - 1$$, and $$3\mathbb{N} - 2$$) that are
all the same size as $$\mathbb{N}$$. Aaargh!


And of course, there is no reason why we should be restricting
ourselves to just 2 and 3. This property applies to every single natural
number. In fact, it's clear that for every natural number $$n$$, there
exist $$n$$ wholly different subsets of $$\mathbb{N}$$ (call them
$$n\mathbb{N}$$, $$n\mathbb{N} - 1$$, $$n\mathbb{N} - 2$$, $$n\mathbb{N} - 3$$, $$\ldots$$, $$n\mathbb{N} - (n - 1))$$ which are all the same size as $$\mathbb{N}$$. To put it differently:

>$$\mathbb{N}$$ contains at least as many subsets that are as large as itself as there are elements in $$\mathbb{N}$$.

###To Infinity and Beyond!###

Since all of these insanely counterintuitive results follow from our
definition of counting, let us call a set <span style="font-variant:small-caps;">countable

 if it has as many elements as a
subset of $$\mathbb{N}$$. Thus, all finite sets are countable (which clearly makes sense!). So are sets like the set $$2\mathbb{N}$$ of even numbers, and even something like the set of all numbers divisible by numbers of the form $$p^{p}$$, where $$p$$ is some prime number. 


Does that mean there are such things are uncountable sets? We will have
to wait and see!


###Extending countability###

Having looked at the definition of countability and the natural numbers $$\mathbb{N}$$, it is but natural (no pun intended) to ask how far this concept can be extended. The natural numbers are pretty awesome, after all, but there are a huge number of things you can't do with natural numbers, including something as basic as subtraction.

####The Integers####

The only operations under which $$\mathbb{N}$$ is closed are addition (that is, you can add two natural numbers and the result will be a natural number) and multiplication, but the latter is pretty limited in the sense that it's basically just repeated addition. So all we can do with natural numbers is "go forth and multiply"; there is no way to reduce them. In other words, there is no "inverse" operation to addition under which $$\mathbb{N}$$ is closed.



So let's define the integers, traditionally noted by $$\mathbb{Z}$$ (from the German *zahlen*, to count), as an extension of the natural numbers that is closed under subtraction. (Technically $$\mathbb{Z}$$ is a group under the operation of addition.) Among other things, this means zero is in $$\mathbb{Z}$$, so that you have an "identity element", something that you can add to any number while keeping it the same. This also means that you have "additive inverses", something you can add to a number to produce zero.


More simply put, $$\mathbb{Z} = {\ldots, -2, -1, 0, 1, 2, \ldots}$$. It is infinite in two directions, so to speak. Now intuition would suggest that this means $$\mathbb{Z}$$ is bigger than $$\mathbb{N}$$, *n'est-ce pas*? Except that our earlier exploration of countability should suggest that our intuitions cannot always be relied upon when it comes to the infinite.

A different intuition—call this the intuition of the mathematician, if you will—would suggest that the even numbers $$2\mathbb{N}$$, despite missing every second number of $$\mathbb{N}$$, are nevertheless of the same size as $$\mathbb{N}$$, meaning that you can essentially "double" the size of a countably infinite set and get another countably infinite set. And since $$\mathbb{Z}$$ is essentially $$\mathbb{N}$$ "doubled", it should also be countably infinite!


How can we be certain about this? Just to make things a little more mathematically convenient, let's take a slightly different set, the whole numbers $$\mathbb{W}$$ = {0, 1, …}. Now clearly $$\mathbb{W}$$ is countably infinite because there is a bijection between $$\mathbb{W}$$ and $$\mathbb{N}$$ (given any whole number $$\mathbb{w}$$, you can index it using the natural number $$\mathbb{w}$$ + 1; given any natural number $$\mathbb{n}$$, you can index it using the whole number $$\mathbb{n}$$ - 1). What we shall do is show that there is a bijection between $$\mathbb{Z}$$ and $$\mathbb{W}$$, which automatically means that there is a bijection between $$\mathbb{Z}$$ and $$\mathbb{N}$$. So what can this bijection be?


Very conveniently for us, we can see that both sets can be neatly divided into three different subsets:


+ The first is $$\mathbb{W}$$, which is the union of the set consisting of the single element 0 (let's call it <b>0</b> = {0}), the even numbers ($$2\mathbb{N}$$, as we called them last time), and the odd numbers ($$2\mathbb{N}$$ - 1). In set notation, $$\mathbb{W}$$ = <b>0</b> ∪ $$2\mathbb{N}$$ ∪ ($$2\mathbb{N}$$ - 1).
+ $$\mathbb{Z}$$ is the union of <b>0</b>, the positive integers (that is to say, $$\mathbb{N}$$), and the negative integers (call them $$\mathbb{N}_{-}$$). In set notation, $$\mathbb{Z}$$ = <b>0</b> ∪ $$\mathbb{N} \cup \mathbb{N}_{-}$$.


We already know that the four lettered sets are all countably infinite, so all we need to do to build a bijection between $$\mathbb{Z}$$ and $$\mathbb{W}$$ is to do the following:


<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">
<ul>
<li>

Given an integer $$z$$  (in mathematical notation, $$z  \in \mathbb{Z}$$, which is read as "*z* is an element of $$\mathbb{Z}$$"):

</li>
<ul>
<li>

If $$\mathbb{z}$$ = 0, index it to the whole number 0. (For now, let's think of the two 0s as being different, just as a matter of convenience. We can call them $$0_\mathbb{Z}$$

 and $$0_\mathbb{W}$$

 if you want. So if $$\mathbb{z}$$ = 



 

$$0_\mathbb{Z}$$

, then index it using 



 

$$0_\mathbb{W}$$

.)

</li>
<li>

If $$\mathbb{z}$$ is a positive integer ($$\mathbb{z}  \in \mathbb{N}$$), then index it to the even number 2$$\mathbb{z}$$. Note that this clearly maps all positive integers $$\mathbb{N}$$ to all even numbers $$2\mathbb{N}$$.

</li>
<li>

If $$\mathbb{z}$$ is a negative integer ($$\mathbb{z}  \in \mathbb{N}$$_), then index it to the odd number 2 |$$\mathbb{z}$$| - 1. Note that we've used the absolute value function here in order to strip away the negative sign of $$\mathbb{z}$$ and to produce a positive number instead. This way we are guaranteed to get a result that belongs to the set $$2\mathbb{N}$$ - 1.

</li>
</ul>
<li>

And for the reverse process, given a whole number $$\mathbb{w}  \in \mathbb{W}$$:

</li>
<ul>
<li>

If $$\mathbb{w}$$ = 
$$0_\mathbb{W}$$

, then index it using the integer 
$$0_\mathbb{Z}$$
.

</li>
<li>

If $$\mathbb{w}$$ is an even number ($$\mathbb{w}  \in 2\mathbb{N}$$), then map it to the positive integer $$\mathbb{w}$$ / 2. (Because $$\mathbb{w}$$ is even, it can be divided by two to produce an even number.)

</li>
<li>

If $$\mathbb{w}$$ is an odd number ($$\mathbb{w}  \in 2\mathbb{N}$$ - 1), then map it to the negative integer (-1)($$\mathbb{w}$$ + 1) / 2. (Multiplying by -1 guarantees us that we will produce a negative number, and then the other parts of the definition guarantee that this will be a negative integer.)

</li>
</ul>
</ul>
</div>

This is a little more complicated than the procedure for showing that the even numbers are countably infinite, but it is even more satisfying! This also tells us something interesting: we can essentially "double" the size of a countably infinite set and still stay countably infinite. This in turn suggests that we can "multiply" the size of a countably infinite set by any finite number and still stay countably infinite. But what happens if we try something more ambitious?

 *Rational numbers*
With the integers, we can now perform addition (and subtraction), but we still cannot divide two arbitrary integers and expect to get an integer. So we expand the set of integers $$\mathbb{Z}$$ to create the set of rational numbers $$\mathbb{Q}$$, formally defined as $$\mathbb{Q}$$ = {$$\mathbb{p}$$/$$\mathbb{q}$$ | $$\mathbb{p}$$, $$\mathbb{q}  \in \mathbb{Z}$$ and $$\mathbb{q}$$ ≠ 0 and $$\mathbb{p}$$, $$\mathbb{q}$$ are in lowest terms}. This is the standard mathematical notation for a set, and is to be read thus: $$\mathbb{Q}$$ is the set of all fractions $$\frac{p}{q}$$ [*p* being the numerator and *q* the denominator, of course] such that both *p* and *q* are elements of the set of integers $$\mathbb{Z}$$, and *q* does not equal 0, and *p* and *q* do not share any multiplicative factors in common (i.e., you can't simplify them any more). The "such that" sign, which is the vertical bar '|', is sometimes replaced by the colon ':'.


This set $$\mathbb{Q}$$ clearly contains far more numbers than $$\mathbb{Z}$$. We can clearly see this if we look at a number line. Whereas the points that represent the integers are separate and visibly far from one another, the rational numbers are not. They are "densely" clustered on the line, limitlessly packed so close that between any two rational numbers we can always find a third rational number (essentially, if you have $$\mathbb{a} \in \mathbb{b}  \in \mathbb{Q}$$, then ($$\mathbb{a} + \mathbb{b}$$) / 2 ∈ $$\mathbb{Q}$$ clearly, and furthermore it lies between $$\mathbb{a}$$ and $$\mathbb{b}$$). We are now surely at a stage where we have a set larger than $$\mathbb{N}$$.


Alas, our intuition fails us once again. As it turns out, $$\mathbb{Q}$$ is also countably infinite; in other words, there exists a bijection between $$\mathbb{N}$$ and $$\mathbb{Q}$$.


But what on earth is this bijection? How do you create a bijection between one set and another that is, in some sense, the first set "squared"? The answer is tremendously simple to see, although my inability to draw an image will make it rather tricky to represent it in words.


For convenience's sake, let us only consider the subset 

$$\mathbb{Q}$$_{+}$$

 = {$$\mathbb{p}$$ /* q* | $$\mathbb{p}$$, $$\mathbb{q}  \in \mathbb{N}$$ and $$\mathbb{q}$$ ≠ 0 and $$\mathbb{p}$$, $$\mathbb{q}$$ are in lowest terms}. This excludes half of the rational numbers, but that is really not a problem as we have seen before; if we can prove that 

$$\mathbb{Q}_{+}$$

 is countably infinite, then it won't be hard to "double" that property to all of $$\mathbb{Q}$$. Since every rational number can be represented as the ratio of two integers, we can write them (theoretically, if we had an infinite amount of time and nothing better to do!) in a table whose columns and rows are indexed by the natural numbers. Our table should look something like




1/1, 2/1, 3/1, 4/1, …




1/2, 2/2, 3/2, 4/2, …




1/3, 2/3, 3/3, 4/3, …




1/4, 2/4, 3/4, 4/4, …




and so on. It should be evident that every positive rational number from 

$$\mathbb{Q}_{+}$$

 is on this list (and in fact, more than once; after all, 1/1, 2/2, 3/3, and so on all represent the same number, the rational number 1). Since we have an infinite amount of time, we decide to scratch out all the numbers that are represented more than once, thus leaving holes in our table:


<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">
</div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">


1/1, 2/1, 3/1, 4/1, …

</div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">


1/2, 

 

xx  , 3/2, 

 

xx  , …

</div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">


1/3, 2/3, 

 

xx  , 4/3, …

</div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">


1/4, 

 

xx  , 3/4, 

 

xx  , …

</div>


Now comes the fun part. Imagine drawing a curve that starts from 1/1 and then zigs and zags through this square: 1/1, 2/1, 1/2, 3/1, 1/3, 4/1, 3/2, 2/3, 1/4, … and so on. (This is where the image would have been really useful; if you like, it sort of resembles the diagram that illustrates the *Aufbau* principle that is used to describe the order in which atomic orbitals are named.) If we now index each point with a natural number in sequence, we will have created a bijection (loosely speaking) between $$\mathbb{Q}_{+}$$ and $$\mathbb{N}$$. In other words, we will have successfully enumerated all the rational numbers using the natural numbers, and vice-versa.


Thus, even though the rational numbers contain so many numbers that are not natural numbers (consider the fact that just between 0 and 1, you have all the numbers 1/2, 1/3, 1/4, and so on, which themselves form a countably infinite set), they are still exactly the same size as the natural numbers.
 *Irrationality and madness*
It would only be rational (no pun intended) to decide at this point that our definition of infinity is good enough for all purposes, and that this is the "largest" that a set can be. But mathematicians are usually gripped by a certain kind of madness: the desire to abstract and to generalize, to push properties to see just how far they can go before collapsing under their own nonsensicality.


In our case, for instance, it turns out that there are a lot of numbers that are just not expressible as rational numbers. The most famous of these numbers is of course the ratio of the circumference of a circle to its diameter, represented by the Greek letter π. Another famous example is √2, about which it is said that the Pythagorean cult in ancient Greece jealously hid the proof of its irrationality because their metaphysics would collapse under such madness. Yet another example is the number $$\mathbb{e}$$ that shows up just about everywhere in the universe. How many such numbers are there after all? And do we really need them?


As it turns out, we really do need them, for what seems like an obscure mathematical reason. $$\mathbb{Q}$$ is very useful because it is well-behaved when it comes to all four major operations (addition, subtraction, multiplication, and division)—in mathematical terms, $$\mathbb{Q}$$ is called a "field". However, $$\mathbb{Q}$$ has one major deficiency: you can have sequences of rational numbers that do not converge to a rational number.


What on earth does that mean? And why does that matter?

</div>  </div>

<div dir="ltr" style="text-align: left;" trbidi="on">
<div dir="ltr" style="text-align: left;" trbidi="on">
 *Sequences and convergence*
We saw earlier that the rational numbers $$\mathbb{Q}$$ are much more versatile than the natural numbers $$\mathbb{N}$$ for doing a wide variety of mathematical operations. However, there is still one thing the rational numbers cannot do adequately: it is possible to construct sequences of rational numbers that do not converge to a rational number. In formal terms, the rational numbers are not *complete*.


Why does this seemingly obscure mathematical quirk matter? Because this is the foundation of calculus. The ideas of sequences and limits are fundamental to calculus, and if such limits don't exist meaningfully, then neither does calculus. But there is another, intuitive reason for why completeness matters.  <!--more-->


Take the sequence {1, 1/2, 1/3, 1/4, …}. It should be intuitively obvious that this set of numbers is getting smaller and smaller, and that although it does not contain the value 0, it is inexorably heading towards it. But if you take a sequence like {1, 1.4, 1.41, 1.414, 1.4142, …}, then we "know" intuitively that this sequence converges to the number √2, which we have proven to be irrational. This suggests that there are lots of "holes" in the set of rational numbers, making them incomplete and even discontinuous, in an intuitive sense. (In terms of topology, this intuition is expressed by the idea that the rational numbers are *totally disconnected*, which roughly means that between every two rational numbers there is at least one irrational number, so that if we tried to walk along the number of rational numbers, we would be forced to jump constantly from one rational number to another.)


When we faced similar problems with $$\mathbb{N}$$ and with $$\mathbb{Z}$$, we extended them by adding all sorts of missing numbers. We can do the same thing now with $$\mathbb{Q}$$, extending it to the set of real numbers $$\mathbb{R}$$, although the mathematical details are not very pretty. The usual non-rigorous method is say that rational numbers have decimal expansions that are either terminating (like 0.3158) or at least repeating (like 0.333... for 1/3), whereas irrational numbers have non-terminating, non-repeating decimal expansions (like 1.4142… for √2). (For those who don't have queasy stomachs, there are at least three different ways of constructing $$\mathbb{R}$$ that are often taught: the easy way by constructing equivalence classes of Cauchy sequences of rational numbers, the standard way by constructing Dedekind cuts, and the coolest way—at least in my book—by continued fractions.)


These details don't really matter; the twofold point is that we can construct the set of real numbers $$\mathbb{R}$$ so that it is *complete* (i.e., doesn't have any "holes" the way $$\mathbb{Q}$$ does) and that we have a nice decimal representation for every real number. (In formal terms, *completeness* can be described in a few different ways, one way being that every sequence of real numbers whose terms get closer and closer to each other—every Cauchy sequence, to be precise—will eventually converge to a real number.) To return now to our initial question: how large is $$\mathbb{R}$$?
 *Cantor's Diagonalization Proof*
By now, all our intuitions about comparing the sizes of sets have been utterly trashed. We no longer really have a good intuition for how large $$\mathbb{R}$$ must be, and it would be entirely forgivable to suppose that $$\mathbb{R}$$ is also countably infinite, just like $$\mathbb{N}$$. We would be utterly wrong.


The mathematician Georg Cantor offered a beautiful proof of the uncountability of $$\mathbb{R}$$ using the idea of *diagonalization*. The full-blown version of the proof is a bit tricky, as always, but here I will sketch out a proof of the fact that there are in fact *far more* irrational numbers between just 0 and 1 than there are natural numbers in their entirety. (Clearly, if this is true, then all of $$\mathbb{R}$$ must also be strictly larger than all of $$\mathbb{N}$$.)


As with <a href="http://pearlsatrandomstrung.blogspot.com/2011/01/one-proof-that-square-root-of-2-is.html">our proof of the irrationality of √2</a>, we will achieve this by contradiction. So let us suppose that the irrational numbers between 0 and 1 are countable; that is, we can enumerate them in a list indexed by the natural numbers $$\mathbb{N}$$. Now, since we know that irrational numbers have non-terminating, non-repeating decimal expansions, we simply go ahead and write down all the irrational numbers in a list, which would look something like this:




1—0.

<b>

5

</b>

48574930…




2—0.3

<b>

5

</b>

3495364…




3—0.57

<b>

9

</b>

473594…




4—0.123

<b>

5

</b>

34967…




5—0.4328

<b>

7

</b>

4239…




6—0.54941

<b>

2

</b>

390…




and so on. This is possible because we have supposed that the irrational numbers are countable.


Here is where the *diagonalization* part comes in. We now essentially have a table of numbers that comprises of all the digits of all the irrational numbers between 0 and 1. So now, let's take a separate, infinitely long piece of paper, and let's walk down the diagonal of the table, writing down the first digit of the first number, the second digit of the second number, …, the *i

</i><sup>

th

</sup>

 digit of the *i

</i><sup>

th

</sup>

 number, … until infinity. (We're assuming we have an infinite amount of time, so this doesn't matter! Gotta love math.) So based on the table we have up here, we will have the number (let's call it $$\mathbb{x}$$) 0.559572…


We then take a second infinitely long piece of paper and copy down the digits of $$\mathbb{x}$$, with one key difference: we add 1 to every digit after the decimal point. (As a convention, we can suppose that if $$\mathbb{x}$$ contains a 9 somewhere, then we write down 0 instead, but this is just really a minor thing.) Let's call this new number $$\mathbb{y}$$; in our case this is going to be the number 0.660681…


So what's so great about what we've done so far? Here is the kicker, the awesome punchline, the crazy part: $$\mathbb{y}$$ is an irrational number that is not part of our list at all!


<ul style="text-align: left;">
<li> *y* is irrational because it is non-terminating and non-repeating. This may not be obvious right at the start, because it is of course possible to imagine that we somehow randomly happen to pick an infinite number of numbers which set up an infinite diagonal of 9s, which would then make the decimal expansion of $$\mathbb{y}$$ contain an infinite number of 0s and thus terminate. However, if this happens, then we can quite easily reorder our original list so that our diagonal is no longer comprised of 9s. (Remember that when we count, it does not matter which particular element gets indexed to which natural number; the only thing that matters is that it can be done. So such a reordering is totally legitimate.)

</li>
<li> *y* is not on our list because, well, it differs from every number on our list at one position, at the very least! This is the neat part: we have consciously constructed $$\mathbb{y}$$ so that the *i

</i><sup>

th

</sup>

 digit of $$\mathbb{y}$$ is different from the *i

</i><sup>

th

</sup>

 digit of the *i

</i><sup>

th

</sup>

 number on our list.

</li>
</ul>


What this means, more simply, is that our initial supposition—that we can enumerate the irrational numbers between 0 and 1—is false. No matter how many irrational numbers we count off against the natural numbers, there will always be more. The set of irrational numbers between 0 and 1 must therefore be strictly *larger* than the whole set of natural numbers $$\mathbb{N}$$ or integers $$\mathbb{Z}$$ or rational numbers $$\mathbb{Q}$$ (which are all the same size, as we have already seen). Just imagine that: between just two numbers—the smallest gap there is in the integers!—lie more numbers than are encompassed by all of the rational numbers! This fact should blow your mind.
 *Uncountable Sets*
But wait! There is more. Let us now define one more mathematical term: the *open interval* ($$\mathbb{a}$$, $$\mathbb{b}$$), which is sometimes written as ]$$\mathbb{a}$$, $$\mathbb{b}$$[ to avoid ambiguity, is the set of all real numbers $$\mathbb{x}$$ that lie between $$\mathbb{a}$$ and $$\mathbb{b}$$ but are not equal to them. In formal mathematical notation, ($$\mathbb{a}$$, $$\mathbb{b}$$) = {$$\mathbb{x}  \in \mathbb{R}$$ | *a *&lt; $$\mathbb{x}$$ &lt; $$\mathbb{b}$$}. So, using this notation, we can say that we just proved that the size of the set of irrational numbers in the open interval $$(0, 1)$$ is strictly larger than the size of the set of natural numbers. (Just so we are clear, the open interval $$(0, 1)$$ contains all the *real* numbers between 0 and 1, which means it contains all the irrational numbers *and* all the rational numbers between 0 and 1.)


Just as we looked first at the natural numbers $$\mathbb{N}$$ and then compared them to the even numbers $$2\mathbb{N}$$, we can now look at a subinterval of the open interval $$(0, 1)$$ and see how it stacks up in size with the bigger interval. Let's take the open interval $$(0, 1/2)$$. This is clearly half as "long" as the open interval $$(0, 1)$$—but does it contain "half" as many elements?


Now that we are talking about sets strictly larger than $$\mathbb{N}$$, we can no longer establish size by naïvely counting all the elements. However, we can certainly use the formalized intuition of counting that we have developed, which is to say, the idea of the bijection. In other words, we can still compare the size of two sets by checking to see if it possible to construct a way to uniquely map every element of one set to exactly one unique element of the other, and vice versa.


There is a very simple bijection between $$(0, 1/2)$$ and $$(0, 1)$$:


<ul style="text-align: left;">
<li>

We can map any $$\mathbb{x}$$ in the interval $$(0, 1/2)$$ to the number 2$$\mathbb{x}$$, which is clearly in the interval $$(0, 1)$$,

</li>
<li>

We can map any $$\mathbb{y}$$ in the interval $$(0, 1)$$ to the number $$\mathbb{y}$$ / 2, which is clearly in the interval $$(0, 1/2)$$.

</li>
</ul>


In other words, the open interval $$(0, 1/2)$$ is "just as large" as the open interval $$(0, 1)$$. And furthermore, our intuition should now suggest to us that there was nothing special about picking the interval $$(0, 1/2)$$; in fact, *every open interval *($$\mathbb{a}$$, $$\mathbb{b}$$) is "just as large" as $$(0, 1)$$:


<ul style="text-align: left;">
<li>

Given any $$\mathbb{x}$$ in the interval $$(0, 1)$$, we can map it to the number $$\mathbb{a}$$ + ($$\mathbb{b}$$ - $$\mathbb{a}$$)$$\mathbb{x}$$, which must lie precisely inside the interval ($$\mathbb{a}$$, $$\mathbb{b}$$).

</li>
<li>

Given any $$\mathbb{y}$$ in the interval ($$\mathbb{a}$$, $$\mathbb{b}$$), we can map it to the number (*y - a*) / (*b - a*), which must lie inside the interval $$(0, 1)$$.

</li>
</ul>


Another way to think about this is that the whole real line is really nothing more than the open interval $$(0, 1)$$ suitably stretched out (or compressed), and hence is just the same size. This should give us a sense of how truly large the size of the real numbers is: we can take as tiny an interval of real numbers as we like, and we will still have more real numbers inside that interval than there are natural numbers. Yet another way to think about it is that every rational number is separated from every other rational number by as many real numbers as there are on the entire real line as a whole. If this does not blow your mind, nothing can.

</div>  </div>


<div dir="ltr" style="text-align: left;" trbidi="on">
<script src="https://d3eoax9i5htok0.cloudfront.net/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript">
</script>


<div dir="ltr" style="text-align: left;" trbidi="on">


I’d been completely side-tracked from this set of posts, and I only just realized I had forgotten to finish it. Last time we checked, we had finally figured out that there are different levels of infinity. We had, however, ended up with a rather strange idea: the idea that the set of all real numbers between 0 and 1 is somehow as big as the set of all real numbers in its entirely. In effect, we have shown that there is no difference between a mountain and a molehill!


We thus have two different lines of inquiry to pursue:


<ol style="text-align: left;">
<li>

Are there levels of infinity beyond the infinity of the real numbers?

</li>
<li>

Are there ways to measure the size of a set that can distinguish mountains from molehills?

</li>
</ol>
 *Levels of infinity*
We begin with the idea of a *power set*: the power set of a set is defined as the set of all subsets of the set. Huh? An example should make things clearer: if $$ A = \{ a, b, c \} $$



, then the power set of $$ A $$, sometimes written as $$ \mathcal{P}(A) $$ and sometimes $$ 2^{A} $$



 (we’ll see why), is the set $$ \mathcal{P}(A) = \{ \{ a \}, \{ b \}, \{ c \}, \{ a, b \}, \{ b, c \}, \{ a, c \}, \{ a, b, c \}, \{ \}  \} $$.



 All those braces are necessary, because every *element* of $$ \mathcal{P}(A) $$ is a *subset* (and not an *element*) of $$ A $$ itself. We note that $$ A $$ itself is an element of $$ \mathcal{P}(A) $$, as is the empty set $$ \{ \} $$.



<!--more-->Now it is fairly easy to show that if $$ A $$ is a finite set of cardinality $$ n $$ 



(written $$ | A | = n $$ 



), then the cardinality of the power set of A is $$ 2^{n} $$*. *More picturesquely, $$ | 2^{A} | = 2^{| A |} $$



.


Why? Well, let’s count the number of subsets of size $$ k $$<i> </i>



for every number less than or equal to 



$$ n $$



:



<ul style="text-align: left;">
<li>

For 



$$ k = 0 $$: There is exactly one subset of $$ A $$ with zero elements, and that is the empty set

</li>
<li>

For 



$$ k = 1 $$: There are $$ n $$ subsets with one element each

</li>
<li>

For 



$$ k = 2$$: There are $$ \binom{n}{2} $$ 



subsets with two elements (where I am using one of many different notations to represent combinations. More on them elsewhere)

</li>
</ul>



… and so on.




When we add them all up, we somehow magically (a.k.a. the Binomial Theorem!) get $$ 2^n $$



! Quite magical (not).


This is all very cute, of course, but what happens when $$ A $$ is not finite? What happens when we take, say $$ \mathbb{N} $$



, as our set? What, in other words, is $$ 2^{\mathbb{N}} $$



?


We know that for any finite number 



$$ n $$, 



$$ 2^n &gt; n $$



. One of the neat things about Cantor’s diagonalization theorem is that it tells us this is true for any $$ n $$—



including infinite 



$$ n $$



! How?


We recall that we had earlier defined “counting” as establishing a bijective correspondence between two sets. This is how we proved that $$ \mathbb{N} $$



 and $$ 2 \mathbb{N} $$ 



were, in fact, the same “size”. So to prove that $$ A $$ and $$ \mathcal{P}(A) $$

<i> <sup>

 

</sup>*are not, in fact, the same size, we must show that *no* correspondence between them can be bijective. And if we can show that no matter what correspondence we take, there is always some element of 



$$ \mathcal{P}(A) $$



 



which gets left out even while every single element of $$ A $$ is accounted for, then we can prove that 



$$ \mathcal{P}(A) $$

<i> <sup>

 

</sup>*is, in fact, bigger than $$ A $$.


We begin by noting that 



$$ \mathcal{P}(A) $$ 



is at least as large as $$ A $$. This is true because there is a bijection between $$ A $$ and the elements of 



$$ \mathcal{P}(A) $$
that are all single-element subsets of $$ A $$. (In symbols, the collection $$ \{ a, b, c \} $$



 has a bijective correspondence with $$ \{ \{ a \}, \{ b \}, \{ c \} \} $$



.) Now consider any function $$\mathbb{f}$$ that maps an element of $$ A $$ to an element of 



$$ \mathcal{P}(A) $$



. We need to show that there is at least one element of 



$$ \mathcal{P}(A) $$ 



that cannot be in $$ A $$ (and let us constantly remind ourselves that an *element* of 



$$ \mathcal{P}(A) $$ 



is a *subset* of $$ A $$ ). How can we find such an element of 



$$ \mathcal{P}(A) $$ 



that does not depend on the particular definition of a correspondence $$ f $$?


This is the step in the diagonalization process analogous to picking one digit from every number on the list and modifying it in order to create a new number. But how do we do that with sets? We note that the correspondence $$ f $$ 



connects every element $$ x \in A$$ 



with an element 



$$ f(x) \in \mathcal{P}(A) $$



 



; i.e., with a subset of $$ A $$. Depending on how we define our correspondence



, it may be the case that $$ x $$ 



is actually an element of the subset that it maps to; or it may be the case that $$ x $$ 



is *not* an element of the subset it maps to. Clever devils that we are, we pick our element of 



$$ \mathcal{P}(A) $$ to be the set $$ B $$ of all those elements of $$ A $$ which *are not* elements of the subset they correspond to. (This is like changing the digit we pick so we know our new number differs from every existing number in at least one place.) In symbols, $$ B = \{ x \in A | x \notin f(x) \} $$



.


How do we know that there is no element of $$ A $$ that can be mapped to $$ B $$ by $$ f $$



 Why, by the very definition of $$ B $$



 itself! Suppose, for the sake of contradiction, that there does exist a $$ y \in A $$



 such that $$ f(y) = B $$



. By the definition of $$ B $$, this must mean that $$ y \notin B $$



. But then by the definition of $$ B $$, we have $$ y \in B $$



! This is a clear contradiction, which shows that there simply cannot be any such $$ y $$



. In other words, 



$$ \mathcal{P}(A) $$ 



is always larger than $$ A $$—regardless of whether $$ A $$ has finitely many elements or not!


Thus, 



$$ 2^{\mathbb{N}} $$ 



must needs be greater than $$ \mathbb{N} $$ 



in size. But we also know, through a different diagonalization proof, that $$ \mathbb{R} $$ 



is greater than $$ \mathbb{N} $$ 



in size. Is it in fact true that $$ \mathbb{R} = 2^{\mathbb{N}} $$?



 



As it turns out, this question is better answered by taking $$ \mathbb{Q} $$ 



rather than $$ \mathbb{N} $$ (



but as we saw earlier, these two sets are the same size, and so it doesn’t really matter). And the answer, which I will not go into in any detail, is yes. When we construct real numbers by the method of Dedekind cuts, we do in fact map every real number to a subset of $$ \mathbb{Q} $$



. The converse can also be shown to be true.


But regardless, the power set argument shows that there *have* to be infinities greater than the uncountable set of the real numbers. The power set of the real numbers, 



$$ \mathcal{P}(\mathbb{R}) $$,



 is strictly larger than $$ \mathbb{R} $$, and its own power set $$ \mathcal{P}(\mathcal{P}(\mathbb{R})) = 2^{2^{\mathbb{R}}}$$ 



is larger still, and so on, *ad infinitum*! (A more concrete example of a set that is of cardinality $$ 2^{\mathbb{R}} $$ 



is the set of all functions from $$ \mathbb{R} $$ 



to $$ \mathbb{R} $$



.)


<i> *</div>
</div>


<div dir="ltr" style="text-align: left;" trbidi="on">
<script src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript">
</script>


<div dir="ltr" style="text-align: left;" trbidi="on">


Alright, so now we finally know that there isn’t one infinity any more. In fact, there is an infinite number of infinities, each infinitely larger than the one smaller than it, and so on upwards. *Excelsior* is a good motto for the infinitude of infinities (as it is for the Coat of Arms of the State of New York).


<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;"><div class="separator" style="clear: both; text-align: center;">
<a href="http://upload.wikimedia.org/wikipedia/commons/6/61/Coat_of_Arms_of_New_York.svg" imageanchor="1" style="margin-left: 1em; margin-right: 1em;">

<img border="0" src="http://upload.wikimedia.org/wikipedia/commons/6/61/Coat_of_Arms_of_New_York.svg" height="307" width="320" />

</a></div>
But we haven’t dealt with another problem: this way of measuring the size of a set just isn’t good enough for our purposes. We need something more refined, something that does distinguish between countable and uncountable while also capturing common-sense notions of the “length” of a line, the “area” of a sheet of paper, the “volume” of a hill, and so on. This is exactly what is studied in the branch of mathematics known as <i>measure theory</i>.

</div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">




</div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">
 *

</i>
<!--more--> *Measuring mountains and molehills

</i></div>

<div>


Now a *measure* is basically a rule (a function) that assigns to a set a number (this being the <i>measure of the set</i>), in a manner that follows certain common-sensical restrictions. The two most important of these restrictions are:

</div>
<ul style="text-align: left;">
<li>

the measure of a set has to be greater than or equal to 0. This is sort of obvious—we don't want areas and lengths to be negative! [It is also not entirely obvious—there are certain other cases where we do want “signed” areas and volumes. This comes into play when dealing with such things as differential forms, integration on manifolds, and all that. But that’s another post for another time!]

</li>
<li>

if a set can be separated into non-overlapping subsets, then the measure of the set equals the sum of the measures of the subsets. So for instance, the measure of the interval $$(0, 1)$$ must equal the sum of the  measures of the interval $$ (0, \frac{1}{2}) $$, the single-point set $$ \{ \frac{1}{2} \} $$, and the interval $$ (\frac{1}{2}, 1) $$.

</li>
</ul>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">


[Technical note: strictly speaking, a measure is not defined on a set but a $$ \sigma $$-algebra<i> </i>over the set, i.e., on a special collection of subsets of the set that satisfy a few important properties. Since this special collection of subsets always includes the set itself, it is not hugely wrong to say that the measure is defined on the set. There are some technical reasons for defining the measure on a 



 $$ \sigma $$-algebra



 over the set rather than on the set itself, but these rise from certain pathological complications that sometimes make it impossible to define the measure of *every* single subset of a set. Using the 



 $$ \sigma $$-algebra



 restricts us to dealing with the measures only of a certain collection of subsets of the set, but in practice this is virtually never a problem since pretty much every conceivably useful subset of $$ \mathbb{R} $$ can be assigned a consistent and meaningful measure.]

</div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">  </div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">


As can be imagined, there are many different measures that can be defined on one set. One example is the so-called <i>counting measure</i>, which assigns to a finite set $$ A $$ the number of elements in it, and to an infinite set (whether countable or uncountable) the symbol $$ \infty $$. Another extremely important example is the <i>Lebesgue measure</i>, which is defined over virtually all “useful subsets” of $$ \mathbb{R} $$ and which preserves our common-sense notion of length.

</div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">
</div>
<ul style="text-align: left;">
<li>

The Lebesgue measure of isolated points is zero (and hence of any countable set of isolated points); in other words, any set for which the counting measure is not $$ \infty $$ has Lebesgue measure zero.

</li>
<li>

The Lebesgue measure of a closed interval $$ [a, b] $$ is defined as $$ b-a $$. Again, this preserves our common-sense notion of length.

</li>
<li>

The Lebesgue measure of a closed rectangle $$ [a,b] \times [c,d] $$ in the plane $$ \mathbb{R}^2 $$  is $$ (b-a) \cdot (c-d) $$, which again accords with our common-sense notion of area. The same principle generalizes to higher-dimensional closed structures.

</li>
</ul>


Using Lebesgue measure thus immediately allows us to distinguish mountains from molehills—even if they both have the same cardinality. 


Lebesgue measure is the foundation of the <i>Lebesgue integral</i>, the standard theoretical integral of integration that is taught in higher mathematics, much more powerful than the <i>Riemann </i>(or <i>Cauchy ) 

integral</i> introduced (but seldom labeled as such) in high school calculus. The fact that it is usually cloaked behind an impenetrable veil of mathematical jargon means that the beauty of Lebesgue integration is usually not at all apparent to the casual reader. Perhaps at some point in the near future I will attempt to explain the need for more and more complicated definitions of integration.


<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">  </div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">




</div>
</div>
</div>
<div dir="ltr" style="text-align: left;" trbidi="on">
<script src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript">
</script>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">


Let’s quickly recap of some of the interesting things we have seen so far.

</div>
</div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">
<ul style="text-align: left;">
<li>

The real numbers are uncountable, and in fact every interval of the real numbers is uncountable. In other words, there are more real numbers between 0 and 1 than there are integers from negative infinity to positive infinity. 

</li>
<ul>
<li>

However, this alone does not really give us a sense of just how much bigger uncountable is than countable. For instance, we can see that the sequence of fractional numbers $$ \{ 1, \frac{1}{2}, \frac{1}{3}, \frac{1}{4}, \ldots \} $$ is also contained within the interval $$(0, 1)$$. It is clear, though, that this sequence has the cardinality of $$ \mathbb{N} $$. It is thus not really clear how it is so remarkable that there are more real numbers in $$(0, 1)$$ than there are natural numbers anywhere at all.

</li>
</ul>
<li>

The Lebesgue measure of an isolated point is zero. Consequently, the Lebesgue measure of a countable number of isolated points is also zero. In particular, the Lebesgue measure of $$ \mathbb{N} $$, the natural numbers, is zero.

</li>
<ul>
<li>

But what if we take an uncountable number of isolated points? Wait, is that even possible?

</li>
<li>

And what if we take “non-isolated” points, whatever that means?

</li>
</ul>
</ul>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">  <!--more-->

Well, let’s begin by defining what it means to be an “isolated” point. We “know” intuitively that the points of $$ \mathbb{N} $$ are “isolated” when considered as a subset of the real numbers $$ \mathbb{R} $$. On the other hand, a set like $$ \mathbb{R} $$ itself is “dense”, which is the opposite of isolated. What does this mean? Formally, we define the notion of “denseness” in terms of a set (call it $$ X $$ ) and a subset of that set (call it $$ A $$ ). In this case, we say the subset $$ A $$ is *dense* in $$ X $$ if *every* point of $$ X $$ is either a point in $$ A $$ itself or arbitrarily close to a point in $$ A $$. What this intuitively means is that there is no getting away from points of $$ A $$ when we are inside $$ X $$; no matter where we go in $$ X $$ and no matter how tightly we try to close ourselves away, there will always be a point from $$ A $$ near us. 

</div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">




</div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">


It’s pretty clear that $$ \mathbb{N} $$ doesn’t fit this definition, because the points are all separate from each and equally spaced out over the real numbers. In this case, we say $$ \mathbb{N} $$ is <i>nowhere dense</i> in $$ \mathbb{R} $$. Surprisingly, denseness is true of the rational numbers! $$ \mathbb{Q} $$ is dense in $$ \mathbb{R} $$, even though it has “as many” elements as $$ \mathbb{N} $$. In other words, even though $$ \mathbb{Q} $$ and $$ \mathbb{N} $$ are both countable, their spatial arrangements (or more formally, their <i>topological structures</i>) are different, giving them different properties. We thus see that a countable set can be either dense in $$ \mathbb{R} $$ or nowhere dense in $$ \mathbb{R} $$.

</div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">




</div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">


It’s worth noting two features about nowhere dense sets:

</div>
<ul style="text-align: left;">
<li>

By one definition, a subset $$ A $$ is <i>nowhere dense</i> in a set $$ X $$ if the *closure* of $$ A $$ in $$ X $$ has an empty *interior*. As a reminder:

</li>
<ul>
<li>

The *closure* of $$ A $$ in $$ X $$ is the set of all those points in $$ X $$ that are limits of sequences of points taken only from $$ A $$. It should be immediately clear that the closure of $$ A $$ always includes $$ A $$, but may often include lots of other points too. Thus, the closure of $$ \mathbb{Q} $$ in $$ \mathbb{R} $$ is $$ \mathbb{R} $$ itself, which is clearly much larger than $$ \mathbb{Q} $$. In some intuitive sense, the closure of a set is a more “natural”, “self-contained” version of the set.

</li>
<li>

The *interior* of 



$$ A $$ is the set of all those points strictly, properly within 



$$ A $$ itself; i.e., for every point in the interior of $$ A $$, it should be possible to establish some sort of exclusive zone around it that contains points only within



 



$$ A $$ itself. So, for instance, the point 



 



$$ \frac{1}{2} $$ is an interior point of the interval 



 



$$ [0, 1] $$, but neither  

 



$$ 0 $$ 



 nor 



 



$$ 1 $$ are. Another example: the interior of 



$$ \mathbb{Q} $$ is the empty set (because you can always find some irrational number that is really close to every rational number, no matter how much you decide to “zoom in”).

</li>
</ul>
<li>

The complement in 



 



$$ X $$ of a nowhere dense subset 



 



$$ A $$ is a dense, open set.

</li>
</ul>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">


[Strictly speaking, $$ X $$ cannot be any regular set; it must be a <i>topological space</i>, a kind of set in which it is possible to talk about ideas such as being connected, being continuous, being “near” or “far” in a loose sense.]

</div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">




</div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">


So to summarize, we have four different things here:

</div>
<ul style="text-align: left;">
<li>

the *cardinality* of a set, according to which the natural numbers $$ \mathbb{N} $$ and the rational numbers $$ \mathbb{Q} $$ are *countable* but the real numbers $$ \mathbb{R} $$ are *uncountable*;

</li>
<li>

the <i>counting measure</i> of a set, according to which $$ \mathbb{N} $$, $$ \mathbb{Q} $$, and $$ \mathbb{R} $$ are all infinite

</li>
<li>

the <i>Lebesgue measure</i> of a set, according to which both $$ \mathbb{N} $$ and $$ \mathbb{Q} $$ are sets of measure zero, $$ \mathbb{R} $$ has infinite Lebesgue measure, and any closed interval $$ [a,b] $$ has the finite measure $$ b-a $$.

</li>
<li>

the *denseness* of a set in another set, according to which $$ \mathbb{N} $$ is <i>nowhere dense</i> in $$ \mathbb{R} $$, but $$ \mathbb{Q} $$ is *dense* in $$ \mathbb{R} $$.

</li>
</ul>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">


Now, it would be natural to think that an *uncountable* set has to be dense, simply because there are so many more points in it (uncountably more, in fact!) than in a countable set. As it turns out, that’s not the case. This is where the <i>Cantor set</i> and other similar structures, sometimes whimsically called the <i>“fat” Cantor sets</i> (more formally, the Smith-Volterra-Cantor sets), come in.

</div>


<div dir="ltr" style="text-align: left;" trbidi="on">
<script src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript">
</script>


The word “dust” <a href="http://pearlsatrandomstrung.blogspot.com/2011/01/counting-uncounting-and-dust-part-one.html">has</a> <a href="http://pearlsatrandomstrung.blogspot.com/2011/01/counting-uncounting-and-dust-part-two.html">appeared</a> in the <a href="http://pearlsatrandomstrung.blogspot.com/2011/01/counting-uncounting-and-dust-part-three.html">title</a> of <a href="http://pearlsatrandomstrung.blogspot.com/2011/08/counting-uncounting-and-dust-part-four.html">every</a> <a href="http://pearlsatrandomstrung.blogspot.com/2012/05/counting-uncounting-and-dust-part-five.html">post</a> in this <a href="http://pearlsatrandomstrung.blogspot.com/2012/05/counting-uncounting-and-dust-part-six.html">series</a>, and we will finally begin to see why. Many counterintuitive marvels remain to be unmasked in the counterintuitive worlds of cardinality and measure theory. Georg Ferdinand Ludwig Philipp Cantor, the mathematician who laid the foundations for the modern understanding of infinity, was responsible for the discovery of some of these truly unbelievable marvels.


<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">




</div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">


There seems to be a whole sub-genre of math blog posts that focus on defining or presenting the Cantor set at different levels of rigor! For our purposes, I will offer two descriptions (without proof). 

</div>
</div>
<div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">
</div>
<ul style="text-align: left;">
<li>

The Cantor set can be described quite “simply” as the set of all real numbers between 0 and 1 whose ternary representation contains only 0 and 2. (We use the *decimal* place value system in everyday life, while computers use the *binary*, using only 0 and 1.) The *ternary* place value system uses 0, 1, and 2 as the only digits. So the number 0.1 in ternary represents the fraction $$ \frac{1}{3} $$, and 0.22 the fraction $$ \frac{8}{9} $$, and so on. It is also worth noting that just as we take the decimal 0.999… to be equal to the number 1, we must also take the ternary number 0.0222… to be equal to the ternary number 0.1, and so on.

</li>
<li>

The Cantor set can also be seen as the limit of an infinite process of cutting up the *closed* interval $$ [0, 1] $$. The rule is simple: at every stage, delete the middle third (*excluding* the endpoints) of every remaining interval. Repeat <i>ad infinitum</i>. The first few stages of such a process are shown in this picture.

</li>
</ul>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">
</div>
</div>
<div class="separator" style="clear: both; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px; text-align: center;">
<a href="http://1.bp.blogspot.com/_9SocnJ7K2Pc/TFCC5kvQADI/AAAAAAAAAL4/PtWEP2HPtRU/s1600/Cantor+Set.gif" imageanchor="1" style="margin-left: 1em; margin-right: 1em;">

<img border="0" src="http://1.bp.blogspot.com/_9SocnJ7K2Pc/TFCC5kvQADI/AAAAAAAAAL4/PtWEP2HPtRU/s320/Cantor+Set.gif" height="171" style="cursor: move;" width="320" />

</a></div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">


How does the Cantor set measure up (pun intended) using our four different definitions of size?</div>
<ul style="text-align: left;">
<li>

Its <i>counting measure</i> is infinite. This is quite easy to see with the ternary representations: there is a very obvious bijective correspondence between $$ \mathbb{N} $$ and subset $$ {0.2, 0.22, 0.222, ...} $$ (in ternary representation). Since this subset is infinite in terms of counting measure, the whole Cantor set itself must also be infinite by this measure.

</li>
<li>

In terms of *cardinality*, it is *uncountable*. This is not obvious at all. However, it can be proven by constructing a *surjective* map from the Cantor set to $$ [0, 1] $$. (There are clever ways to do this, but setting one up and showing that it is in fact surjective is probably a little too detailed for now.) This will show that the Cantor set has at least the same cardinality as $$ [0, 1] $$. Since it’s also a proper subset of $$ [0, 1] $$, it cannot have a cardinality greater than $$ [0, 1] $$. Therefore, it has the same cardinality as $$ [0, 1] $$; i.e., it is uncountable.

</li>
<li>

Its <i>Lebesgue measure</i> is zero. To see this, we begin by noting that the Lebesgue measure of $$ [0, 1] $$ is 1. We then add up the Lebesgue measure of each of the *deleted* subintervals: $$ \frac{1}{3} + 2 \frac{1}{3^2} + 2^2 \frac{1}{3^3} + ... $$. (It is not immediately obvious that adding up an infinite sum of Lebesgue measures is a legitimate procedure: infinities can be a nasty thing. However, because none of the deleted intervals overlap in any way, the addition process ends up being legitimate.) This infinite sum is the geometric series $$ \frac{1}{3} \Sigma_{i=0}^{\infty} \left( \frac{2}{3} \right)^i $$, which evaluates to exactly 1. Thus, the Cantor set has Lebesgue measure zero!

</li>
<li>

It is <i>nowhere dense</i> in $$ [0, 1] $$. How does that make sense? 

</li>
<ul>
<li>

Well, for one, the Cantor set is a *closed* set in 



$$ [0, 1] $$. One way to see this is to “intuit” (or to formally prove) that every sequence of numbers in the Cantor set converges to some point in the Cantor set. (It’s easier to “see” this if you think about our description of the Cantor set in terms of numbers with ternary representations containing only 0 and 2.) Another way is to remember that the complement in 



$$ [0, 1] $$ of the Cantor set is a countable union of open intervals. Since this complement is open, the Cantor set itself must be closed in  

 



$$ [0, 1] $$.



 (This is of course false for $$ \mathbb{Q} $$.) 

</li>
<li>

But like $$ \mathbb{Q} $$, it’s also true that for any number in the Cantor set, there will always be some number from $$ [0, 1] $$ arbitrarily close to it that does not belong to it. Thus, the *interior* of the Cantor set is empty. By definition, a <i>nowhere dense</i> set is one the interior of whose closure is empty; and so we see that the Cantor set is nowhere dense in 
$$ [0, 1] $$.

</li>
<li>

And as a cross-check, the complement of the Cantor set in $$ [0, 1] $$ is both open (since it’s a countable union of open intervals) and dense in $$ [0, 1] $$ (because, well, it includes almost all of $$ [0, 1] $$ anyway, and for those points that it doesn’t contain (i.e., for the points belonging to the Cantor set), it’s possible to get arbitrarily close to them!

</li>
</ul>
</ul>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">
</div>
<div style="margin-bottom: 0px; margin-left: 0px; margin-right: 0px; margin-top: 0px;">


Thus, the Cantor set is a remarkable beast: 
uncountable, nowhere dense, and Lebesgue measure zero. 


But there are even cooler sets, known as the “fat” Cantor sets, or more formally as the Smith-Volterra-Cantor sets. Like the Cantor set, these are uncountable and nowhere dense; unlike the Cantor set, they have *positive* Lebesgue measure. Indeed, it’s possible to define fat Cantor sets with Lebesgue measure as close to 1 as we want!


When we constructed the Cantor set by removing one-third of each interval at each step, we were in a sense removing as much as we could if we wanted to keep our intervals equal in length at each step. We could, however, remove *less* than one-third. If, for instance, we removed the central one-sixth of each interval at each step, we would end up removing a total length of $$ \frac{1}{6} + 2 \frac{1}{6^2} + 4 \frac{1}{6^3} + ... = \frac{1}{4} $$. This gives us a set of measure $$ \frac{3}{4} $$.


In general, if we remove $$ x^n $$ from each interval on the $$ n^{\text{th}} $$ step, we will end up with a fat Cantor set of Lebesgue measure $$ \frac{1-3x}{1-2x} $$. When $$ x = \frac{1}{3} $$, we get the “regular” Cantor set of measure zero; and clearly $$ \lim_{x \to \infty} \frac{1-3x}{1-2x} = 1 $$. Ta-da!


<i>Why “dust”?</i>


I’ll wrap this all up with one quick remark: why “dust”? The answer is: there ain’t no good answer. There are higher-dimension analogs of the Cantor set which retain its strange properties of nowhere denseness and Lebesgue measure zero. Approximate visual representations of these beautiful fractals resemble stationary clouds of dust just hanging out there in a cube, spread out around it but taking up no space at all. Stunningly beautiful.




</div>
</div>
