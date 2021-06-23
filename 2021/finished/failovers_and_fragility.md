# Failovers and Fragility

### Tags: Software Engineering, Economics

I was recently listening to a great episode of Freakonomics where they basically just
interviewed Ben Bernanke about his tenure as Chairman of the Federal Reserve (check out
the episode [here][freak-ben]. Ben certainly convinced me that I would be miserable
as chair of the fed, thankfully that wasn't my next career move, but he got me back in
the rut that NTT has been digging in my brain recently.

Reading and listening to NTT has just pushed me further into a mix of intellectual humility
+ nihilism, why worry about things that we can't control or understand? When Ben was
describing his responsibilities it just made my stomach drop, definitely pitied him.
I got the sense that being the chair of the fed is a bit like driving a car with a blindfold
on and with disconnected brakes. You're techincally in the drivers seat and you probably
have the most control out of any one person, but that's not saying very much. Piloting the
economy sounds like an extremely high visibility position with an excrutiating lack of control
over what's actually going on. The worst aspects of a leadership position on steroids.

But anyways, I didn't want to just call out how hard/insane it is to run the fed. I was
thinking about how fragile our economy is and what underlying reasons contribute to that.
I'd really prefer for our economy to not just crumple if one sector does something really
stupid. How have other fields solved this type of problem?

## Failovers

I began thinking about how software engineers make their systems more robust and antifragile
and failovers immediately came to mind. For those who don't know, a failover is essentially
when the primary system is shut down and the secondary system replaces the primary. Robust
services need to be able to failover without manual oversight in order for the system as a
whole to be resiliant to outages.

But how do you encourage engineers to build robust services? The easiest option is just to
talk about it a lot. Add it to the "Core Values" list! Bring it up in All Hands! While this
approach has some value, it turns out that just talking about something isn't enough to instill
it as a cultural value. There need to be processes, there needs to be an environment that
actually encourages robustness.

One of my favorite tech posts was Netflix's post about [Chaos Monkey][netflix-monke], which is
a great example of a company curating their engineering environment to reward a particular
cultural value. Basically, Netflix realized that the best way to build robust services is
to create a tool that actually breaks production instances. Netflix understood that agents
respond to their environment and changed the environment to be filled with failovers. This
strategy is far more effective than regulation, code reviews, pow-wows, or retroactively
punishing engineers for putting out fragile work.

I'm not sure what a Chaos Monkey for the world economy would look like. I'm not convinced that
breaking various parts of the supply chain is a good idea, even in the pursuit of long term
robustness and prosperity. But I do think we need to get creative with our policies, we can't
allow ourselves to only react when things go wrong. There's a need to get proactive, shape
the culture and the environment to reward agents when they behave in an anti-fragile manner.

[freak-ben]: https://open.spotify.com/episode/0RbRoe12Fe2aJB0XSyaInV?si=66W1ZDA1Sluy-D8MCpveuw&dl_branch=1
[netflix-monke]: https://netflixtechblog.com/the-netflix-simian-army-16e57fbab116
