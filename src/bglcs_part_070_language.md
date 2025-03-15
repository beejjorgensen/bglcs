# Learning a New Language

The first language you learn is the hardest. Not only are you learning
the language, but you're also learning the _concepts_ that are used
within the language. By concepts, I mean things like how to organize
functions and pass arguments, how to run loops, how to do conditionals,
etc.

All languages have these same concepts (more or less—more on that
later), and so learning the second language is just learning how to
apply those same concepts you already know.

It's like if you already know Spanish, learning Italian isn't that big
of a jump.

This chapter is about learning additional languages after you've learned
your first one. This is important because you're going to be learning
new languages your entire career. Luckily, though, learning new
languages it itself a skill, and the more new languages you learn, the
easier it becomes.

There are two big pieces to learning a new language in a paradigm
you already know (procedural, object-oriented, functional, etc.)

1. **Learn the syntax**. Like `if` and `while`, and how to declare
   variables and functions, etc.

2. **Learn the standard library**. This is the built-in functionality
   that you can take advantage of, like reading and writing a file, or
   printing to the screen, or connecting to a web server.

Learning the syntax is often the easier of the two. Most languages have
relatively simple syntax.

By analogy, you can learn what verbs, nouns, and adjectives are, and how
to [flw[diagram sentences|Sentence_diagram]]. But that's not enough to
write a masterful literary work. You also need to know what words you
have at your disposal.

And that's the more complex part. Many standard libraries have a *lot*
of built-in functionality. [fl[Scroll through the Python standard
library for an example|https://docs.python.org/3/library/index.html]].

## Learning the Syntax

Jump right in! Follow a tutorial and write "toy" programs. These are
programs that just exercise some aspect of the language.

How do we do conditionals in Rust? Let's write a toy program to check it
out.

``` {.rs}
fn main() {
    if (1 == 2) {
        println!("Something is horribly wrong.");
    } else {
        println!("That's correct.");
    }
}
```

Wait—are those parens necessary around the `if`?

``` {.default}
$ rustc foo.c
  warning: unnecessary parentheses around `if` condition
```

No, they aren't! It's a toy program; we're just using it to learn.

To learn all the necessary syntax, take the concepts you already know
and look up how to apply them in the new language.

* The main function
* Variables
* Conditionals
* Loops
* Classes
* etc.

It will be frustrating to you at first because you have to look up
every. Single. Thing. Like with a new human language, you know
conceptually that you want to go to the supermarket, but you have to
look up all those Italian words if you don't know Italian.

The good news is that the syntax of a computer language is *way* simpler
than a human language. And you can get it down pretty quickly.

## Learning the Library

The standard library is the pre-baked functionality that ships with a
language. It's nice because you know everyone who has the language
installed has all these functions already and they don't have to
download any additional third-party dependencies.

But you need to be familiar with that language's standard library so
that you know what the language can do out of the box, and so that you
don't reinvent the wheel when you don't have to.

One recommendation is the skim the standard library for a language
you're using. You don't have to know exactly how to use Python's
[flw[IMAP|Internet_Message_Access_Protocol]] functionality, but knowing
it's there in case you do is very valuable. At the very least, it lets
you know that Python is a contender for choice of language if you need
to do some IMAP work.

Then when you do need some of that functionality, you can dig into the
documentation and examples and see how it works.

I tend to learn libraries piecemeal, learning in detail only what I need
to get a job done. I know the rest of what it _can_ do (because I
skimmed the docs), but I only know bits and pieces well enough to code
with them.

And that's okay, since the libraries are massive, and it's unlikely
you're going to achieve mastery of everything in them. You just need to
be able to learn what you need to complete your work.

## Learning a New Paradigm

First, what is a _programming paradigm_? It's a way of modeling a
problem so that you can come up with a solution. I know that's vague but
bear with me for a couple paragraphs.

Imagine doing your taxes. (Sorry.) When you do them, it's a sequence of
steps one after another. Fill in your name. Fill in your income. If your
income is more than some value, do _x_. Else do _y_. It's a procedure
that you're following. You can model it as a series of steps.

Imaging you're simulating a 3D fantasy world. In that world you might
have a type of creature called an orc, and there might be many creatures
of that type running around. And they all have their own independent
coordinates, and their own [flw[hit
points|Health_(game_terminology)#Hit_points]], but they all have the
same behavior when you walk up to them. You can model them as a
collection of objects that are independent but have similar behavior.

These are two different ways of solving a problem, either by modeling
them as a sequence of steps, or as objects.

We call these differing models _programming paradigms_. The first
example is "procedural programming" (kind-of; I'm hand-waving a bit),
and the second is "object-oriented programming".

There are [flw[a lot of paradigms|Programming_paradigm]], but the Big
Three are procedural, object-oriented, and functional.

Here's the bummer: learning a new paradigm is hard. A lot harder than
just learning another language in the same paradigm.

If you know Spanish, learning Italian is relatively easy. But learning
Chinese, that's something else! Not nearly as easy. Keeping with the
analogy, it's a different paradigm. You have to learn new techniques and
concepts you might not even be aware of from the romance languages.

> **I learned Erlang a while ago**. [fl[Erlang|https://www.erlang.org/]]
> is a functional language, and I was weak with the functional paradigm.
>
> For example, in Erlang, once you set a "variable", you can never
> change it. And every single way I knew for modeling problems involved
> changing variables!
>
> I mean, how are you supposed to get _anything_ done if you can't
> change a variable?!
>
> But clearly, massive systems had been implemented successfully in
> Erlang, so there was a way. But I had to change my thinking about how
> I modeled problems, and learning that new way was a significant
> challenge.

My main piece of advice here is to use a _lot_ of examples to see how
that language performs basic tasks. That is, gather and study a lot of
toy programs.

Then come up with related challenges (or find some online, or ask an AI
to generate some) that allow you to work out to build your skills and
find gaps in your understanding.
