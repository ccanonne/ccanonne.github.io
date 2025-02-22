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

This question, framed this way, is known as the EQUALITY$${}_n$$ problem in communication complexity:
> How much communication between Alice and Bob is required to decide whether $$a$$ equal to $$b$$?
and more specifically, here, the randomized communication complexity of EQUALITY$${}_n$$, in the public-coin 🎲 setting. _("Public-coin" refers to the fact that there is shared randomness: there is a magic fair coin being tossed publicly infinitely many times, that both Alice and Bob observe.)_
That's good news for Alice and Bob, since a lot of **very** clever people have done a lot of work on communication complexity. **There's hope.** 🎉
