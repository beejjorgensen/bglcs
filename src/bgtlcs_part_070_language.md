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

Follow a tutorial and write "toy" programs. These are programs that just
exercise some aspect of the language.

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

One recommendation is the skim the standard library for a language
you're using. You don't have to know exactly how to use Python's
[flw[IMAP|Internet_Message_Access_Protocol]] library, but knowing it's
there in case you do is very valuable. At the very least, it lets you
know that Python is a contender for choice of language if you need to do
some IMAP work.

TODO

## Learning a New Paradigm

TODO

