__Code 1:__ looking at ``plop()``, we see that x,y are independent uniform random variables in [0,1], and we return 1 if the vector (x,y) has Euclidean norm at most 1. What is the probability that this happens? We're picking a point uniformly in the top right square, which has area 1, and looking at the probability to land into the circle (of radius r=1), whose intersection with that square is a fourth of the total circle area, so πr²/4 = π/4.

So each draw of plop() is 1 with probability π/4: ``plops()`` then computes the empirical mean of n such independent draws, multiplies it by 4, and... we get something whose expected value is π/4*4=π 🥧! Moreover, since we're basically looking at the empirical mean of a bunch of independent Bernoulli random variables (a.k.a. a (scaled) Binomial), we get by [Hoeffding](https://en.wikipedia.org/wiki/Hoeffding%27s_inequality)/[Chernoff](https://en.wikipedia.org/wiki/Chernoff_bound#Sums_of_independent_Bernoulli_random_variables) bounds that this converges to π *really* fast (exponentially in n). 

__Code 2:__ ``fleb()`` picks an integer between 1 and n uniformly at random, and returns 1 if it's prime. What is the probability that this happens? It's entirely obvious, but the [Prime Number Theorem (PNT)](https://en.wikipedia.org/wiki/Prime_number_theorem) guarantees that, as n goes to infinity, this behaves as 1/ln(n). More precisely, if π(n) [Yes, π... but not that π 🥧!] denotes the number of prime numbers in {1,..,n}, then the PNT states that 
$$\frac{\pi(n) \ln (n)}{n} \to 1
$$

How fast does it get there? It doesn't say 🤷. But "we" [not me] can get quantitative bounds, and it gets there quite fast: https://en.wikipedia.org/wiki/Prime_number_theorem#Non-asymptotic_bounds_on_the_prime-counting_function
Now, what does ``flebs()'' do? Given a (large enough?) n, it tries to estimate that probability to be prime, $\frac{\pi(n+1)}{n+1}$, by random sampling (again, empirical mean of a bunch of Bernoulli... using n+1 instead of n for no particularly good reason) It does that for n attempts, takes the average, _and voilà!_ A very good estimate of the constant... 1. (It converges, again, exponentially fast! To 1. 🧐)

Note that there is no particular reason to use the same n for both the "large number in ``fleb()'' *and* the number of repetitions to do the statistical estimate. They are absolutely not tied to each other, but that quiz didn't try **not** to confuse you 🙃.

__Code 3:__ 
