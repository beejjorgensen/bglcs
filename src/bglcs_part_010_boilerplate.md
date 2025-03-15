# Foreword
<!-- Beej's guide to Learning Computer Science
# vim: ts=4:sw=4:nosi:et:tw=72
-->

<!-- No hyphenation -->
<!-- [nh[scalbn]] -->

<!-- Index see alsos -->
<!--
[is[Git Log==>see Log]]
[is[Recursion==>see Recursion]]
-->

Are you getting into Computer Science, or thinking about it? Or maybe
you're in it already. This super-high-level guide is for you!

I'm not going to talk about how to write code (much). I'll I'm going to
talk about in these roughly 40 pages is more about _how to learn_ when
you're a nascent software developer.

Now, as much as I'd like to know exactly the way that everyone learns
(and manage to wedge that into 40 pages), I, to be perfectly honest,
don't.

What I do have is 40+ years of programming experience (self-taught
before college), 20 years of industry experience, and 8+ years of
teaching experience. And a BS and MS in Computer Science.

And I have opinions about how to best way to learn how to program!

Now, let's get this right out of the way: you might completely disagree
with what I have to say here. And I'm okay with that.

But I have had the opportunity to see students make a wide variety of
mistakes. And hopefully I can head some of these off at the pass for a
number of readers.

Students and teachers, alike: if you find something you disagree with or
something vital that is missing, please don't hesitate to [fl[let me
know|mailto:beej@beej.us]] so I can improve the guide.

Disclaimer: like with all the guides I write, I'm not the master of the
subject. And with a squishy topic like how humans learn, I'm even less
so.

But give it a read and take what's useful and leave the rest for the
[flw[boids|Boids]].

## Audience

[i[Audience]]

Undergrad students just getting into programming are the people I had in
mind while writing this. So give-or-take a bit around that target
audience. People in high school or just looking to learn how to program
are also probably out there in the audience, as well.

## Official Homepage

[i[Home page]]

This official location of this document is:

[fl[`https://beej.us/guide/bglcs/`|https://beej.us/guide/bglcs/]].

## Corrections

[i[Corrections to the Guide]]

I make these guides available for free in the sincere hope that people
will find them maximally useful. If there's something that's not
maximally useful (or, you know, "wrong"), I'd love to hear about it so I
can fix it in furtherance of my mission.

* [fl[Email me|mailto:beej@beej.us]]
* [fl[Report an issue|https://github.com/beejjorgensen/bglcs/issues]]
* [fl[Submit a pull request|https://github.com/beejjorgensen/bglcs]]

Thank you!

## Email Policy

[i[Emailing Beej]]

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

[i[Mirroring]]

You are more than welcome to mirror this site, whether publicly or
privately. If you publicly mirror the site and want me to link to it
from the main page, drop me a line at
[`beej@beej.us`](mailto:beej@beej.us).

## Note for Translators

[i[Translations]]

If you want to translate the guide into another language, write me at
[`beej@beej.us`](mailto:beej@beej.us) and I'll link to your translation
from the main page. Feel free to add your name and contact info to the
translation.

Please note the license restrictions in the Copyright and Distribution
section, below.

## Copyright and Distribution

[i[Distributing the Guide]]

Beej's Guide to Learning Computer Science is Copyright © 2025 Brian
"Beej Jorgensen" Hall.

With specific exceptions for source code and translations, below, this
work is licensed under the Creative Commons Attribution-Noncommercial-No
Derivative Works 3.0 License. To view a copy of this license, visit:

[`https://creativecommons.org/licenses/by-nc-nd/3.0/`](https://creativecommons.org/licenses/by-nc-nd/3.0/)

or send a letter to Creative Commons, 171 Second Street, Suite 300, San
Francisco, California, 94105, USA.

One specific exception to the "No Derivative Works" portion of the
license is as follows: this guide may be freely translated into any
language except English, provided the translation is accurate, and the
guide is reprinted in its entirety. The same license restrictions apply
to the translation as to the original guide. The translation may also
include the name and contact information for the translator.

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
