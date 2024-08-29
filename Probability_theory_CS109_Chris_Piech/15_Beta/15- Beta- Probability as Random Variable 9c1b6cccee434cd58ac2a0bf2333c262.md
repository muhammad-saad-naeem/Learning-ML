# 15- Beta- Probability as Random Variable

Created: July 27, 2024 12:21 PM
Class: Probabability Theory - CS109

## Beta

![image.png](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/image.png)

Sometimes we dont know what the probability for some event is. For example, a coin’s both sides might not be equal resulting in a different probability fo a heads than 1/2. SImilarly, we dont know the probability taht a drug will work or not. We need a method to estimate the probability p itself to be used for our further analysis. 

**We can take p as a random variable itself and make a PMF/PDF for it and estimate p.**

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled.png)

Since probability is continuous, we use PDF. Applying Bayes Theorem. The **denominator is the normalization constant**. We have a **prior belief called f (X=x)** which we need to assume. The best assumption for now is that it remains **constant i.e uniform distribution**. We are assuming that any value of p is equally likely. We also have a likelihood function, P(H=9, T=1| X=x).  **This function is a world where X(probability we are trying to estimate) has taken a value x and we want to know the probability that there were 9 heads and 1 tails, P(H=9, T=1| X=x).** This narration can also be called, 10 trials, 9 successes (heads) with a probability of x. This narrative is called the Binomial Distribution. So collectivily we end up with :

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled%201.png)

All the constant like normalization constant and (10 9) and anythign which doesnot change with x is termed as K. 

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled%202.png)

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled%203.png)

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled%204.png)

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled%205.png)

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled%206.png)

The new belief in probability now depends on how many heads and tails we have seen in our experiments. We can put them as n and m and then solve for every value of x to get a PDF and a plot of p instead of single p value. The plot is nice because it also gives us confidence about where the p value might be including the variance of p. It tells us how uncertain we are about our probability. It tells us how confident we are in our p estimation 

 

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled%207.png)

But there is a little modification where: a = n+1; b= m+1. They do it to make mathematics to be simpler which leads to easier formulas for Estimation and Variance

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled%208.png)

This new modification is called the Beta Random Variable and leads to simpler formulas for Estimation and Variance. But keep in mind that : a = n+1; b= m+1.

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled%209.png)

Now we assumed eariler that our prior believe f(X=x) was uniform i.e. all p values are equally likely. What if we had some other prior belief? What if looking a the coin and judging its physics gives us a prior belief that heads is more likely? I could express that we have n (successes)= 3, m =2.  We could also use Beta itself as a prior.

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled%2010.png)

now our prior is a function instead of single discrete value:

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled%2011.png)

But this can be further simplified 

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled%2012.png)

Our end result also looks like a beta just with different parameters. Instead of just a and b, we now have n,m a and b.  **n and m is our experiments to find out p and a and b are our prior beliefs.** n is not same as a. and m is not same as b. So our end result is also a Beta. Beta of a Beta is a Beta:

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled%2013.png)

So after having a specific prior belief in success and failure, we get to use the equation of the same format as when our prior was uniform and equally likely.  

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled%2014.png)

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled%2015.png)

We have some initial belief as a and b. And we can use them to update our belief on p by seeing in experiments how many n and m we see. And we do this all with Beta. 

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled%2016.png)

a=2 and b=2 meaning 1 heads and 1 tails is also a popular prior belief. 

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled%2017.png)

Three different ways of saying 80%. The more trials we chose as our prior, the less our own experimental data will effect the p. So usually its a good choice to rely on the experimental data and to choose a prior that does not have a lot of trials.

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled%2018.png)

## Thompson Sampling

How does one decide which option to choose from A or B given no prior info. One of the best algorithms to do this is Thompson which tries to optimize success and also exploration of unknown option. Pick any random sample from A and B and pick whichever has higher sample of p. 

![Untitled](15-%20Beta-%20Probability%20as%20Random%20Variable%209c1b6cccee434cd58ac2a0bf2333c262/Untitled%2019.png)

##