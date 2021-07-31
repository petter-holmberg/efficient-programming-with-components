Foreword
==========

Alexander Stepanov is well-known for being the creator of the C++ "Standard Template Library" (STL).
Anyone who has used `std::vector` has benefited from his work.
Much less well-known is that STL is not just a collection
of common routines,
it's an ecoystem for a *theory of programming*
championed by Alex called **generic programming**.
For those not familiar with it's ideas, the STL
can be a confusing and verbose mess.
But with just a short introduction to generic 
programming
principles, its thoughtful design and capability
for writing reusable and correct code become clear.
These lectures are intended to teach exactly that.

Programming, as distinct from computer science
tends to be described as a craft or art,
rather than a field ofs cience or engineering.
It's learned by experience and by studying a loose collection
of examples and rules passed down;
don't make functions "too long", hide "unnecessary" details
in abstractions, group "similar" functionality,
don't use global variables,
avoid duplicating code.
These hint at some truly good ideas, but also 
suggest that perhaps that the underlying principles
of the field have yet to be understood.

Alex's work is about discovering these principles
much more than anything in particular about C++.
It's about the basic logic and math which govern programs,
and it's ability to describe programs is being recognized
 in more [areas][wwdc].

Generic programming starts with algorithms.
Given an algorithm how do we know it will work?
To answer this question a programmer must discover its essential mechanism
and consequently the minimal requirements, for it to work.
These requirements are described as mathematical
constraints on it's inputs.
From this understanding we can *express* the algorithm
in an implementation useful for others, called a **component** .
Complex programs are written simply by combining simple
components that are well understood.

Generality and abstraction actually comes from minimalism;
reducing to essential parts,
as opposed to hiding information,
which is the mantra of black-box layering.
Programs written this way also tend to be fast,
which is a helpful ingredient for reusing code.
If a component doesn't perform, then 
there will always be some performance sensitive application
which can't use it.
Of course, not every algorithm is the best choice for all needs,
but those limitations should be imposed by the algorithm,
not the implementation.

Alex's work makes an additional contribution 
to the question, what does developing software look like in the future?
Will we scavenge for snippets to piece together from the GitHub junkyard?
Will programs be carefully specified and verified with formal proof systems?
Can you `npm install banking-app-starter-template` and 
start customizing?
Are all programs written by hobbyist C artisans? (the vision I'm most partial to)

Alex derives a different model from generic programming,
resembling engineering as done in other fields.
Mathematicians and computer scientists discover algorithms.
Software engineers work together as an industry to implement these as 
standard components with a high degree of professionalism.
These are distributed as standardized catalogs.
Each component is documented in detail, with references to academic literature.
They specify their requirements and complexity in mathematical terms.
It displays graphs of their performance on various data-sets.
Programmers carefully select components that fit their needs
and assemble them into applications.
To understand these catalogs and make contributions of their own
programmers must be educated in basic mathematics
and computer science,
in the same way that engineers require
physics and calculus.

-- Justin Meiners


[wwdc]: https://developer.apple.com/videos/play/wwdc2015/408/

# Acknowledgments

Original course by Alexander. A. Stepanov.

![alex](img/alex.jpg)

Course notes assembled from videos, course materials, interviews,
and books by [Justin Meiners](https://github.com/justinmeiners) in 2021.

The lectures were given in 2013 at [A9](https://en.wikipedia.org/wiki/A9.com).
These notes are intended 
to share scientific information for educational and historical purposes. 
This is a non-commercial project.
Most of the code comes from [Ryan Ernst's repo](https://github.com/rjernst)
who attended the lectures.

# FAQ

**Why do we need these notes if we can watch the [videos][videos]?**

This has all the information an organized form, with references,
and working code.

The videos are actually pretty hard to watch, due
to the slow pace, and interaction with the audience.
Sometimes a mistake is made and they go back and fix it.
Alex may introduce story, and then finish it days later.
Consequently some videos have fewer than 800 views,
and at least 10 of those are me.

[videos]: https://www.youtube.com/watch?v=aIHAEYyoTUc&list=PLHxtyCq_WDLXryyw91lahwdtpZsmo4BGD

**Is all this information available in his books?**

A majority, but not all of the code is available in other forms.
In the lectures you get history, opinions, motivation, practical tips, applications, responses to criticism, all at once.
This is not present in the books, especially "Elements of Programming" which is very formal.
Having this rich context makes the books much more approachable and meaningful.

**This is 10 years old. Is it relevant for a C++ programmer today?**

Absolutely. He will almost certainly teach you applicable things about current
day C++ and STL you did not know.

**Is this relevant for a non-C++ programmer?**

These ideas are not limited to C++ and are being adopted
in more and more libraries and languages.
I hardly ever write C++ anymore.
But, If you have no familiarity with C++ then
this presentation will probably be difficult
to follow.
Try the first lesson.

**How similar is Alex's vision to the  "modern C++" style?**

The emphasis on value types and templates over dynamically allocated
objects with virtual members is similar,
but I think that's where the similarities ends.

It's important to emphasize that this is not a style guide,
but a theory of programming.
The C++ style is then one way of representing this theory in C++.

In my opinion, (somewhat supported by various comments made by Alex)
most developments since C++11 seemed to have missed the point of STL.
A lot of it has been partially understood and remixed in strange and inconsistent ways.
Things which were understood, are no longer (see [std::find is broken][find-broken]).

If you study these notes you will find that Alex outlined much cleaner solutions to many of the problems which later C++ versions attempt to address. 
The most baffling of these to me are three way comparison and ranges.
I am unsure of his opinion on move semantics.
I am unable to comment on whether the Concepts which made it into C++20
are anything like his original vision.

[find-broken]: https://sean-parent.stlab.cc/papers-and-presentations/#warning-stdfind-is-broken

**I have a correction, additional references, or other helpful ideas.**

That would be welcome. Please, make a [pull request](https://github.com/justinmeiners/efficient-programming-with-components).

**How accurate is this text?**

These are course notes, not a transcript.
I try to discern and communicate his intended message,
not necessarily make a historical record of the conversation.

If Alex is sharing a strong opinion or giving a speech
it is likely an exact quote (minus grammar and filler words).
The technical exposition is where 
I have rearranged and filled in missing parts
for educational purposes.

A lot of the links to people and concepts may seem unnecessary
as they are quick google
search away, but I do add those for historical purposes.
Some references may be obvious now which will be difficult to understand
or track down in the future.

