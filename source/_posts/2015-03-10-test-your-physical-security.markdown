---
layout: post
title: "Have you checked your security?"
date: 2015-03-10 09:36:22 +1300
comments: true
categories:
 - pentest
 - security
---

**Disclaimer: I take NO responsbility for personal or business damages and/or
technical alarm issues as a result of you following my blog post.**

Formalities out of the way ...

We all have a fancy expensive alarm system in our work places, some more fancy
then others; motion sensors, cameras, biometrics, door bolts, lets face it, theres
alot of stuff here... But have you ever actually tested it?

<!--more-->

No, I don't mean the odd "I came into work on the weekend and set it off" excuse
given by staff who say "Well it definitely worked". I mean testing the physical
security of your system as a burglar hoping to actually steal your sensitive financial and
company documents.

It's not something we think of when it comes to security, sure we get our
networks, web applications and business processes audited and tested by
auditors and ethical penetration testing consultants, but the physical alarm system
is never "physically" tested - We get it installed and take the installers word
that, "Your all protected now", and for some reason, that's enough to keep our
worries at bay.
Imagine if your developers say, "Oh yeah, our new Credit Card
database is all protected" and you left it at that, our world would be a VERY
different place.

When it comes to testing your physical security, it's not recommended to just
"go for it" (Did someone say hack on prod?). You might find your staff, and
building neighbours may not appreciate it.
You need to create (setup) a test environment which is a copy of your real alarm, and
now, I don't mean go buy a whole new system just for testing, instead consult your alarm
security contractors about creating a test zone to act like the main system. - Unless of
course your one of these DIY "she'll be right" kinda guys who thinks they have the skill to
program it, them go right ahead.

Next, identify potential targets such as financial documents, important servers
or anything business critical. These should be targets which would be of interest
to anyone breaking in, whether they have insider knowledge or not. These targets
should be what you concentrate on "testing" and in future require careful planning
and protecting.

Finally, inform your monitoring company of your actions, or tell
them to ignore any alerts they recieve while you "test". Who wants Mr Plod showing up to your
building as you attempt to break in? At least you could always try the "I
Locked my keys inside" excuse and see how that fly's...

Now you have set yourself up, think up some creative ways to "break in",
have a look around your offices; are the doors secure;
can you climb the walls; can you move undetected from motion sensors? Cameras? etc, etc...
I Find Google has the best ideas and solutions to problems you might overcome
when trying to bypass a motion sensor.

A few simple words of advice:

1. Be safe, you could find yourself dropping from
   heights or doing something physically demanding, always have a look at whats
   load bearing and stable.

2. Watch out for fire alarm cables. Sometimes you can't make a test environment
   for everything. There's nothing worse than an expensive false callout fee (or
   two) and even worse, setting the sprinklers off all over your perfectly
   good not-on-fire office assets. - Your insurance company may not like you
   very much.

3. Go slow and take your time. Your here to test, it's not a time trial. I've
   never heard of a criminal who stated his break-in was timed. You're in
   control, take your time, look at everything, explore routes etc. If you set
   off your test alarm. reset it and start again.

4. Don't break anything. This could be dangerous and costly to you and your
   business, theres nothing worse than breaking your managers' new expensive oak
   desk by stepping in the wrong place.

You now have a repeatable test environment, which can be used to test your
physical security, over and over again. If you make changes or add new security
devices, simply update your test environment and have a go.


We recently underwent this process when a co-worker researching RFID swipe
cards managed to clone our access cards, rendering them unsecure, because of
this we started exploring what would happen if someone entered our building.
What can they do and, what could they take?

With that, we closed our office, set up a test alarm area, disabled the ear
piercing siren and told our monitoring company to ignore everything and played
a simple Capture the Flag game where we all took turns breaking in.

Unfortunately the results were not what we thought, it was somewhat easier then
we expected. We had people record pin numbers, climb walls, break tiles and
leave dirty shoe marks on our walls - All in an attempt to grab a nice cold
alcoholic beverage from our "secure" area.

This exercise was a wakeup call and allowed us to see what flaws we have,
instead of letting a security installer tell us it's all OK.


I Recommend that every business should actively test their phyiscal security, wheither you yourself
or an independent contractor do it. This should be annaully, or when things change in the business.

Lets face it, its better you find your security holes before a would-be criminal does, so you can
fix them before it's too late.


So, in conclusion, here is my helpful advice again to avoid problems:
<ul>
  <li>Always be safe!</li>
  <li>Create a dummy test zone which mirrors your usual alarm area/s.</li>
  <li>Look out of fire alarm cables, fire engine callouts are not cheap.</li>
  <li>Tell your monitoring company to ignore anything they receive.</li>
  <li>Create goals for your testers.</li>
  <li>Play it slow and safe, if something's not right, stop and have a look.</li>
  <li>And finally... Have Fun!</li>
</ul>
