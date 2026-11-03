# Use of AI

[i[Artificial Intelligence]<]

*[This sub-section was written in 2025. Subsequent sub-sections, below,
might have been updated more recently.]*

As of this writing, AI is the new hotness[^0D45]. Everyone is using it,
and no one can stop talking about it.

[^0D45]: Unlike the expression "new hotness", which is now tired.
    "Tired" is also tired, but that's self-referential so I think it has
    bottomed out.

The question no one seems to have an answer for is what's going to
happen. [flw[Sam Altman|Sam_Altman]] and others will tell you that AI is
any second now going to take over the world and solve everything and
humans will be rendered obsolete.

I like to think that will not happen, and that even if AI starts solving
everything, people will still want to use their ingenuity to push the
envelope farther than AI is able to.

What does all that mean for you as a computer science student (as of
this writing)?

Let's talk about how you should use an AI as a student and at work,
because those are two different things.

But before that, let's talk about what you're _not_ supposed to do.

## What Do You Need To Learn?

*[This sub-section was written in November, 2026.]*

I considered titling this section *What Is Even The Point*, but I
rejected it as too downbeat. Forget I said it.

Last February, I felt I could see about one month into the future when
it came to the state of AI. That was relatively terrifying from an
instruction standpoint, as we like to at least pretend we know what the
jobs market will look like after you get BS. And it's certainly
terrifying from a student (and student loan) standpoint.

But today, I feel like that's settled down a bit, and now I feel I have
7-8 months of visibility. It's a lot less than the four years I had
before, but at this point, I'll freakin' take it.

The reasons for increased visibility are twofold:

* The rollout time of LLMs at work is slower than-expected. Lots of
  movers and shakers were saying there would be no engineering jobs by
  now. But the demand for seniors devs is *up significantly*.
  Additionally, there are multiple studies showing that outside of tech,
  AI has not favorably impacted the bottom line. And it's looking a bit
  more and more like Fred Brooks's essay [*No Silver
  Bullet*](https://en.wikipedia.org/wiki/No_Silver_Bullet) is actually
  holding true.

* There's an undersupply of senior devs right now, but there's an
  *oversupply* of junior devs. This gives us a window into what skills
  employers are looking for: the difference between senior and juniors.

Here are the skills that I currently believe you need to learn in order
to succeed. The first two have always been there. The last four are new
AI-world requirements. Lots of universities have taught them to greater
or lesser degrees, but today they're first class targets just like
reading and writing.

(*Caveat:* this is all IMHO. There will be many who disagree with me or
feel this short list is woefully inadequate. Remember, I claim today to
only be able to see 7-8 months into the future. And I'm only so smart.
Read this list with a critical eye!)

* **Writing code.** Even if your LLM will be writing all your code, the
  act of learning to code exercises the problem-solving skills you need.
  As LLM enthusiasts love to say, *it was never about the code*. I'm not
  going to go *that* far, because I think writing code has additional
  benefits. Like it makes you much more skilled at reading code.
* **Reading code.** Your LLM will churn out reams of code before you can
  say [Jack
  Robinson](https://en.wikipedia.org/wiki/Jack_Robinson_(idiom)). Is it
  any good or is it pure unadulterated crap? You're going to sign your
  name on it claiming on your honor and skill as a dev that the code is
  of the *utmost quality*. Wouldn't you like to know if you're right?
* **Problem decomposition.** You have been tasked with something giant
  and you have no idea how to do it. How do you take this huge
  intractable problem and break it down into pieces that you *do* know
  how to solve? One-shotting a massive project will likely result in
  failure; at the very least, it will not be a maintainable piece of
  software. And the more maintainable the software is, the fewer tokens
  you need to burn to make successful changes.
* **Abstraction.** When receiving data over a network, are you receiving
  a stream of bytes or a sequence of packets? If the latter is easier to
  deal with, you should write code to abstract those bytes into packets.
  As data moves around a project, how is it represented at different
  abstraction layers? Where does the conversion happen and why? What
  functionality are you sacrificing by introducing a layer of
  abstraction? What simplicity are you gaining by doing so? Beginners
  are notoriously bad at mixing layers of abstraction. As are some
  experts.
* **Systems-level design.** How do you take a problem and solve it with
  a number of abstract connected components? What components do you need
  in order to meet functional and non-functional requirements? This is a
  toughie—universities typically let the industry handle this
  post-graduation. You'd get a small bug to fix in a specific piece of
  code, and gradually, over the years, you'd learn how the system was
  put together. Do that a few times, and you could start building your
  own large-scale systems.
* **Testing.** With LLMs producing more code than you can check
  line-by-line, tests need to be put in place. Usually the LLM writes
  the tests, and it *really* wants those tests to pass, so much so that
  it can even lie about it. You need to know about different kinds of
  testing so that you can verify the LLM-generated tests are actually
  testing the code.

Instructors should be rolling those last four items into as many courses
as they can without sacrificing code writing and reading. (Speaking as
an instructor, I can tell you this is a massive effort and will be a
work-in-progress for some time.)

When you graduate, you need to be able to solve any computing problem
thrown your way, regardless of whether or not you know the framework or
the language.

This actually has been the goal of practical computer science colleges
everywhere for the last 50 years. It's not new. But now the scope of
"solve any computing problem" has increased.

## How *Not* to Use AI as a Student

[i[Artificial Intelligence-->Student non-usage]<]

*[This sub-section was updated in November, 2026.]*

I've mentioned elsewhere that I like to study the book [i[SICP]]
[flw[SICP|Structure_and_Interpretation_of_Computer_Programs]] to improve
my skills. And how I give myself a six-hour time limit to solve the
problems presented.

Now, these problems aren't real-world problems at all. They're contrived
training problems. And—get this—the answers are all freely available on
the Internet in a wide variety of places.

So why do I spend up to six hours? What a waste, right? Why not just
clone someone's repo and declare that it's implemented so I'm done?

Or, if not that, why not just copy what my friend made?

Or, if not that, why not hire someone to write the answers for me?

Of course, you know the answer. I don't do that because if I do, I
haven't learned anything. More specifically, _I haven't struggled with
the problems_ so the learning that would come from that is lost.

I think you see where this is going: just asking AI to solve the problem
isn't going to increase your skills at all. It's just asking someone
else to do the hard work.

It's like I went to the gym and asked my robot to lift the weights for
me. Sure, I can walk out saying the weights had been lifted
successfully, but I gained nothing from the experience.

I want you to name an activity that, aside from being at the gym,
involves lifting weights all day. Answer: there are none (generally
speaking for the majority of the population). Then why do we spend time
lifting dumbbells at the gym if there are zero other activities that
involve it?

The weights, of course, are just tools we use toward the greater goal of
being generally stronger.

*School is exactly like this*. The programming problems you get in
school are dumbbells. They're not real. They're designed to give you a
workout so that when you get to the job, you have the strength to do the
work.

And because the problems aren't real, AI can solve them all _really_
easily. There's tons of training material out there for them to learn
from.

*But don't be fooled*. Just because AI can solve your school problems
doesn't mean it can solve the real-world problems you're going to face
in your work. (As of now, it can't.)

(And if it could solve all those problems, how much do you think devs
would earn? There's a reason being a dev pays well, and it's because the
work is hard. If it was as easy as typing in an AI prompt, it would pay
minimum wage. That should clue you in to the fact that if *all* you can
do is prompt AI, you're not getting a high-paying gig.)

But that's not to say you shouldn't get good at using AI; it's just that
while you're a student, you have to use it the right way to maximize
your skills development.

The TLDR of this section is this: never ask AI to solve your entire
programming project. It probably can do that, but you'll learn nothing.
The goal of the project is not to complete the problem; it's to get a
workout while you complete it.

Remember: ***every single time you delegate a task, your skill
atrophies***. I don't care if that's doing systems-level project
planning or if it's coding a `for`-loop. You have to decide if the gain
is worth that damage. In school, our focus is (or should be, at least!)
on the *gain*.

[i[Artificial Intelligence-->Student non-usage]>]

## How to Use AI as a Student

[i[Artificial Intelligence-->Student usage]<]

*[This sub-section was updated in November, 2026.]*

First things first: if your school or instructor has banned AI, that's
the rule. And you have to ignore what I've written here. Sorry. I'm
going to assume it hasn't done that foolish thing, and proceed.

So how should you use it? 

* **Use it like you're working with a decent tutor** who knows a lot of
  things kinda well. The AI tutor definitely makes mistakes and gives
  poor advice from time to time, so you should cast a critical eye on
  everything you learn from it.

* **When you're stuck on a small part of a project, ask about that.**
  When you can't remember syntax, ask about that. Ask about the
  idiomatic way to write a loop that removes elements from the array
  it's iterating over. Ask about what a particular operator does or how
  to use it. When you have questions about the language or library, ask
  those. Little bite-sized pieces are fine to ask it about. It can be
  way faster than a standard Internet search.

* **Ask the AI for hints.** You can drop in a functions-worth of code
  and tell the AI, "Something is wrong with this [describe the issue].
  But don't tell me the answer and don't give me the corrected code.
  Just give me hints about how I need to think about the problem to find
  the solution on my own."

* **Get quizzed.** When you think you know a topic, prompt the chatbot
  to ask you questions about it. It tends to be an excellent tester of
  the well-trodden subject matter we use in college and I guarantee
  you'll learn a lot really quickly.

* **Get a code review.** When you've completed the project (and it works
  completely!), then you can feel free to ask AI for a code review.
  Remember: *reflection* is an important part of the problem-solving
  framework! It absolutely will find things you've missed.

Keep in mind that some of the "improvements" aren't going to be
improvements at all, and you'll want to ignore them. *Cast that critical
eye. [Be opinionated](#be-opinionated) and have a rationale for which
advice you're accepting and which you're rejecting.*

Lastly, there's another time it's fine to use AI to solve entire
projects: when your instructor says you can. This happens when they're
giving you more real-world practice as opposed to lifting weights. Both
are valuable uses of your study time.

[i[Artificial Intelligence-->Student usage]>]

## How to Use AI at Work

[i[Artificial Intelligence-->Work usage]<]

*[This sub-section was written in 2025.]*

First, a caveat: the last time I was working in production (and I did so
for 20 years), AI as we know it today did not exist. That said, I do use
it to get things done more quickly today. So that's my level of
"expertise".

I'd mentioned earlier that new devs solve problems with logical
reasoning, but [i[Experts]] experts, in addition, recognize patterns. As
a more-experienced dev, you have a better understanding of which
building blocks make up a problem. You recognize the pieces that you
need, and you logically reason about how to assemble them.

In other words, experienced devs are better at _Understand_ and _Plan_.
(They're better at all phases, but recall that _Understand_ and _Plan_
is where the battle is.)

As such, they can leverage AI to help them write the code for those
building blocks. They can say things like, "I need to filter those
results for anything that matches this regular expression"—and then they
ask an AI to code up that building block, they expertly verify that the
code is correct and modify it to suit their needs, and then move on.

Even with technologies they aren't familiar with, this can help them get
the job done. But they still need to rely on their expertise to know
when they need to learn more. That is, experienced devs have a nose for
dangerous code and know when they need to proceed carefully and gather
more knowledge.

In this regard, AI can be really useful for doing proof-of-concept work
and rapid prototyping where the code is often throwaway.

> _"Let us hurry! There is nothing to fear here!"_\
> _"That's what scares me."_
>
> —Satipo and Indiana Jones, _Raiders of the Lost Ark_

Again, as a student, you can't bring that experience (that you haven't
yet acquired) to bear, and if you just try to use AI like a [i[Experts]]
seasoned dev, you're going to have buggy, fragile code that you don't
know how to fix. And worst of all, you won't be developing the skills
you need.

But as you gather more experience, you can definitely rely on AI to
write a large amount of boilerplate code for you that you already know
the logic behind, anyway.

[i[Artificial Intelligence-->Work usage]>]

## AI and the Jobs Market

[i[Artificial Intelligence-->Job market effects]<]

*[This sub-section was updated in November, 2026.]*

When you read this, I want you to know that I, the author, thought
[fl[Yahoo!|https://www.yahoo.com/]] was a dumb idea when it first
launched. I kinda still do think it was, but it made a bazillion dollars
since then, so I was wrong. At least capitalistically.

One thing old devs have been hearing their entire careers is that we're
on the verge of the "no code" revolution, and that this tool or that
tool will finally put coders out of a job because everyone everywhere
will be able to produce software.

Every one of these predictions has something in common in that they were
all fantastically wrong.

But things are only wrong until they aren't, and LLMs like ChatGPT are
definitely novel beasts that don't play by the previous rules.

> **I do recognize the stock pumping, though.** All those "no code"
> companies were talking a big game trying to get big returns for their
> investors. OpenAI and other AI players also talk that big game.
>
> That's not to say they won't realize those gains; but it is to say it
> smells familiar.

And LLMs are showing incredible coding expertise. I am perpetually
amazed by what they can do. But can they do it all?

I have a thought experiment for you. Let's say there's an AI so good
that I can tell it, "AI, design and implement a corporation that will
crush all my competitors and make me the richest person on Earth," and
it will actually successfully do it.

But the catch is that everyone has access to the same AI and they can
all make the same request. Where does that land us? We're back to square
one where we're on equal footing.

As a capitalist, though, I don't like equal footing. I want to get an
edge on my competition. So I start thinking, "What can we do that's
slightly different than what the AI is telling my competitors?"

And just like that, humans are back in the game!

I think that trend's going to continue, maybe forever.

What will happen, I predict, is that the easy boilerplate jobs that
exist now will experience a massive tightening. AI can solve lots of
those easy problems, and you don't need a big team of engineers behind
them. You can have a senior engineer commanding a bunch of bots to get
the work done.

The unfortunate effect is that there is a large demand for senior devs
now (up ~10-20% as of this writing), and a small demand for junior devs
(down ~10%). So the question, again, becomes: what's a senior got that a
junior doesn't? "Experience" is the glib answer. But what does that even
mean? IMHO, we need to look back at those skills of problem
decomposition, abstraction, systems-level design, and testing.

Going back in time, consider when most programs were written in
[flw[assembly language|Assembly_language]] and it took a lot of
specialized knowledge to get these error-prone programs written. And
then compilers became popular and now no one[^F913] writes in assembly
any longer; those jobs are toast, destroyed by the faster, easier coding
that compilers afford.

[^F913]: Well, a few people do. You should try it for fun. It's something
    else.

In short, I think we're going to keep pushing it, and AI will become a
very useful tool, but only with humans at the helm. I think. We shall
see.

[i[Artificial Intelligence-->Job market effects]>]

> _"And... Always look on the bright side of life..."_
>
> —Lead Singer Crucifee, _Monty Python's Life of Brian_

## Chapter Reflection

* Contrast the useful and non-useful ways students can use AI.

* What goes wrong if you use AI badly as a student?

* How do things differ with AI at work versus at school?

* What are some of the hazards of using AI at work?

[i[Artificial Intelligence]>]

