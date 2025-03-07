# Problem Solving

This is an idea completely stolen from the book [flw[_How to Solve
It_|How_to_Solve_It]] by George Pólya. It's a book about attacking math
problems. And since computer science is just math under the hood, it
completely applies!

Actually it doesn't completely apply, and I just said that because it
sounded so good. But it can be bent into shape pretty easily. And I
recommend reading the book.

So what is it? It's short and pretty easy to memorize:

1. Understand the problem
2. Come up with a plan
3. Code up the solution
4. Reflect on what you could do better

That's it.

And if you think about it, that's really just a four-step process for
solving just about any problem at all. Is your living-room light not
working? You can solve it with these steps.

I want to stress something: **Steps 1, 2, and 4 do not involve
coding**[^3cfe]. These steps are all in your head and on paper. I would
argue that ***solving programming problems does not involve a
computer***. That seems clearly nonsensical, but that's where the action
actually is! Especially in step 2, coming up with a plan. That's the
hard part. That's why you get paid the big bucks. Anyone can type a
program in once the problem has been solved.

[^3cfe]: Sometimes they can, actually, but only to write small,
    throwaway, exploratory proof-of-concept programs.

Step 3, coding it up, is simply writing the solution down. The hard work
isn't writing the solution down; the hard work is coming up with it in
the first place!

Also, you're unlikely to progress linearly through these steps. You'll
probably have to pop back and revisit earlier steps from time to time,
but hopefully your overall progress is in the upward direction.

Finally, as a student, you must resist the urge to look up the answers.
The goal here is for you to exercise your problem-solving muscles
(because no one will hire you as a dev without those skills).
Virtually every problem any instructor will come up with has been
extensively covered on the Internet or can be solved with some AI.
Remember that getting the correct answer isn't the point; the point is
to practice problem-solving so that you can get an answer to any problem
that's thrown at you.[^b374]

[^b374]: I don't think AI can solve *all* problems that get thrown at
    it, meaning that you'll still have a job, but they can solve the
    relatively basic problems that are commonly used in computer science
    curricula. It's 2025 now and we'll see how well this footnote ages.

Let's explore the steps.

## Understanding the Problem

Everyone, students included, loves to skip this step. Wise instructors
will add a quiz to be turned in before coding starts that verifies you
understand the problem[^873c]. But you need to pressure yourself to do
this step first, regardless.

[^873c]: I could stand to be more wise, myself.

Logically, if you don't understand the problem fully, none of the rest
of the steps matter. You could come up with the best plan and code it up
perfectly, but if you didn't understand the problem to begin with,
you've just coded up the perfect solution to the wrong problem![^8050]

[^8050]: Once on a programming challenge website I coded up perfect
    solutions to *two* problems that weren't the one I was meant to
    solve. I misunderstood it twice. Took me three-times longer than it
    should have to get the actual solution in place.

And that's a waste of your employer's time and money, at best. Or, if
you're still a student, a waste of time you could have spent studying
for that discrete math exam that's coming up. Or whatever.

So don't skimp on this one—it's fundamentally important.

What do I do? Here are some ideas.

* Read the problem slowly and methodically. These descriptions tend to
  be concise and error-prone. They're not easy to read.
* Take notes. Especially note inconsistencies, omissions, errors, and
  outstanding questions.
* Rewrite the problem in your own words. This is a very effective
  technique.
* Research things you don't understand.
* Ask clarifying questions[^99ca].

[^99ca]: This is actually part of your job description as a dev. People
    will expect and rely on you to do this in the workplace. So don't be
    afraid of doing it; be afraid of *not* doing it.

How do I know when I'm done? ***You're done when you can teach someone else
what the problem is.*** (You don't need to teach the solution—just the
problem.)

It's very, *very* hard to write a complete description of a problem, and
the ones you'll get at work or even in school will certainly be wanting.
Don't believe me? Write down the rules of tic-tac-toe ("noughts and
crosses" if that's what you call it) and I can guarantee I'll find
something you didn't write down[^5b26].

[^5b26]: You didn't say how to choose who moves first, if it could be
    played by three people, or that my "X" couldn't take up more than
    one square. For example.

Because of this, you'll very likely have to ask clarifying questions.

> **Anecdote time!** I was on a project where I was writing the
> front-end of a system and someone else was writing the back-end. There
> was a very specific document describing the exact interaction between
> the two.
>
> One of the interactions involved the transmission of the result of a
> computation. There was an example in the doc that gave the answer, in
> hex, to the math. It was something like:
>
> > Given the inputs `"abc"` and `"xyz"`, the result will be the number
> > `f319c2c6dcfb`.
>
> I coded it up (it was easy since the algorithm pseudocode was given),
> and it computed the answer correctly. I added the code to transmit the
> 6-byte number to the server and that was it.
>
> Except the person writing the server wrote me and said that I was
> sending garbage.
>
> We had some back and forth, and it turned out they thought the spec
> meant I'd send a string with those hex digits in it, and I thought the
> spec meant that I'd send the raw bytes of the result. The spec was no
> help—it was ambiguous and neither of us caught it.
>
> The easiest thing was for me to convert the number to string and send
> it, so I added that line of code and the problem went away. But we
> could have caught it earlier with more careful examination of the
> spec.

## Coming Up with a Plan

Time to start coding? **NO!** Not yet, eager beaver![^77b5]

[^77b5]: As of 2025, I worked at Oregon State University. Go Beavs!

This step, coming up with a plan, is where programming actually happens.
Like I said before, this is what makes the job hard, and is why it pays
well. This is the step you have to be good at to be a dev.

So you must understand the problem well enough to teach it to someone.
Or at least you *think* you do. You might learn more later. But
understanding the problem isn't the same as knowing how to solve it.

If the problem is really simple and familiar, you might come up with a
plan almost instantly. Experienced devs faced with familiar tasks don't
need to spend long planning once they've fully understood the problem.

But experienced devs faced with unfamiliar tasks **do** need to spend
time at it. It doesn't matter how good you are—if you haven't seen the
problem, you're going to need to plan the solution.

Literal pencil and paper can be useful for this step. Here are some
things to think about.

* How will data flow through the system and be transformed, from the
  known input to the desired output?

* During those transformations, what are the subsystems that will
  perform each step?

* What technologies will you need to perform these steps?

* What are the known unknowns?

One big thing to notice is that we're talking about breaking down a
problem into its subcomponents. How to do this isn't always obvious,
though the more experience you get, the easier it becomes.

A trick you can use is to think, "This project would be easy if only the
input data were in *this* form." Then see if you can come up with some
code that converts the data into that form.

Another benefit of breaking up the project into smaller parts is that
it can naturally suggest a way to break up your code into smaller
functions or classes. This makes your code more maintainable and
readable.

You'll have to do some research during this phase to learn what tools
you have at your disposal. Expect to do that.

It's *really* common during the planning phase to realize that you've
failed to understand the problem fully. When this happens, drop back to
the Understanding phase to get clarity, then jump back to planning.

***You know you're done with planning when you can simulate the run on
paper and in your head and you're confident it works. And you can write
high-level pseudocode.*** Bounce your plan off a few [flw[rubber
ducks|Rubber_duck_debugging]] to see if it holds water.

## Coding Up a Solution

This is the easy part! You have to translate your pseudocode plans into
code.

If you've understood the problem and come up with a solid plan, the code
will work. Maybe even on the first try, if you're very lucky.

If you didn't understand the problem and didn't come up with a plan,
then this is not the easy part. You will see no end to trouble, and
might fail to complete the project.

Of course, we're only human and we'll mistype things and make dumb
errors, but that's *way* easier to debug than if you have a bad plan, or
worse, bad understanding of the problem. Yikes!

The hard parts of coding it up are:

* Knowing the language syntax.
* Knowing what libraries are available.
* Not making trivial mistakes.
* Following the plan exactly.

We'll talk about how to learn languages later, and the second two bullet
points can be addressed by being more careful, using something like
[flw[pair programming|Pair_programming]], or leaning on AI.

While you're coding, you might find a place where your plan doesn't
work. This happens quite a bit. When it happens, drop back to the
planning phase, fix the plan, and then come back up to the coding phase
to implement it.

Again, this phase is supposed to be relatively easy. If you're having
trouble trying to get it to work beyond just fixing your syntax errors
(i.e. there's something more structural amiss), your understanding or
your plan is likely flawed. You should drop back to the planning phase
to fix it, and maybe back to the understanding phase, if required.

***You're done with this phase when the code works and passes all your
tests.***

## Reflect on Improvements

Last and definitely not least, look back and cast a critical eye on what
you've done. Yes, it works and passes all the tests. But is it as
elegant as it could be? Is it as readable and maintainable as it could
be? Are there are places where the code is fragile and might fail on
unexpected inputs?

No matter what your skill level is, there is always room for
improvement. And one of the top ways we learn is to look back on the
crappy code we wrote and see how we could have made it better.

Code reviews are fantastic if you can coax someone into taking the time
to do it for you. They will make suggestions for things you can
improve, and you can fix them now and remember them for next time. And
you might disagree and not make those fixes; that's okay, too.

Again, we can leverage AI to help with this. Once you've solved a
problem and have it working, ask the AI for suggestions for
improvement[^08dd] and see if there are any worth following. This
technique is effective on small pieces of code, not large projects, but
that makes it a great assistant for undergrad work.

[^08dd]: Make sure your instructor and/or employer allows this.

> **But, very importantly for undergrads, you need to solve the problem
> first**, and only then ask the AI to help you improve it. Your goal in
> school training (just like in gym training) is to get a workout with
> feedback, not have someone else do the work for you.

***You're done with this phase never.*** Well, practically you're done
with it when you give up and decide you've learned enough about
improving the code. But you're probably not going to find the _Ultimate
Solution to the Problem Ever_ because you're still building your skills
throughout your life.

That said, this phase is where a **lot** of learning happens. This is
where you can effectively build your stats with relatively low effort.

## Think Like a Villain

When solving problems, I want you to think like a villain; that is,
think like someone who is going to abuse the system that you're
designing and building.

A real square root function, for example, could be well tested. Give it
some perfect squares, some non-perfect squares, some fractions, etc.
Works perfectly. You wouldn't pass in negative numbers, right? That
would be silly. But you know who would? A villain!

> **I once visited an online shop that allowed you to order negative
> amounts of product.** The checkout page said they were going to credit
> my account by tens of thousands of dollars.
>
> I never had the guts to check out, though, since I didn't want to be
> on the hook for shipping all that product to them.
>
> Plus, I'm not a real villain... I was just thinking like one!

Expect the unexpected in terms of data that your code will receive.
Expect malicious actors to feed in data in an attempt to gain
unauthorized access or manipulate the system in undesirable ways. Test
for that stuff in your code.

This applies to all phases from understanding to reflection.

> **Someone I knew in college worked for the army** looking at plans for
> things like tanks that had not yet gone into production. His job was
> to think like a villain and ask questions like, "How are you going to
> get a wrench between those pipes to tighten that bolt?"

Thinking like a villain can not only catch problems you might not have
otherwise considered, but it will lead you to a deeper understanding of
the project that will produce more durable and maintainable code.

## Use in Interviews

The four-step process from this chapter is exactly what you should use
on interview coding challenges.

See, these interview problems are quite insidious. They don't have
obvious answers at all.

And why not? Is it because you haven't studied enough? **No.** That's
not it at all. No matter how much you study, interviewers will come up
with a question that doesn't have an obvious answer to you, the sadistic
devils.

And why would they do that? Do they want you to fail? Not at all. *They
want to see you apply your problem-solving skills*.

> **This isn't universal, incidentally.** There are a million
> interviewing styles, and some of them really do just want to see how
> many correct answers you get. But I would argue they aren't
> interviewing optimally. And further, I'd argue that the only way to
> get correct answers is to apply the problem-solving steps, so you
> might as well do it in every case.

It's natural when you're under the stress of the interview and are
presented with an initially-impossible problem that you seize up like a
deer in the headlights. All your knowledge suddenly vanishes in a cloud
of mist and you know you'll never get this job now ever and—

***If you panic, STOP.*** Say to yourself these words: "The only thing
that matters now is *understanding the problem*." Forget the solution.
That's not important. Coding it? Not important. Just focus on step one:
understand the problem.

There are two main reasons for this. One is that the interviewer is
hoping you'll start there. (And that should be reason enough.) But the
other is by starting with understanding the problem, your brain will
kick back into gear and automatically start thinking up strategies for
solving the problem... and that's step two of the problem-solving
framework! You're already on your way.

Try to think (you villain) of anything ambiguous in the problem
description. Ask questions to clarify those things. What are the limits
on the input? What are the limits on output? What do you do in error
conditions? Maybe suggest an example input and output and verify that
you have it right with the interviewer.

This tells the interviewer that you give attention to detail, an
important trait to have.

And get this: for many interviewers, seeing you effectively attack a
problem in a systematic way is actually more important than you getting
the actual correct answer. And on the flip side, not showing your
problem-solving skills when giving an answer might sink you, even if the
answer is correct!

> **When I interviewed at Activision**, there were two questions I did
> not get right. But I hammered my way through them aloud as best I
> could, showing how I'd attack problems. I got the job.
>
> The blown questions were: "What is the fastest way to reverse the bits
> in a byte?" and "Optimize this computation that builds a grid of
> distances between all soccer players on a field."

So go through the whole process with the interviewer. And don't forget
the final reflect step! What would you do better? How could the solution
be improved? Interviewers love that stuff, and you love keeping
interviewers happy, right?

