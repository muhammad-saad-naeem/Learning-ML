# 10- Normal Distribution

Created: July 14, 2024 1:28 PM
Class: Probabability Theory - CS109

- Definition
    
    A bell curve defined by its mean (the tallest point of the curve) and variance (width of the peak)
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled.png)
    
- Why Normal or Gaussian Distribution is so important- its a **very reasonable assumption for a lot of things, and its easy to use.**
    
    Many things in the world are not distributed normally but data scientists and computer scientists model them as Normal distributions anyways. Why? Because it is the most entropic (conservative) modelling decision that we can make for a random variable while still matching a particular expectation (average value) and variance (spread).
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%201.png)
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%202.png)
    
    Simplest explanations are preferred and Gaussian wins these. 
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%203.png)
    
    Although things are complex, simplifying them usually leads to a generalised description that fits normal distribution. If we remove all the complexity and define things simply, a lot of things follow the normal distribution are easily defined by it with acceptable accuracy.  **Gaussian is a very reasonable assumption for a lot of things.**
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%204.png)
    
- The PDF of Normal Distribution
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%205.png)
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%206.png)
    
- Integrating a  Normal Distribution to get a probability
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%207.png)
    
    The integral is kind of unsolvable.  
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%208.png)
    
    BUT. WE solved it numerically to get a magical function, phi. 
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%209.png)
    
    How? **We can use a transformation of any normal to a normal with a precomputed CDF.** Lets see some of the properties of the Normal Distribution function first:
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2010.png)
    
    Linear transform means adding a constant to the normal and multiplying the normal with a constant. Linear transformation of a normal is also a normal. We know what the new normal, post linear transformation will look like. It will have a new mean and a variance due to the linear transformation.  
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2011.png)
    
    We can also do a very special linear transformation where we choose a specific a and b which leads to the mean 0 and variance 1. In this linear transformation, we make a new normal, the STANDARD NORMAL DISTRIBUTION, which has mean =0 and variance =1. And it looks like this:
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2012.png)
    
    Since the Standard normal is a computationally less expensive, the CDF for it can be calculated numerically. It can be solved for a lot of x values to get the Phi. Phi is like a table with all the CDFs for possible x values. 
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2013.png)
    
    So, summarizing:
    
    We did not have a CDF or a way to integrate the Normal Distribution. Now we know that:
    
    - A linear transformation of normal leads to a normal
    - We can apply a special linear transformation to a Normal to get a simplified normal with mean =0 and variance =1 called the Standard Normal
    - Calculating a CDF for a Standard Normal is easier, doable and also now available.
    
    This gives us a recipe to solve any Normal distribution. We can convert any Normal  to a Standard Normal and calculate its CDF.  
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2014.png)
    
    We can also use this phi table to solve ANY Normal Distribution. This means we can do a CDF of any Normal and use the same phi from the table above :
    
    For any normal, if you subtract the mean (𝜇) of the normal and divide by the standard deviation (𝜎) the result is always the standard normal.
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2015.png)
    
    This means just minus mean from X and divide the wohloe thing with Std. This mean and Std are from or original Normal Distribution. This way we havesimplified the whole linear transformation process and got to use the Phi from the Standard Normal table
    
- Solving Problems
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2016.png)
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2017.png)
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2018.png)
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2019.png)
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2020.png)
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2021.png)
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2022.png)
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2023.png)
    
- Normal Distribution approximates Binomial Distribution without intense computation
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2024.png)
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2025.png)
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2026.png)
    
    The answer is not accurate beacuse we are missing something 
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2027.png)
    
    We need to account for missing or adding soemthing that shouldnt be there . The correction table:
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2028.png)
    
    But Poisson also approxiamtes Binomial. Which one do we use and when?
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2029.png)
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2030.png)
    
    if p is small, Poisson is good. If n and variance is large, Normal is good
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2031.png)
    
- 68% of X is within 1 of the std.
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2032.png)
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2033.png)
    
    ![Untitled](10-%20Normal%20Distribution%20ea1957e54bd84870833666a3ce6839da/Untitled%2034.png)