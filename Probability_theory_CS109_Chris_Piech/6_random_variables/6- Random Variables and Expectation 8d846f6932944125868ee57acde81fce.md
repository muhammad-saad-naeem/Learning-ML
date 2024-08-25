# 6- Random Variables and Expectation

Created: July 7, 2024 12:11 PM
Class: Probabability Theory - CS109

- Conditional Independence
    
    The independence can change when some condition is put onto the events. 
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled.png)
    
    Originally G5 is dependent on T. But once we condition the existence of G2 i.e if G5 affects T given G2 exists, G5 and T become independent. Its because G5 makes G2 more likely which makes T more likely. 
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%201.png)
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%202.png)
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%203.png)
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%204.png)
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%205.png)
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%206.png)
    
- Random Variables
    
    Its a variable just like when we write code but we don’t know what the value of that variable would be. Its uncertain. 
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%207.png)
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%208.png)
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%209.png)
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%2010.png)
    
- Probability Mass Function
    
    The probability mass function (PMF) provides the "mass" (i.e. amount) of "probability" for each possible assignment of the random variable.
    
    For a variable (call it 𝑋) to be a proper random variable it must be the case that if you summed up the values of P(𝑋=𝑘) for all possible values 𝑘 that 𝑋 can take on, the result must be 1:∑𝑘P(𝑋=𝑘)=1
    
    For further understanding, let's derive why this is the case. A random variable taking on a value is an event (for example 𝑋=2). Each of those events is mutually exclusive because a random variable will take on exactly one value. Those mutually exclusive cases define an entire sample space. Why? Because 𝑋 must take on *some* value.
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%2011.png)
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%2012.png)
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%2013.png)
    
    Y was a random variable as we didnt know what value it actually had. Y=2 is now an event since we know its value. Any boolean operation on a random variable will make it an event. Y<2 is also an event as we have entered a space where Y is not uncertain anymore.
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%2014.png)
    
    If Y=2 then probability that Y =2 is between 0 and 1
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%2015.png)
    
    k can be any number and then the function will generate the probability of y being k
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%2016.png)
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%2017.png)
    
    PMF can be represented in different ways:
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%2018.png)
    
- Expected Value
    
    A random variable is fully represented by its probability mass function (PMF), which represents each of the values the random variable can take on, and the corresponding probabilities. A PMF can be a lot of information. Sometimes it is useful to summarize the random variable! The most common, and arguably the most useful, summary of a random variable is its "**Expectation**".
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%2019.png)
    
    Loop through all the values x that the random variable can take, get the probability of x and multiply x with P(X=x). Sum over all the looped values. It tries to center the Expected value towards the most likely outcome. 
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%2020.png)
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%2021.png)
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%2022.png)
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%2023.png)
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%2024.png)
    
    Expectation from data is just weighted average i.e. mean of all values in dataset
    
    If you take expectations of two variables and sum them, it is equal to expectation of the Sum. It does not matter how X and Y are related. 
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%2025.png)
    
    It doesnot matter if you multiply (elongate) you expectation and sum something to it, with linearity, expecation holds its property.
    
    ![Untitled](6-%20Random%20Variables%20and%20Expectation%208d846f6932944125868ee57acde81fce/Untitled%2026.png)
    
    but expectation is not enough. It summarizes everything in PMF to a single value which looses a lot of information or could be misleading 
    
- 
-