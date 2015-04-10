---
layout: post
title: DSU, SAC, conjugation, and all that
tagline: On a family of problem-solving techniques
---

It just struck me (in a dream, believe it or not!) that a number of patterns for solving problems all share an underlying metapattern, so to speak. I will illustrate a few of these patterns first, and then talk about the metapattern, which I will call *generalized conjugation* for reasons that will hopefully become apparent.

## Example 1: Python list sort ##
Python lists have a default ```sort()``` method, which applies the less-than operator ```<``` to the elements of the list to produce a sorted list. Thus, for instance:

{% gist 2092b8b43a7635d885a7 list_sort_no_key.py  %}

### Sorting, ignoring case ###
In Python 3.4, the ```sort()``` method takes a keyword-only argument which, according to the [Python 3.4 docs](https://docs.python.org/3/library/stdtypes.html?highlight=sort#list.sort), "is used to extract a comparison key from each list element (for example, ```key=str.lower```). 
The key corresponding to each item in the list is calculated once and then used for the entire sorting process."

This is mighty helpful. 
Consider the following situation: You have a list of strings, and you want to sort them. 
What happens if you simply call ```sort()``` on the list? 
It gets sorted in lexicographic order, of course. 
This means, however, that all the upper-case words will end up prior to all of the lower-case words (thanks to the ASCII values for these letters). 

If you want to ignore case, you will need to sort the list based on some other comparison key: 
in this case, the lower-case version of each word. And that can be achieved by using the ```str.lower``` function.

{% gist 2092b8b43a7635d885a7 list_sort_with_key_1.py  %}

### Sorting by length of string ###
What if you wanted to sort the list not in alphabetical order, but in order of string length? Well, 
the ```len``` function takes care of that!

{% gist 2092b8b43a7635d885a7 list_sort_with_key_2.py  %}

### A somewhat crazier example ###
But what if you wanted to sort a list of numbers based not on their numeric value, but on their names?
(I cannot think of any reason why you might want to do this, unless you need a contrived example to explain the ```sort()``` in Python, but we will let that pass for now!)
Remember, the ```key=``` argument takes a function of one argument which must return a "comparison key".
In our case, this custom function must take a number as input and return its name as output.
That situation will look something like the following (for brevity, I am only dealing with single-digit numbers, but the principle is straightforward):

{% gist 2092b8b43a7635d885a7 list_sort_with_key_3.py  %}

### "A *what*zian transform?" ###
In earlier versions of Python, this technique for sorting a list based on some other comparison keys was known as the DSU (for *D*ecorate-*S*ort-*U*ndecorate) pattern.
Wikipedia tells me that this idiom, when used in Perl, was called the [*Schwartzian transform*](http://en.wikipedia.org/wiki/Schwartzian_transform), which I must admit sounds way cooler.

DSU is not just an idiom any more in Python 3.4, because there is a language construct for handling it.
But it is really easy to implement the pattern in code:

{% gist 2092b8b43a7635d885a7 DSU_by_hand.py  %}

Isn't this amazing? That's how simple the whole process is!

(_Note:_ I'm glossing over a small subtlety here, which is that my hand-implemented DSU pattern does not in fact give the exact same result as the ```sort()``` with its key.
If you look at the effects of passing ```str.lower``` to the two functions, you'll notice that my DSU implementation inverts the order of the words ```"FOX"``` and ```"fox"```.
Can you guess why?
(_Hint:_ Where is the sorting actually happening in my DSU implementation?)
My implementation is thus *not* guaranteed to produce stable sorts.)

### A high-level picture ###
As the name "DSU" itself suggests, there are three steps that take place here:

1. *Decorating*: We take each element of the list we care about, and "decorate" it with the comparison key that we actually care about sorting.
   We do so by using a tuple of the element and its corresponding comparison key.
2. *Sorting*: We then sort the comparison keys.
   Because they are in a tuple, this automatically sorts the list we care about in the order that we care about.
3. *Undecorating*: We finally extract from each tuple just the element, and then collate all the elements together to get the sorted list.

From this perspective, it is clear that there are a number of things that can be generalized:

* I have hard-coded tuples as the method of decoration here, but it may be that different problems would call for other ways of decorating the original list.
* As a dual to the first, I have hard-coded my method of undecoration as well, but this would also have to change if we had a different method of decoration.
* I have hard-coded the middle step of sorting, by calling on Python's ```sort``` method, but we may well want to do something entirely different with a decorated list.
* Finally, I have hard-coded the assumption that we're working with a list, but we may very well want to work with all sorts of other data structures.

Now all of these could be handled with the appropriate code changes in Python.
We could, for instance, write something like the following:

{% gist 2092b8b43a7635d885a7 DSU_generalization.py  %}

But I want to turn to other examples of a similar problem-pattern first.

### Appendix: Sorting lists in Ruby ###

For those who prefer to write code in Ruby, most of the same principles apply.
Of course, since functions are not first-class in Ruby, we cannot pass a sorting function as a parameter to the sort method.
Instead, as might be expected, we can pass a block that tells us how to go about doing the comparison.

A few other differences emerge between Ruby and Python, which are really quite typical of the differences between the two languages:

* Ruby has two methods, ```sort``` and ```sort!```, where the former returns a new list that is sorted, while the latter returns the list sorted in-place.
  In contrast, the Python method ```sort``` sorts the list in-place *and* returns ```None```.
* The block passed into Ruby's ```sort``` / ```sort!``` must take two parameters, and must return -1, 0, or 1 depending on the result of the comparison.
  Python's ```sort```, on the other hand, can take an optional function as argument, but this has to be a single-parameter function that generates a comparison key for an element of the list.
* Ruby also has two additional methods, ```sort_by``` and ```sort_by!```, which do take a single-parameter block that works much like the Python ```sort```.
* Python ```sort``` can only be called on lists, while Ruby's ```sort``` / ```sort!``` and ```sort_by``` / ```sort_by!``` can be called on Enumerables in general.
  In this regard they are more like the Python ```sorted```.

(Perhaps this comparison really should be broken out into a separate post!!)

Ok, enough talk; here is Ruby code that does pretty much all the same things the Python code above did.
I have not added code to implement the Schwartzian transform by hand though.

{% gist 0b41add0846ec11943e6 %}

And with that, adieu for now. 
Next time, more examples of similar patterns of problem-solving.
