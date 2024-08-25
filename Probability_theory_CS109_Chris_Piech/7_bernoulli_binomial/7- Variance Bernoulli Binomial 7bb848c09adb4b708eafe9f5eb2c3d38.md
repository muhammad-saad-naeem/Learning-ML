# 7- Variance| Bernoulli Binomial

Created: July 7, 2024 12:11 PM
Class: Probabability Theory - CS109
AI summary: This document discusses the concepts of Bernoulli Binomial and Bernoulli Random Variable in probability theory. It explains the formulas and properties associated with these random variables, including the probability mass function (PMF), expectation, and variance. It also introduces the concept of standard deviation as a more interpretable measure of spread.

When solving problems, if you can recognize that a random variable fits one of these formats, then you can use its pre-derived probability mass function (PMF), expectation, variance, and other properties. Random variables of this sort are called **parametric** random variables. If you can argue that a random variable falls under one of the studied parametric types, you simply need to provide parameters. 

- Bernoulli Binomial
    
    A pattern appears in many probabilty based problems…
    
    ![Untitled](7-%20Variance%20Bernoulli%20Binomial%207bb848c09adb4b708eafe9f5eb2c3d38/Untitled.png)
    
    ![Untitled](7-%20Variance%20Bernoulli%20Binomial%207bb848c09adb4b708eafe9f5eb2c3d38/Untitled%201.png)
    
    All of the examples above follow the same pattern of story. There are n experiments, p is the probability of success if nth experiments and we want to know the probabilty of k successes out of n trials.
    
    A simple generalized formula can be used in all of the above cases:
    
    ![Untitled](7-%20Variance%20Bernoulli%20Binomial%207bb848c09adb4b708eafe9f5eb2c3d38/Untitled%202.png)
    
    This generalized formula takes on the form of Bernoulli Binomial so it can be applied to a random variable. Remind that random variable can take any value and a PMF will generate the probability of the value that a random value can take. 
    
    ![Untitled](7-%20Variance%20Bernoulli%20Binomial%207bb848c09adb4b708eafe9f5eb2c3d38/Untitled%203.png)
    
    So when we try to calculate the Probability of this random variable X, the PMF becomes:
    
    ![Untitled](7-%20Variance%20Bernoulli%20Binomial%207bb848c09adb4b708eafe9f5eb2c3d38/Untitled%204.png)
    
    Here k is the value that random variable X can take on and generate, using the Bernoulli Binomial, the probability of k successes from n trials where success has probability of p. The n is not included in P(X=k) because we declared, already above, X as a binomial with trials n and probability p. Below is Bernoulli in action:
    
    ![Untitled](7-%20Variance%20Bernoulli%20Binomial%207bb848c09adb4b708eafe9f5eb2c3d38/Untitled%205.png)
    
    ![Untitled](7-%20Variance%20Bernoulli%20Binomial%207bb848c09adb4b708eafe9f5eb2c3d38/Untitled%206.png)
    
    Once a random variable, H, is declared as Binomial, we can access without any proof, the formula and get the answer. The key is that H as random variable should follow the same pattern of story that Binomial attempts to solve. 
    
    ![Untitled](7-%20Variance%20Bernoulli%20Binomial%207bb848c09adb4b708eafe9f5eb2c3d38/Untitled%207.png)
    
    If H=0 and H=10 are mutually exclusive, OR (+) can be applied. H cant be 0 and 10 at the same time, making both events mutually exclusive. so P(H=0 or H=10) = P(H=0) + P(H=10)
    
    ![Untitled](7-%20Variance%20Bernoulli%20Binomial%207bb848c09adb4b708eafe9f5eb2c3d38/Untitled%208.png)
    
    Steps to solve 
    
    1. define a Random Variable
    2. Declare the random variable a Binomial using X =Bin(n,p)
    3. Use the Binomial formula 
    
    ![Untitled](7-%20Variance%20Bernoulli%20Binomial%207bb848c09adb4b708eafe9f5eb2c3d38/Untitled%209.png)
    
    ![Untitled](7-%20Variance%20Bernoulli%20Binomial%207bb848c09adb4b708eafe9f5eb2c3d38/Untitled%2010.png)
    
- Bernoulli Random Variable- A special case of Binomial where n=1.
    
    It can take on two values, 1 and 0. It takes on a 1 if an experiment with probability 𝑝 resulted in success and a 0 otherwise.
    
    ![Untitled](7-%20Variance%20Bernoulli%20Binomial%207bb848c09adb4b708eafe9f5eb2c3d38/Untitled%2011.png)
    
    Bernoli only takes value 1 or 0. Its binary. Happens or doesnt. Sum of all bernoullis in a Binomial. 
    
    ![Untitled](7-%20Variance%20Bernoulli%20Binomial%207bb848c09adb4b708eafe9f5eb2c3d38/Untitled%2012.png)
    
    ![Untitled](7-%20Variance%20Bernoulli%20Binomial%207bb848c09adb4b708eafe9f5eb2c3d38/Untitled%2013.png)
    
    Variance is especially useful for comparing the "spread" of two distributions and it has the useful property that it is easy to calculate. In general a larger variance means that there is more deviation around the mean — more spread. However, if you look at the leading example, the units of variance are the square of points. This makes it hard to interpret the numerical value. What does it mean that the spread is 52 points
    
    2
    
    ? A more interpretable measure of spread is the square root of Variance, which we call the Standard Deviation
    
    Std(𝑋)=Var(𝑋)
    
    . The standard deviation of our grader is 7.2 points.