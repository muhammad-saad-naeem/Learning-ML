# 4- Conditional Probability and Bayes

Created: July 2, 2024 8:26 PM
Class: Probabability Theory - CS109

![Untitled](4-%20Conditional%20Probability%20and%20Bayes%2055661c94467b4bf38090c114aeb44d66/Untitled.png)

Probabilty of either one of the event happening is equal to the sum of each probability, such that both events are mutaually exclusive.

- Mutually Exclusive Events
    
    Two events: 𝐸 ,are considered to be mutually exclusive (in set notation
    
    𝐸∩𝐹=∅
    
    ) if there are no outcomes that are in both events (recall that an event is a set of outcomes which is a subset of the sample space). In English, mutually exclusive means that two events can't both happen.
    
    ![Untitled](4-%20Conditional%20Probability%20and%20Bayes%2055661c94467b4bf38090c114aeb44d66/Untitled%201.png)
    
    ![Untitled](4-%20Conditional%20Probability%20and%20Bayes%2055661c94467b4bf38090c114aeb44d66/Untitled%202.png)
    
    ![Untitled](4-%20Conditional%20Probability%20and%20Bayes%2055661c94467b4bf38090c114aeb44d66/Untitled%203.png)
    
    ![Untitled](4-%20Conditional%20Probability%20and%20Bayes%2055661c94467b4bf38090c114aeb44d66/Untitled%204.png)
    
- Conditional Probability
    
    We already know something and in this case our sample space shrinks and finding the second probability is easier. In this case , the sample space will become F (something already known) and event space will be intersection of E and F consistent with event F.
    
    Probability of something is hugely updated once we know some information. This is how, in reality, probabilities are calculated. We know something and want to know the probability of something else given that the information we know is true. 
    
    what is the chance of an event 𝐸 happening given that I have already observed some other event 𝐹. It is a critical idea in machine learning and probability because it allows us to update our probabilities in the face of new evidence.
    
    Given that event 𝐹 has occurred, the conditional probability that event 𝐸 occurs is the subset of the outcomes of E that are consistent with 𝐹
    
    ![Untitled](4-%20Conditional%20Probability%20and%20Bayes%2055661c94467b4bf38090c114aeb44d66/Untitled%205.png)
    
    ![Untitled](4-%20Conditional%20Probability%20and%20Bayes%2055661c94467b4bf38090c114aeb44d66/Untitled%206.png)
    
    ![Untitled](4-%20Conditional%20Probability%20and%20Bayes%2055661c94467b4bf38090c114aeb44d66/Untitled%207.png)
    
    ![Untitled](4-%20Conditional%20Probability%20and%20Bayes%2055661c94467b4bf38090c114aeb44d66/Untitled%208.png)
    
    Given that we know the probability of E given F and the probability of F, we can find the probability of E AND F
    
- Law of Total Probability
    
    ![Untitled](4-%20Conditional%20Probability%20and%20Bayes%2055661c94467b4bf38090c114aeb44d66/Untitled%209.png)
    
    ![Untitled](4-%20Conditional%20Probability%20and%20Bayes%2055661c94467b4bf38090c114aeb44d66/Untitled%2010.png)
    
- Bayes’ Theorem
    
    ![Untitled](4-%20Conditional%20Probability%20and%20Bayes%2055661c94467b4bf38090c114aeb44d66/Untitled%2011.png)
    
    ![Untitled](4-%20Conditional%20Probability%20and%20Bayes%2055661c94467b4bf38090c114aeb44d66/Untitled%2012.png)