# Frameworks and Complexity

## Thinking about what tools to use when writing code

### Tags: Software Engineering, Complexity, Organization

Writing clean code, in my view, is all about properly expressing
and containing the complexity that is inherent in your product. The
purpose of all software development tools is to provide helpful
abstractions for representing complexity. When we can effectively organize
complex concepts, we free our mind to think clearly.

What I find interesting about frameworks is that they provide a new interface
with a promise to developers that this interface is a helpful construct for
containing complexity in their problem domain. They offer a tradeoff, spend
time and energy learning how to move in a new system with the hope that this
system will reduce future complexity.

When we decide to learn a framework we're gambling that this up front work
is going to pay off in the long run. Sometimes this doesn't pay off, maybe our
problem domain doesn't align cleanly with the framework, maybe the framework is
poorly written, maybe the framework is poorly maintained, these are all risks
that we decide to accept when we onboard a new framework. Sometimes the gamble
pays off and we are able to express our ideas in a clean, elegant fashion using
our new framework. And it feels nice because I get to put a new tool in the
bottom section of my resume.

When on a team, it's extremely important that everyone knows that tools they are
expected to know in order to move about in their codebases. Whenever a team
decides to commit to using a framework, they're gambling with the time and energy
of the entire team. This can create a lot of friction if expectations aren't clear
or if several memebers find the framework to be unhelpful. If half the team loves
framework A and uses every obscure feature of the framework, while half of the team
isn't particularly enthralled by it, divison will quickly spring up amongst team members.

No one likes using tools they don't understand and people also don't typically like
being forced to learn new tools. A healthy team will try to identify a few frameworks that
naturally fit into their problem domain and commit to learning and using them seriously.
They will also keep the barrier to entry reasonably low, only committing to a framework
if they seriously believe it will reduce complexity.

## Magic Methods

I just read fluent python so I've got python on the brain.

Implementing a bunch of magic methods in python strikes me as a dangerous tradeoff to make
on most teams. Simply enumerating all of them is already a lot of information to take in and
oftentimes it requires developers to intimately understand all the gory details of Python's
data model. The reward for using magic methods is typically that your code can be
significantly more pythonic once all these methods have been implemented. Creating a high
barrier to entry and introducing many hard-to-debug pitfalls in order to write pythonic
code is really only a useful tradeoff for a team that REALLY loves python.

Of course, learning this stuff is still quite interesting and can be very useful for anyone
who finds themselves writing a lot of python code. Just don't try to implement 15 magic methods
for your class if the majority of the team just treats python like dynamic Java.
Perhaps committing to learning python correctly is a worthwhile bet to make for your team, but
that's a decision that needs to be made communally, not by someone submitting PRs filled with
their preferred tools and frameworks.

## Flask

Flask is a framework whose complexity tradeoff is beneficial in many situations. It's fairly
simple to pick up, provides an interface for an extremely useful tool (a web server), and
contains relatively few pitfalls.

Frameworks are pretty cool. Here's a nice quote to round this out from Paul Graham:

When I see patterns in my programs, I consider it a sign of trouble. The shape of a program should reflect only the problem it needs to solve. Any other regularity in the code is a sign, to me at least, that I'm using abstractions that aren't powerful enough-- often that I'm generating by hand the expansions of some macro that I need to write.

