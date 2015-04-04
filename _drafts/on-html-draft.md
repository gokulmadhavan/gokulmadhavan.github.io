---
layout: post
category : web
tagline: "Thinking through the tools of the web"
tags : [intro, speculation, beginner, html, css, js, jquery, tutorial]
---
{% include JB/setup %}

What goes into a website? How does one go from an idea in the mind to a page on the intertubes that can be read by the whole world?
In the process of setting up this blog, getting a handle on Twitter Bootstrap, and plotting out a series of future posts, I have found myself thinking a lot about the ways in which our current "standards" for the web (HTML, CSS, and JavaScript) interact with one another and with the content, and about some of the challenges I face in using them to translate my thoughts to the web.

Since these thoughts have been brewing for a while now, I figured I might as well put my thoughts down in writing.
(This has the added benefit of allowing me to put off writing my dissertation!)

## Limitations of the present exercise ##
I fully acknowledge that HTML, CSS, and JavaScript have all achieved their present forms after long, intense debates among experts of various stripes, and thus there are likely good reasons for why they work the way they do.
I also fully realize that many of the issues that I will bring up can be addressed within these tools---indeed, this flexibility is part of the reason why these tools are so amazing.
And I also acknowledge that I am not, in fact, proposing concrete solutions to the problems I'll be raising.

These are limitations, to be sure, but none of them should invalidate the exercise itself.
It is a sign of a tradition's vitality for it to be able to sustain critiques from the inside (and make no mistake, these tools, with all of their historical baggage and opinionated views of the world, constitute a tradition).
Identifying gaps in the tool-tradition (often identifiable precisely because the tradition acknowledges them in a way and addresses them in some way or the other) helps us realize what our tools privilege.
And having a clear sense of these gaps is the first step towards fixing them, after all.

But enough with the preliminaries, and on with the show!

## A sample page ##
Let us dive into things right away.
Consider the following passage:

> Let's talk about websites. 
> A website is the child of the marriage of four components: content, its organization, its presentation, and its responses to various stimuli. 
> The first of these components is usually textual matter, although a rapidly increasing proportion of content is audio and/or visual in nature. 
> The second is expressed a markup language like HTML.
> The third is usually captured in CSS.
> The fourth is coded up in programming languages like JavaScript, often assisted by specific libraries like jQuery.
> What is tricky about this marriage is that (like any marriage) all the four components interact with one another, and can in certain cases alter one another.

How would we go about presenting this passage as a website?

### What, exactly, is the content here? ###
The content of this passage would seem to be straightforward: it's just a paragraph, right?
We can just wrap this between the `<p>` and `</p>` tags and be done, right?

It really isn't quite so straightforward as that. It isn't really obvious that this is a paragraph.
Ok sure, it is *typeset* as a paragraph, which is to say that it is typeset as a single unit of text in which the sentences flow after one another.

### Grammatical Markup ###
But there is no reason we should constrain ourselves to thinking about this in *typographical* terms.
We could, for instance, think of this in terms of sentences, which are both typographical units and grammatical units:

> `<p> <sentence>`Let's talk about websites.`</sentence>`
>
> `<sentence>`A website is the child of the marriage of four components: content, its organization, its presentation, and its responses to various stimuli. `</sentence>`
>
> `<sentence>`The first of these components is usually textual matter, although a rapidly increasing proportion of content is audio and/or visual in nature. `</sentence>`
>
> `<sentence>`The second is expressed a markup language like HTML.`</sentence>`
>
> `<sentence>`The third is usually captured in CSS.`</sentence>`
>
> `<sentence>`The fourth is coded up in programming languages like JavaScript, often assisted by specific libraries like jQuery.`</sentence>`
>
> `<sentence>`What is tricky about this marriage is that (like any marriage) all the four components interact with one another, and can in certain cases alter one another.`</sentence> </p>`

Indeed, we could get even deeper into the grammatical thicket, and identify all the components of each sentence: we could mark different types of grammatical clauses, tag different words as being certain kinds of parts of speech, and so on.
We could imagine using tags like `<clause>` and `<pos type='preposition'>` to do so.

This structure is, of course, inherent in the passage: it is a well-known fact that English sentences (and indeed sentences in any language) are structured hierarchies.
This *grammatical* organization is thus an essential part of the content of the passage.
Without it, the passage would just be word-soup.
However, since this grammatical structure is parsed beautifully and relatively effortlessly in our heads, we don't typically include that in our web markup.

### Lectional Markup ###
There are yet other ways this passage could be marked up.
We could focus on the *lectional* properties of this passage, for instance.
This would be intended to help the reader correctly enunciate stresses, pauses, and intonation.
Because English punctuation is designed to indicate many such features, lectional markup may often overlap with typographical markup, and in turn with grammatical markup as well.
However, there are often subtle differences in the length of time that we pause for different commas, and there are also important differences in word- and syllable-level stresses that are only rarely indicated in English typography.
Sometimes these alterations can dramatically alter the meaning of a passage---in which case they surely count as part of its content, no?

Let's try marking up a part of the passage we have above for both grammatical and for lectional structure.
To contrast between them, I will use HTML-style angular brackets for grammatical tags and parentheses for lectional tags.
It should go without saying that both of these markups are *extremely* rudimentary, and are meant to be suggestive rather than definitive.

> `<p> <sentence>` A website `(pause length='3' /)` is the child of the marriage of `(stress level='high')` four `(/stress)` components: `(stress level='medium')` content `(/stress)`, `(pause length='5' /)` its `(stress level='medium')` organization `(/stress)`, `(pause length='5' /)` its `(stress level='medium')` presentation `(/stress)`, `(pause length='5' /)` and its `(stress level='medium')` responses `(/stress)` to various stimuli. `(pause length='7' /) </sentence>`
>
> $$\ldots$$
>
> `<sentence>` What is `(stress)` tricky `(/stress)` about this marriage is that `(intonation level='stage-whisper')` (like any marriage) `(/intonation)` all the four components interact with one another, `(pause length='4' /)` and can `(pause length='2' /)` in certain cases `(pause length='2' /)` alter one another. `</sentence> </p>`

With this sort of passage, whose content is fairly obvious technical or factual information, we are not likely to see major clashes in such markup.
However, with other sorts of readings---particularly poetry---there may be real collisions among these different levels of markup.

#### A (much) harder example ####
Consider the following famous lines, which constitute a single grammatical sentence, from Tennyson's [*Ulysses*](http://www.bartleby.com/42/635.html):

> Yet all experience is an arch wherethro'
>
> Gleams that untravell'd world, whose margin fades
>
> For ever and for ever when I move.

The poem is composed in iambic pentameter, which means that every line is supposed to have ten syllables, with the even syllables stressed and the odd syllables unstressed.
However, if we were to blindly impose such a stress pattern on these lines, we would get no stress on "Gleams" and a stress on "that"---say it out loud for yourself, and watch yourself wince with the unnaturality of such a pattern!
Let's go ahead and annotate this with all three kinds of markup: typographical [brackets], grammatical <angles>, and lectional (parentheses).

> `<sentence> [line] <clause type='main'>` Yet `(pause duration='0' /)` `(stress level='10')` all `(/stress)` ex`(stress level='8')`pe`(/stress)`rience is `(pause duration='0' /)` an `(pause duration='0' /)` `(stress level='8')` arch `(/stress)` `</clause>` `<clause type='relative essential'>` wherethro' `(pause duration='0' /) [/line]`
>
> `[line] (stress level='9')` Gleams `(/stress)` that `(pause duration='0'/) (stress level='6')`un`(/stress)(stress level='8')`tra`(/stress)`vell'd world, `<clause type='relative inessential'>`whose `(stress level='7')`mar`(/stress)`gin `(stress level='5')` fades `(/stress) [/line]`
>
> `[line]` For `(stress level='5')`ev`(/stress)`er and for `(stress level='5')`ev`(/stress)`er `(pause duration='3') (intonation type='fade-to-silence')` when I move. `(/intonation) </clause> </clause> [/line] </sentence>`

Now that's well-nigh incomprehensible, so you may want to listen to this utterly stunning recitation of the poem by Sir Lewis Casson instead:

<iframe width="420" height="315" src="https://www.youtube.com/embed/hY4TuheKUbQ" frameborder="0" allowfullscreen></iframe>

### The first challenge ###
If you actually tried to read the three types of markup on that sentence, though, you may have noticed a very interesting feature:
*Not all types of markup forms a tree.*
In this example, for instance, the intonational and the typographical markup criss-cross, with neither cleanly forming a subset of the other.
In other lines in the same poem, the intonation and the grammatical markup may clash---strange as that might sound.
Those clashes and dissonances are part of what makes this superlative poetry.

Why does this matter? Because, as is drilled into all of us from Day Zero of working with webtools, the Document Object Model which is the heart of web rendering structures pages into trees.
Well-formed HTML markup is required to be in the form of a tree.
You cannot, simply cannot, have HTML tags that criss-cross.
This means, in effect, that *some kinds of combinations of markup cannot be rendered appropriately by HTML*.


