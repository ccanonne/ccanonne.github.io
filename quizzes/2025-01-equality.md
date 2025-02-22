# First Quiz: Alice and Bob compute EQUALITY (or go to jail)

_See the [Quiz on BlueSky](https://bsky.app/profile/ccanonne.bsky.social/post/3lidolztdy22n)._

## Backstory

 🧩 📊 Alice and Bob are in trouble. They've been accused (wrongly, of course!) of stealing classified data, and as theorists they now have to prove they innocence and defend their honour: they've never used any data!

Now their lawyers will give them each a statement, including a list of things they must swear to have done or not. So many things—n of them—to state or deny! To be found innocent, they'd better agree on all of these n items..

That's the trick though. They won't get these lists before the trial!

Worse, they'll have to testify separately, without knowing what the other one says. Their only chance to coordinate? On the way to the trial, in the corridor, they might be able to briefly wink or wave at each other before being ushered into the courtroom.

Alice and Bob are a _little_ stressed.

Thankfully they have an extra resource: the courtroom has one of these big lava lamps in the hall, which they'll both see, and can use to get some shared random number, should they see a need for it. Better than nothing?

They can only communicate 1 bit of information after getting their lists... so **help them** make it count!

1. Alice gets her list of $$n$$ yes/no 📋
 Bob gets his list of $$n$$ yes/no 📋
2. They go to the courtroom, both see the same lava lamp 💡🎲
3. They get to wave or not in the corridor, sharing one bit of information 👋
4. Alice and Bob both testify then plead guilty/innocent

If they plead innocent and their lists are identical (the $$n$$ yes/no statements), they walk free 🎉
If they plead innocent and their lists are different, they go to jail for a long time 🧑‍⚖️
If they plead guilty or disagree, they go to jail (but a much shorter time)

So they'd better be confident!

This is where YOU can help them. What do you think they should say to the judge? Or, to make it simpler: _what should they do to figure out if the lists their lawyers gave them are the same or not?_

> What is the best probability Alice and Bob with which can be sure their $$n$$ yes/no statements 📋📋 are all the same?

Now, the above asks you what you think their best probability of success is. The second question is open ended, and will require you to put your lava lamp where your mouth is:

>  **How** you would suggest Alice and Bob proceed?

## What's the question, again?

Let's try to extract the gist of the question: 
+ Alice and Bob are given, respectively, arbitrary $$n$$-bit strings $$a,b \in \\{0,1\\}^n$$ (the lists 📋 given to them by their lawyers), where $$n$$ is a very large integer; and must jointly decide whether $$a=b$$ with as high a probability of success as possible (over whatever randomness they use to make that decision).
+ To do so, they can only communicate __one__ bit of information (through the waving 👋) to each other. That's not a lot, given that both $$a$$ and $$b$$ require $$n$$ bits to fully communicate!
+ But have an extra resource: they have _shared randomness_, which you can model as a string of uniformly random bits $$r\in\\{0,1\\}^\ast$$ (thanks to the lava lamp which they both observe), which is independent of $$a,b$$.

This question, framed this way, is known as the $$\text{EQ}_n$$ problem in communication complexity:
> How much communication between Alice and Bob is required to decide whether $$a$$ equal to $$b$$?

and more specifically, here, the _randomized communication complexity_ of the Equality function, $$R^{pub}(\text{EQ}_n)$$, in the public-coin 🎲 setting. _("Public-coin" refers to the fact that there is shared randomness: there is a magic fair coin being tossed publicly infinitely many times, that both Alice and Bob observe.)_

That's good news for Alice and Bob, since a lot of **very** clever people have done a lot of work on communication complexity over the past decades. **There's hope.** 🎉

## What's the answer?
As [≈21% of you answered at the time I write this](https://bsky.app/profile/ccanonne.bsky.social/post/3lidokfl6tq2n), by communicating only _one_ bit 👋 __Alice and Bob can succeed with probability at least 50%__. I don't know how to emphasize how _absolutely bonkers_ that is 🤯: they both have an arbitrary $$n$$-bit string, and yet _1 measly bit_ is enough to decide whether they're equal or different!

Thanks to the lava lamp, that is...

## How do we do that?
Let's first consider what happens without randomness 🎲 at all: no lava lamp, first, and no randomness for Alice and Bob either. If they must act deterministically and succeed no matter what $$a,b$$ are, then there's basically nothing they can do unless they communicate $$\Omega(n)$$ bits -- basically their whole input. Put differentially, with only one bit of communciation, Deterministic-Alice and Deterministic-Bob are screwed, and go to jail.

> __Theorem.__ The deterministic communication complexity of $$\text{EQ}_n$$ is $$D(\text{EQ}_n) = \Omega(n)$$.

But the deterministic requirement is a lot to ask. Allowing Alice and Bob to use their own "private" (not shared) randomness, and err with some probability $$\delta < 1/2$$, could help maybe? _(Here we want probability less than 1/2, since the trivial protocol where Alice chooses an answer at random (without even looking at her input $$a$$) and sends it to Bob takes one bit of communication, and has error exactly 1/2...)_

Well, yes. But not __that__ much: one can prove that to achieve probability of error say $$\delta=1/3$$, with only private randomness Alice and Bob still need to communicate quite a lot!

> __Theorem.__ The (private-coin) randomized communication complexity of $$\text{EQ}_n$$ is $$R_{1/3}(\text{EQ}_n) = \Theta(\log n)$$.

The upper bound (algorithm) is not too complicated, but we won't give it here (you'll why soon! 🧐). As for the lower bound, it actually follows from the deterministic case, $$D(\text{EQ}_n) = \Omega(n)$$, as in general one can show (it's not trivial!) that $$R_{1/3}(f) = \Omega(D(f))$$. That's not exactly what we want (we want to see what's the best Alice and Bob could do with _one_ bit of communication), but somehow this does imply that the best probability of error they could achieve __without public randomness__ vanishes with $$n$$.

Which brings us to the lava lamps! 🎲

> __Theorem__(Alice and Bob Get Out of Jail). The (public-coin) randomized communication complexity of $$\text{EQ}_n$$ is $$R^{pub}_{1/3}(\text{EQ}_n) = O(1)$$. Moreover, given $k$ bits of communication, $$\text{EQ}_n$$ can be solved with probability of success $$1-1/2^k$$.
