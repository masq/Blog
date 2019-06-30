# Getting Started in InfoSec

# So you want to get started in Information Security
That's awesome, and I would argue it's a great field to get into. That said,
it's a very intmidating field to get into. There is a lot of jargon to
understand, and some people's jobs are kinda stops along the way to being some
type of InfoSec god. What I mean by that is that some "subfields" of infosec
require you to understand how code is written, how it works, and how to write
some of it yourself; software developers should understand security too, but
sadly, often do not.

Honestly though, this field being difficult to get into is not to say that
others are not hard to get into... but this field has so many _free_ and
available resources to learn with, which is awesome, but it's really _really_
hard to find the correct "starting" point. Instead you find yourself trying to
get into an impenetrable circle of knowledge—any time you try to learn something
it's hard to learn it because of the dependencies on other knowledge.

# Get over being stupid. You are. You always will be.
I realize this is a strong statement, and I intend it to be. But hear me out.

Starting off in this field, you will find it intimidating. Starting off for the
first time in a CTF or something _will_ be intimidating, you will feel dumb.
And, you're _not_ dumb per se, but you are certainly ignorant. You're ignorant
in that you've not yet had the chance to learn this thing. That's okay. Everyone
_must_ start somewhere.

Now, that's just within yourself, there is also the difficulty of the other
people in the field. They will also be intimidating. Why? A variety of reasons.
First off, once you get stuck, you'll think about asking a question, but you
pause; you don't want to ask your question for fear of the other person thinking
you're unintelligent. Unfortunately, there's no easy way to overcome this other
than to just not care. I say, be stupid! Embrace it! Some people _will_ give you
flak for being unknowledgable about something that they find fundamental. That's
okay, and I think everyone is guilty of this from time to time (though, some
more than others). This usually comes across in the form of the question "Wait,
you really don't know X!?" said incredulously. Then the question asker is put in
the awkward position of essentially admiting their own stupidity. It's crappy,
but it's honestly going to happen so many times that you must get over it in
order to proceed in learning. Personally, I learn best via others; so I've
definitely needed to get over sounding/being stupid, because in all honesty, I
was, and in some fields, I still am. That said, there's also the infamous

## Imposter Syndrome...
Which helps to contribute to this incredulous question asking. People want to be
smart, and are insecure in their own intelligence. It starts when they start off
in the field and everyone around them is so knowledgable... and it never goes
away. They will _always_ feel like they're the "underdog" so to speak, feeling
that they are not the expert. I've been called an expert in some things, and I
never really felt that classification resonate with me. There are still so many
things that I'm not good at / don't know within the infosec field, and yet,
there are still many many things that I do know.

# Strategy
I recommend failing fast. Realize what things you don't know and then just go be
stupid at experts in order to goad them into telling you the information you
need. Play off of the imposter syndrome—people want to feel smart, so go be dumb
at them so they show you how things work and they feel good about themselves.
The added benefit to this is generally that they feel good about
teaching/showcasing their skills/knowledge, and you actually gain that
knowledge.

Personally, I gained much of the knowledge I have today by attending every talk
I could, spending time with peers that were working on infosec things (I joined
a CTF team/club). The first _year_ of working on that stuff, I didn't really
dive in because I felt like an outsider the whole time... that I didn't know
enough to really be able to contribute or fit in. After the first year, I was
able to solve my first actual CTF problem (not just the high school/practice
CTFs), and that was when I felt like I could do this. That's when I went full in
on the CTF team and I started getting the most benefit and learning out of it. I
highly recommend interacting with people, going to conferences when you can and
networking. Working on things together with people and exchanging those ideas
together is how we learn things. So put the idea that you're intelligent at the
door, just accept your own ignorance/stupidity and blaze on through
conversations with people for that mutual benefit I mentioned earlier. You
_might_ even contract some friends \*shudders\*

# All of this said
and yet I didn't even say where to get started. I've mentioned CTF at this point
a few times, and so you're probably wondering wtf I'm talking about. CTF stands
for Capture The Flag (CTF), and I can't define it better than just sending you
to [CTFTime](ctftime.org), which is a website all about CTFs. It's not the
physical version of CTF, but a hacking challenge/puzzle game.

# What all is there in infosec
I'd say there are quite a few sub-fields within infosec. I think that as of this
writing, redteaming/appsec are the current hotness. Here is a list of the
sub-fields within infosec that you might want to check out/consider.

* Reverse Engineering
* Application Security
* Red Teaming
* Cryptography
* Exploitation
* Forensics
* Network Security
* Endpoint Security
* Blue Teaming
* Threat Intelligence / Reconnaissance
* Policy & Compliance
* Hardware Security
* Critical Infrastructure / ICS Security
* Security Engineering / Development

NOTE: None of these are entirely independant... they often have overlaps with
each other in terms of skillset/knowledge required.

Reverse Engineering is taking some code that someone else wrote and reading it.
That sounds unimpressive, but that _is_ what it is. However, there are lots of
obstacles that can crop up and it's a really important field. You generally are
going to be a malware analyst or you're going to be doing this in the name of
Application Security or Exploitation.

Application Security is trying to break an application and/or discover flaws in
it. Generally comapnies that create software (or hardware) will employ people
that test their products to make sure that they're not vulnerable to attacks by
hackers. This is often called Penetration Testing or PenTesting for short. The
reason I avoided using that name here is because PenTesting is a generic term
that could be used to describe someone doing Application Security or someone who
does Red Teaming.

Red Teaming is basically trying to break into networks, be they physical or
digital. Generally as a red teamer, a company would hire you to break into them
and then you tell them how you did it so they can remediate that security
vulnerability you exploited to break into them.

Cryptography is the study of math but with a focus on protecting information
from interception by a third party. This can go both ways though, where you
could be studying how to break "cryptographic methods", or means of encrypting
some data, i.e. break the means of rendering the data uninterpretable by a third
party.

Exploitation is essentially taking Application Security a step further and
developing code that will exploit or take advantage of the vulnerability or hole
in the software so that you can accomplish a goal unintended by the developer of
the application. For example, the most severe vulnerability will allow for an
attacker to send code into the application, where the application expects data,
and the application runs the attacker's code.

Forensics is looking back to understand what happened or what's being hidden
somewhere. The best example I can think of of this type of work would be the
work law enforcement might do on seized hard drives, looking for evidence of
wrong-doing. This can also be 

Network Security is about defining proper pathways for data to flow within a
network, and remediating situations where data is flowing in the wrong place.
This is often times setting up firewalls and networking monitoring tools to
ensure the network is secure.

Endpoint Security is about ensuring that hosts in a network are secure and
working properly. Think anti-virus, but this could also be incident response.

Blue Teaming is often about taking data from Endpoint Security and Network
Security people and actioning it. For example, working in a Security Operations
Center (SOC).

Threat Intelligence is often represented as Recon challenges in a CTF. It's
kinda a niche sub-field, but it's been getting a lot of press lately. It is
traditionally a military thing, but it's also in the private sector too now.
It's going to be about collecting/processing/analyzing data in order to inform
decisions. This is kinda a job based around googling things \*ducks\*; I'm not
doing it much justice since I don't think I can be concise about it, but it's
actually a cool field.

Policy and Compliance is basically the intersection of Law and InfoSec. I
personally find a lot of this stuff dry, but it's super important. These are the
people that make sure that there are actually laws/policies in place for how to
actually handle things in a secure and respectful way. Lots of orgs will have
policy/compliance officers.

Hardware Security... I'm probably lumping a bunch of stuff together and the
hardware hackers will get mad at me, but this is going to be working on various
embedded systems (e.g. smart TV). Anyone who makes hardware is going to need
hardware security.

Critical Infrastructure / ICS Security is going to be security focused on larger
control systems like nuclear power plants, the electricity grid, HVAC, etc.
These systems are kinda specific compared to most other computers out there, so
it requires its own special people

Security Engineering / Development is going to just be coding work related to
security. There are tons of things that need coded that are for security
specific domains.

# Recommendation
B-but Spencer, I don't know which thing I want to do and they're all equally
interesting. I get that... so then you're probably wondering which one is
easiest so you can start. Well... None of them are easy, so that's not really a
good filter for where to start.

I would say pick one, even if you aren't sure you'll like it, and just try to
get at least a good working knowledge of that one. If you find you love it, hell
yeah, go for it. But if you get to a good place with it and you're just kinda
thinking it's "meh", _definitely_ try out some of the other fields. But I would
definitely recommend focusing on one thing for a bit.

I would play some CTFs and just try to work on one category. When you get stuck,
that's great, stick with it for 2 hours of being stuck. Then, if you haven't
made _any_ progress and are completely out of ideas after hitting your head
against the wall for 2 hours, then move to a different problem. Once you've done
this with every problem for the given category, the CTF will probably be over or
you'll need to sleep or something. If not, feel free to look at other
challenges, but the important bit is to bang your head on the wall for a long
period of time. That will make the problem memorable for you, and what the
problem was that you needed to solve. Once the CTF is over, wait a bit/watch for
Writeups that people put out on how to solve the problem. This will allow you to
see where you got stuck and see what was needed to overcome that obstacle and
you will absolutely remember to do that next time it comes up.

# Resources
TODO: links to resources




