# Making Something From Nothing

# How do you make something from... nothing?
When you want to learn how to program, you will come upon two different types of
resources. One of those resources will start with the assumption that you know
how to program already, you're just trying to learn a different programming
language. Moving from one programming language to another is much easier to do,
as you already know most of the fundamental concepts of how computers work, how
your code works, and how to reason programmatically about things. This can be
likened to changing from a Windows computer to a MacOS computer. Much of the
things are the same, there are just different words, or placement of buttons.

The second type of resource you're going to come upon is the tutorial from the
ground up. This is the thing you're looking for, but often the author uses
jargon, or they assume other knowledge that you have. Alternatively, the author
will just brush certain things off, and just plow ahead, telling you "oh, just
ignore that for now, you'll understand what it means later." Unfortunately for
me, and you might be in the same camp, that doesn't really cut it. I don't like
just doing something without understanding the inner workings of things. I'm
going to be slightly hypocritical here and show you an example.

```java
public class Example {
	public static void main(String[] args) {
		system.out.println("Hello World!");
	}
}
```

This snippet of code (Java is the language, BTW), was shown to me when I first
started programming. Lots of things to unpack here, and my teacher would gloss
over many of the details. I asked "what does public mean"? and admittedly, they
did try to answer, but the answer came with so many more concepts that I didn't
know or understand, the answer was pretty meaningless. So it's understandable
that most teachers just say to memorize certain things. My intro Java teacher
told me to just memorize "public static void main paren string bracket bracket
args end paren", for example. This was irksome to me, so I want to straighten
some of this out and try to really get a "from the ground up" approach to this.

# The computer runs on 0's and 1's
You always see this in shows, and when you're on the computer... you see
Facebook, you see the windows desktop, etc. I see no zeros and ones, so what's
the deal with that?

Well... it is true, technically... But we need to take a step back in order to
really put it in perspective and understand what that statement even really
means. so, let's back up a little bit just to think of the
theory of information. Take this string of characters for example:

```
ORDLAXSEAIADATLHNLBOS
```

What do these characters mean? Well, as it stands, not much. However, if we
break them up in a certain way, it might become more useful.

```
ORD LAX SEA IAD ATL HNL BOS
```

Okay, does this mean anything to you? This is much more useful to me. Once
broken up with spaces like this, I actually recognize those three letter
groupings as acronyms for airports in the USA. (It's okay if you didn't
recognize that, I'm just a freak, it's fine). 

## Interpreting information
Great, that's really cool, we can recognize some meaning from a string of what
seemed like random characters. This is effectively what a computer does with
0's and 1's. And we can too, if we went with similar (what I'll call) "rules".

```
0100100001100101011011000110110001101111001011000010000001110010011001010110000101100100011001010111001000100001
```

Here's a string of 0's and 1's. What does it mean though? Not necessarily
anything, unless we apply some of the right rules to interpret this data.

Well... a long time ago, back in like the 60's (1963 is when the first edition
of the ASCII standard was published), a bunch of people came together and made
some hard decisions. They decided what a grouping of 0's and 1's would be, and
they also decided what each group would correspond to. The American Standard
Code for Information Interchange, or ASCII (pronounced Ask-y) is one such set
of "rules" for how to interpret this series of ones and zeros. Basically, we
told the computer that whenever it sees `01100001`, it should display the
character `a` (under ASCII). ASCII describes an entire mapping of each
permutation of eight 0's and 1's. We call each 0 or 1 "slot", a `bit`. A
grouping of 8 bits is one `byte`. Let's break up the previous string of bits 
into bytes.

```
01001000 01100101 01101100 01101100 01101111 00101100 00100000 01110010 01100101 01100001 01100100 01100101 01110010 00100001
```

And if we interpret these bytes as ASCII...

```
H e l l o ,  r e a d e r !
```

Boom!

I added spaces just for the visualization, but of course the computer doesn't
need to break this up with spaces, since it can figure out the bytes by itself.


# Okay... but why 0's and 1's???
Long story short, because electricity.

The longer story, it's about voltage, and our ability to confidently measure 
that. I'm not going to pretend that I'm an electrical engineer, but I will try
my best to describe what goes on here. We set voltage high or voltage low in
order to store information, like a light switch—the light is either on or off,
and we don't really have any intermediate states (shush about those weird 
slider lights, this is just an example/analogy). Therefore we're storing
information in a series of either on's or off's.

There are people researching how to do quantum computing, which would
theoretically allow us to store information in 4 states, or base 4. This is
still experimental... but the gist of it is that it's looking at the quantum
states of an electron and how it exists in order to encode information.


# So how come I so rarely actually see 0's and 1's?

Typically, we humans can't easily tell what a byte means when displayed as a
string of 0's and 1's, so often we display it in another format: Hexadecimal.
For our `Hello, reader!` example, this would look like:

```
48 65 6c 6c 6f 2c 20 72 65 61 64 65 72 21
```

How is this equivalent...? Well, math. The system of numbers we all know and
love is in "base 10", and is thus called "decimal". Remember the decimal point?
that was so we could break something down to be less than 1. Let's take the
number 127 as an example. Essentially, we had the following in decimal:

| 100's | 10's | 1's |
|--------------------|
|  1    |   2  |  7  |

_Table 1: The number 127 broken down into base 10 (decimal) columns_

In order to get the number 127. Which means there are 1 groupings of 100, 2
groupings of 10, 7 groupings of 1. Each time we hit a "10 boundary", we remove
all elements from the first "bucket" we're in, and mark one in the next highest
bucket. So when we get to 10 1's, we increment the 10's column, and set the 1's
column back to 0. This should be familiar to you.

Well binary is just base 2, and hexadecimal is base 16. so that means the
boundary is at 2 for binary, and the buckets go 1, 2, 4, 8, etc. In hexadecimal,
the boundary is 16, so each "bucket" or column can hold up to 15 in it before it
resets and increments the next column over.

All of these things are succinctly described with math—like so, from right to
left. Base 10:

| 10<sup>2</sup> | 10<sup>1</sup> | 10<sup>0</sup> |
|--------------------------------------------------|
|     1          |       2        |       7        |

_Table 2: The number 127 broken down into base 10 columns by powers of 10_

Basically, for any base, you just make that the big number and put the power
next to it of the column index from the right to left and those are your
"buckets". Pretty neat, huh?

So, what does 127 look like in bases 2 and 16?

| 128's | 64's | 32's | 16's | 8's | 4's | 2's | 1's |
|----------------------------------------------------|
|   0   |  1   |  1   |  1   |  1  |  1  |  1  |  1  |

_Table 3: the number 127 broken down into base 2 (binary) columns_

| 16's | 1's |
|------------|
|  7   |  f  |

_Table 4: the number 127 broken down into base 16 (hexadecimal) columns_

For hexadecimal, it should be noted that since they run out of digits (0-9 being
used already) they just leak over into the alphabet and start taking from the
top. That is, letters A-F are used to denote 10-15 in hexadecimal.
