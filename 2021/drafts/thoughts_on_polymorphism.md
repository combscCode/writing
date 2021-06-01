# Thoughts on Polymorphism

### Tags: Software Engineering, Programming Languages


## Golang

I really like the idea of interfaces, golang does a good job of
separating out bundles of data and the functions that operate
on those bundles. 
 
Is there a way to explicitly say that a data type needs to implement
a certain interface?

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

## Java
I feel like the strict OOP stuff that Java enforces leads to a lot of
spaghetti code. Whenever I read through Java code I can't help feeling
like there's so much verbosity and unnecessary complexity floating
around in the code base.

Rarely do the complex inheritence trees that Java lends itself to
actually help me understand what's going on or what a class is supposed
to be doing.

When I see classes that only implement 1 method I immediately want to
delete the repo from my disk. That just seems so obviously incorrect,
what's the point of bundling data together if your interface only
provides 1 method??? Just make a function. It typically aligns much more
clearly with the purpose of that class, when we put stuff in a class
it makes implicit promises about how this data is going to be used.
