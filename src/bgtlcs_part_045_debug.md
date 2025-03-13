# Debugging

Before we begin, the best way to debug a program is to not have bugs to
begin with. Though we're only human and we'll certainly mak mstakes,
<!-- sic --> the best way to avoid bugs in the first place is to adhere
to the problem solving framework. Remember that the programming battle
is in the _Understand_ and _Plan_ phases. The more completely and
correctly you complete those phases, the fewer bugs you'll have when
coding it up.

That said, let's talk about what to do when the inevitable happens.

## Mental Model

This is one of the most important things about being a developer: *have
a mental model of computation*.

That is, you should be able to read code and know what's going to
happen.

``` {.python}
def foo(n):
    i = 0

    while i < n:
        i = i + 1 + (i % 2)

    print(i)

foo(5)
```

Read the nonsense Python code, above. Mentally compute the output. Then
see if you're right. (I wrote the code, and it still took me a solid
minute to mentally model the answer. But I was right!)

***If you cannot "run" the code in your head, you cannot debug.*** Yes,
I'm going that strong. I'm sure some people disagree with me, but I want
to drive home how important this is.

*Debugging is the art of finding the part of the code where your mental
model of the computation and the reality of the computation diverge.*
And then fixing it.

If you don't have a mental model, you don't have anything to compare
against and you'll make little progress.

*Study code*! Trace through it. Try to understand how it works before
you run it. This is a skill that you can improve with practice.

## Finding the Bug

There is a bug somewhere. You know that because when you give your code
some input, and it cranks away at it, eventually it gives you unexpected
output.

Somewhere in that big process the reality of the computation diverges
from your mental model of the computation.

At first, all you might know is that somewhere in 10,000 lines of code
something went wrong. So you've narrowed it down to that. Your mental
model said that if the input was `2`, the output would be `3490`. And
instead the output was `299792458`.

Therefore you know the bug is somewhere between the input and the
output.

You _could_ just start changing random things in the code to see if it
gets fixed. This is sometimes called _shotgun debugging_ or _prayer
debugging_, and it very, very, very, very, *very* rarely works. Way more
often you'll just mess things up and make the problem even harder to
find. It's like trying to fix your car's electrical issues by randomly
adding and cutting wires. It's not even worth debugging this way.

And yet despite that, it's a very common technique practiced by
students worldwide. You, however, should not use it.

Instead, it's time to be systematic. Somewhere in that pipeline of
computation the intermediate computed values diverge from your mental
model. Your job is to find out where.

So you start probing _inside_ the program at various points to see
where things go off the rails. Binary search is great—jump to the middle
of the process and examine the values during a run (see below). If they
are as expected, the bug must therefore be between the middle of the
program and the end! You've just halved your search space. Now do it
again until you narrow it down far enough to see the bug.

I would contend, though some might disagree, *the bug is not found until
you understand it*. That is, you **must** understand exactly how your
program was giving the output `299792458` instead of the expected
`3490`. Gaining that full understanding has a couple benefits:

* You can be more confident you've fixed the bug for-realsies.
* You will learn to recognize the patterns that led to this bug,
  allowing you to better avoid it in the future.
* You're working out your problem-solving skills while you do this.

Once you understand how the wrong output was produced, then decisively
and correctly fix the issue, and know why the fix will work.

## Print Debugging

The good old-fashioned standard way of probing software in the middle of
a run is called _print debugging_, or, if you're a C programmer, _printf
debugging_ (pronounced "print eff").

This is basically just tactically placing print statements inside your
code to see what state your program is in.

There are a couple common uses of this:

* Print anything at all to see if some part of the code actually
  executes.

  ``` {.python}
  print("A")

  x = foo()

  print("B")

  if x == 3:
      print("C")
      x *= 2
  else:
      print("D")
      bar()

  print("E")
  ```

  Notice that when I run the code, I can see how far it gets before a
  crash, and I can determine if `x` were `3` or not.

* Print some specific values to see what they are.

  Here's an example where we're getting data from some sensor in a loop
  for processing. We suspect that some of the data is wonky (maybe the
  sensor is busted) so we're printing it out to see what we get.

  ``` {.python}
  while not done:
      data = get_sensor_data()

      print(f"Got sensor data: {data}")

      process_sensor_data(data)

      done = data < 0
  ```


> **Don't use f\-\-king profanity in your debugging statements.**
> Murphy's Law says that if you do use profanity, you'll forget to take
> it out and even though it was in some part of the code that you're
> certain will never run, it will inevitably pop onto the screen while
> you're doing a client demo with your boss the day he's assessing you
> for a raise.
>
> I know as well as anyone how infuriating programming can be. And when
> I'm feeling that way and forget to take a deep breath and recenter, I
> print this:
>
> ``` {.python}
> print("AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA");
> ```
>
> <!-- ` --> Not only does it stand out nice and clear on the screen,
> but it's really easy to type in frustration and helps dispel some of
> my bad energy. And if the client sees it, it's a minor transgression.

Now, print debugging is kinda frowned upon as a lesser means of
debugging compared to using a real debugger (as in the following
section). But everyone does it at some point or another, and some
people even swear by it.

The place that I think it really shines is when you need to gather a lot
of data about the run to see a larger pattern emerge, or when you need
to catch an infrequent event. If something happens one run in 10,000,
single stepping through with a standard debugger is going to take
forever. You can add some print statements and script a run 10,000 times
and watch the output to see when it manifests.

One thing to watch out for is that if you're printing a lot, it can be
tough to visually parse the output, and error messages might be lost in
it. I'd recommend redirecting the output to a file and then bringing it
up in an editor to search.

And, finally, don't forget to remove all your print statements before
you ship your work!

## Debuggers

TODO

## Time-travel debuggers
