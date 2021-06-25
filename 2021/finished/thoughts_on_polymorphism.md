# Thoughts on Polymorphism

### Tags: Software Engineering, Programming Languages

Polymorphism seems kinda strange. It's one of those subjects where there's just a thousand
different ways to tackle the problem and they can all "technically" do the same thing but
everyone has extreme opinions about which one is the best. I guess if I got more experience
working in the different philosophies I'd also become a radical but I'm not quite there yet.
It's a really interesting topic though so this is just me expounding on my own malformed
opinions.

## Golang

I really like the idea of interfaces, golang does a good job of
separating out bundles of data and the functions that operate
on those bundles. My internal model for computation usually defaults
to that model so golang's interfaces just nestle in so nicely. I also
feel like golang's interface provides the least amount of pitfalls, it
doesn't offer many features so it's easy to not get tripped up by something
you forgot about.

Composition over inheritance is cool!!! Instead of a new data type
inheriting from an ancestor, we just include the ancestor in the new
data type + whatever extra functionality is required. I like that approach,
it conforms to the folds of my mind.


## Python
Duck typing is cool but I don't think it's the most clear way to do
polymorphism. Duck typing allows us to just create a class and implement
methods that make sense for that class. Then if it turns out that class
A lends itself towards being a sequence, we'll be able to use it as a
sequence.

Duck typing allows us to stay flexible with how classes are used.
Often our design changes, our requirements change, and when we're doing
strict inheritence trees it creates a bunch of weird boiler-plate code
to express something that should be fairly simple. Duck typing allows us
to just give classes the methods that they need to use to do their job,
then if we've done it right (an important caveat) we can use it for a variety
of other purposes.

One issue w this is just the weirdness that can happen. A lot of times its
hard to figure out how a class can be used without just inspecting its code
(while also knowing a ton about the python data model). Once you've mastered
the data model this seems enticing but the complexities it introduces also
introduces opportunities for BUGS!!!

## Java
I feel like the strict OOP stuff that Java enforces leads to a lot of bad
uses of OOP. Whenever I read through Java code I can't help feeling
like there's so much verbosity and unnecessary complexity floating
around in the code base.

Rarely do the complex inheritence trees that Java lends itself to
actually help me understand what's going on or what a class is supposed
to be doing.

When I see classes that only implement 1 method I immediately want to
nuke the repo from orbit. That just seems so obviously incorrect,
what's the point of bundling data together if your interface only
provides 1 method??? Just make a function. It typically aligns much more
clearly with the purpose of that class, when we put stuff in a class
it makes implicit promises about how this data is going to be used.

## Conclusion

There is no conclusion to this, only ramblings. I don't have enough experience
actually writing maintainable software to put forward my opinions. This doc is
just a historical record for future Chris Combs to laugh at.

