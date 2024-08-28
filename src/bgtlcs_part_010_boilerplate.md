<!-- Beej's guide to Teaching and Learning Computer Science

# vim: ts=4:sw=4:nosi:et:tw=72
-->

<!-- No hyphenation -->
<!-- [nh[scalbn]] -->

<!-- Index see alsos -->
<!--
[is[Git Log==>see Log]]
-->

# Foreword

Boy, did you come to the wrong place! What you have here is a book
written by a programmer with 20 years of industry experience who has
been teaching computer science since 2017.

And I have an opinion about how to teach and learn computer science!

Now, let's get this right out of the way: you might completely disagree
with my stance(s). And I'm okay with that.

But with my meager experience, I have had the opportunity to see
students make a variety of mistakes. And I've also seen instructors make
what I consider to be mistakes, as well[^d01a]. And hopefully I can head
some of these off at the pass for a number of readers.

[^d01a]: Of course, they figure they're right and that _I'm_ the one
    making mistakes. And maybe they're right! What can ya do.

Instructions for students: I encourage you to read both the teaching and
learning part of this guide. And if you find something you disagree
with, please don't hesitate to let me know so I can improve the guide.

Instructions for teachers: I encourage you to read both the teaching and
learning part of this guide. And if you find something you disagree
with, please don't hesitate to let me know so I can improve the guide.

Why is this a single tome? Teaching and learning are completely
intertwined. To teach, the teacher must learn to be a learner. To learn,
the learner must learn to be a teacher. This is why I feel there's
something to be had for all audiences in both the teaching and learning
sections of the guide.

Disclaimer: like with all the guides I write, I'm not the master of the
subject. And with a squishy topic like teaching and learning, I'm even
less so.

So give it a read and take what's useful and leave the rest for the
[flw[boids|Boids]].

But first, some boilerplate!

## Audience

Both teachers and learners of computer science are the target of this
guide. Skill level is assumed to be beginner—beyond that and you might
know more than I have to say in these pages.

As a student, I have in mind an undergrad. Some of the advice I give in
the guide isn't good for PhDs, where you might, in fact, have to learn
or use the things that I say you don't. This guide is not written with
research or discovery in mind.

But I'm hoping by the time you're a PhD, you have it down.

Full disclosure: I only have a BS and MS in CS.

## Official Homepage

This official location of this document is (currently)
[fl[https://beej.us/guide/bggit/|https://beej.us/guide/bggit/]].

## Email Policy

I'm generally available to help out with email questions so feel free to
write in, but I can't guarantee a response. I lead a pretty busy life
and there are times when I just can't answer a question you have. When
that's the case, I usually just delete the message. It's nothing
personal; I just won't ever have the time to give the detailed answer
you require.

As a rule, the more complex the question, the less likely I am to
respond. If you can narrow down your question before mailing it and be
sure to include any pertinent information (like platform, compiler,
error messages you're getting, and anything else you think might help me
troubleshoot), you're much more likely to get a response.

If you don't get a response, hack on it some more, try to find the
answer, and if it's still elusive, then write me again with the
information you've found and hopefully it will be enough for me to help
out.

Now that I've badgered you about how to write and not write me, I'd just
like to let you know that I _fully_ appreciate all the praise the guide
has received over the years. It's a real morale boost, and it gladdens
me to hear that it is being used for good! `:-)` Thank you!

## Mirroring

You are more than welcome to mirror this site, whether publicly or
privately. If you publicly mirror the site and want me to link to it
from the main page, drop me a line at
[`beej@beej.us`](mailto:beej@beej.us).

## Note for Translators

[i[Translations]<]
If you want to translate the guide into another language, write me at
[`beej@beej.us`](mailto:beej@beej.us) and I'll link to your translation
from the main page. Feel free to add your name and contact info to the
translation.

Please note the license restrictions in the Copyright and Distribution
section, below.
[i[Translations]>]

## Copyright and Distribution

Beej's Guide to Teaching and Learning Computer Science is Copyright ©
2024 Brian "Beej Jorgensen" Hall.

With specific exceptions for source code and translations, below, this
work is licensed under the Creative Commons Attribution-Noncommercial-No
Derivative Works 3.0 License. To view a copy of this license, visit
[`https://creativecommons.org/licenses/by-nc-nd/3.0/`](https://creativecommons.org/licenses/by-nc-nd/3.0/)
or send a letter to Creative Commons, 171 Second Street, Suite 300, San
Francisco, California, 94105, USA.

One specific exception to the "No Derivative Works" portion of the
license is as follows: this guide may be freely translated into any
language, provided the translation is accurate, and the guide is
reprinted in its entirety. The same license restrictions apply to the
translation as to the original guide. The translation may also include
the name and contact information for the translator.

The programming source code presented in this document is hereby granted
to the public domain, and is completely free of any license restriction.

Educators are freely encouraged to recommend or supply copies of this
guide to their students.

Contact [`beej@beej.us`](mailto:beej@beej.us) for more information.

## Dedication

The hardest things about writing these guides are:

* Learning the material in enough detail to be able to explain it
* Figuring out the best way to explain it clearly, a seemingly-endless
  iterative process
* Putting myself out there as a so-called _authority_, when really
  I'm just a regular human trying to make sense of it all, just like
  everyone else
* Keeping at it when so many other things draw my attention

A lot of people have helped me through this process, and I want to
acknowledge those who have made this book possible.

* Everyone on the Internet who decided to help share their knowledge in
  one form or another. The free sharing of instructive information is
  what makes the Internet the great place that it is.
* Everyone who submitted corrections and pull-requests on everything
  from misleading instructions to typos.

Thank you! ♥
