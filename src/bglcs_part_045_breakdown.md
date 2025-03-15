# Breaking Down Problems

[i[Breaking down problems]<]

> _"There's games beyond the game."_
>
> —Stringer Bell, _The Wire_

If the problem solving steps (_Understand_, _Plan_, _Code_, _Reflect_)
had a sequel, this chapter would be it.

Those steps really do get you through every problem, but it turns out
those problems exist as fractal problems within problems within
problems.

As an example, maybe you want to build a table. That's the entire
problem:

* Build a table

Well, that might not be enough if you haven't built a lot of
tables. So you break down the problem into dependent subproblems.

* Build a table
  * Attach legs to tabletop
    * Build tabletop
    * Build legs

And maybe that's not enough. How do you make legs? How do you make the
tabletop?

* Build a table
  * Attach legs to tabletop
    * Build tabletop
      * Sand table surface
        * Glue trim to top
          * Cut main top
            * Learn to use a table saw
          * Cut trim
    * Build legs
      * Cut legs
      * Turn legs on lathe
        * Learn to use a lathe

And so on. *We keep breaking down the problem until we get the step
small enough that we know we can accomplish it.*

When you're first starting out, you might have to boil the problem down
into single lines of code. [i[Experts]] Experienced devs often don't
have to break it down that far because they are well-versed in the
sub-steps.

For example, a carpenter with modest experience might only need to break
down building a table into our second set of steps, above, and not go
into such detail.

Like everything, breaking down a problem is a skill, and you get better
with practice.

When breaking down problems, think back to our earlier consideration:
"This problem would be easy if the input data were in _this_ form."
That's a hint that you should break out a subproblem that converts the
input data into that form, thus making the problem easy.

And once you have a subproblem, pretend that it's the entire problem,
just for a bit. Focus closely on it and see if you can solve it in
isolation. If not, ask yourself what would make it easy to solve, and
break that out into a subproblem.

Repeat.

The more you practice breaking down problems and coding solutions, the
better you'll get at it. Soon you won't have to break down problems
quite as far as you needed to before, and, like an [i[Experts]] expert,
you'll start recognizing patterns you can reuse.

However, it's not always obvious _how_ to break down a problem.

One technique is to imagine a physical manifestation of the thing you're
trying to code. (For example, you're writing a sort? Imagine a bunch of
alphabet blocks on a table and you have to sort them.)

And then, to push it farther, imagine that you're teaching a
non-technical friend how to solve it. How would you describe the steps?
The conditionals? When they're done?

If you can physically sort the books on your shelf (whatever "books"
are), you can write an algorithm to do that exact same thing. You just
need to break down the steps.

## Pseudocode

[i[Pseudocode]<]

One of the bigger tools that devs use to explore ideas is to write
pseudocode. This is "code for humans". Computers can't read it. (Though
some might argue that Python is pretty close to pseudocode.)

But you can use it to outline steps of an algorithm or process to do a
sanity check or just explore how you might get something done.

You could write some pseudocode to insert a value into an already-sorted
list of values.

``` {.default}
find correct spot in list
insert the value there
```

But that's not really descriptive enough. We might have to break it
down.

``` {.default}
find correct spot in list
    → find first entry larger than the new one
    
insert the value there
    → shift all the higher values to the right
    → insert the new value in the newly-opened spot
```

Getting there.


``` {.default}
find correct spot in list
    find first entry larger than the new one
        → loop through items, stop when you find a larger one
    
insert the value there
    shift all the higher values to the right
    insert the new value in the newly-opened spot
```

And now it's becoming a little clearer.


``` {.default}
find correct spot in list
    find first entry larger than the new one
        loop through items, stop when you find a larger one
        → record the index before it
    
insert the value there
    shift all the higher values to the right
    insert the new value in the newly-opened spot
        → set the list item at the index to the new value
```

And we're getting dangerously close to being able to translate our
pseudocode to real code. Maybe it's still unclear how we're going to
shift all the values to the right, and we should break that out a bit
more.

Sometimes devs add the pseudocode to their real code as comments and
implement the real code under them.

This is a powerful tool to use during the _Plan_ phase. It can really
help solidify your thinking on the overall process.

[i[Pseudocode]>]

## Proof of Concept

[i[Proof of concept]<]

What if you've broken down the bigger problem into smaller subproblems,
but you simply don't know if one of the things is even possible to do.

For example, "Can you render an image to an HTML canvas and then save
that image directly to the photo gallery on a mobile phone?" Maybe
you've never done that, and you don't know if the phone and web
technology even have that capability.

One sure way to find out is to code up a proof of concept.

So you make a web page, add a canvas, draw something distinctive on it,
like a rectangle, and then add the code to download it when a button is
pressed.

This used to involve a lot of reading books and, later, searching the
web. And it still often does. But more commonly now we lean on AI[^4914]
to answer the "is it possible and how" questions, and even come up with
some proof-of-concept code.

[^4914]: Again, if allowed in your work or school environment.

Once you have the code working, you know two things:

1. It works!
2. How to write the code to do it.

Usually the proof-of-concept code isn't production-ready, but forms the
core of what you'll eventually deliver.

Another use of proof-of-concept code is to demonstrate to people what
the finished product will look or how it will behave. Sometimes people
code up a mock implementation where only a small part of the UI is
operational but a viewer can get the gist of how the software will
eventually work.

Often the majority of the code you wrote up for the proof of concept
will be thrown away, and you might feel some resistance to discarding
that work. But don't worry about it. The important part of the
proof of concept is the knowledge gained while doing the work, not the
work itself.

[i[Proof of concept]>]

> _"Plan to throw one away; you will, anyhow."_
>
> —Fred Brooks, _The Mythical Man-Month_

[i[Breaking down problems]>]
