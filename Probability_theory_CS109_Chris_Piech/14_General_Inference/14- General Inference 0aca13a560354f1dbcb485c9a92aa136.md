# 14- General Inference

Created: July 22, 2024 8:15 PM
Class: Probabability Theory - CS109

## Covariance and Correlation

Covariance does not always clarify if two things are dependent. In the example below, X and Y are clearly dependent but there covariance is zero.  

![Untitled](14-%20General%20Inference%200aca13a560354f1dbcb485c9a92aa136/Untitled.png)

Another problem is that covariance absolute value doesnot mean something specific. In the example below, we dont know what 45.77 mean:

![Untitled](14-%20General%20Inference%200aca13a560354f1dbcb485c9a92aa136/Untitled%201.png)

so a solution to this is correlation. It is normalized covariance so it remains between 0 and 1
 

![Untitled](14-%20General%20Inference%200aca13a560354f1dbcb485c9a92aa136/Untitled%202.png)

## Bayes Net

To construct a Bayes net, we first need a causal network that can be built by guessing or by finding out the correlations between different things 

Marginalization can make things complicated

![Untitled](14-%20General%20Inference%200aca13a560354f1dbcb485c9a92aa136/Untitled%203.png)

## Rejection Sampling Algorithm-

We need to define a Bayesian Network in code and all the probabilities and conditional probabilities that go with it.

Then you need alot af samples from the joint

How to create a sample? → Defining the probabilites based on Bayes Net and randomly running the numbers of the parents and then the children. Running this loop n times will give us n samples from the joint. The sample quality depends on how good the Bayes net is. If it is weird and not properly related in terms of causality or have too many arrows, the samples will not make sense because sampling depends on causlaity defined in the Bayes net which we have coded with the respective probabilities.  Fever is dependent on whether you have a flu. Flu is dependent on the probability chosen in the beginniing. The bern function in the code below assigns flu=1 with probability of 0.1 

![Untitled](14-%20General%20Inference%200aca13a560354f1dbcb485c9a92aa136/Untitled%204.png)

After collecting n samples, we now reject and count. We reject all the samples from our data set which are not consistent with our inference question and only count those who are consistent. For eg if we are looking for P (F1=1| U=1, T=1), probbaility that someone is undergrad and is tired, we only keep the samples consistent with this condition. We reject all other. By doing this we are doing a conditional property. We are entering a world where these conditions are true and we throw away all samples that are not consistent i.e. out of this world. Once we have rejected all the non-consistent samples, we can count the consistent ones to calculate the P (U=1, T=1). 

![Untitled](14-%20General%20Inference%200aca13a560354f1dbcb485c9a92aa136/Untitled%205.png)

The probabilty at the end is calculated in a very trivial way, we are left with only samples where U=1, T=1 is true. Out of those which also have Fe=1 are counted on numerator and divided by the total selectd samples with U=1, T=1 is true :

![Untitled](14-%20General%20Inference%200aca13a560354f1dbcb485c9a92aa136/Untitled%206.png)

Numerator is where Fever =1

![Untitled](14-%20General%20Inference%200aca13a560354f1dbcb485c9a92aa136/Untitled%207.png)

![Untitled](14-%20General%20Inference%200aca13a560354f1dbcb485c9a92aa136/Untitled%208.png)

If you’re looking for the probability of a very rare event, your n samples might have no such samples or two few samples to give a accurate probability. In this case, you might end up rejecting everything.  We might need to sample alot of samples in this case.