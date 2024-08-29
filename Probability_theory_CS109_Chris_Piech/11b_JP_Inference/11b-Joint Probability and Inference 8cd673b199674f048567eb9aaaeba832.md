# 11b-Joint Probability and Inference

Created: July 16, 2024 9:09 PM
Class: Probabability Theory - CS109

An important insight regarding probabilistic models with many random variables is that "the joint distribution is complete information." From the joint distribution you can compute all probability questions involving those random variables in the model. 

![Untitled](11b-Joint%20Probability%20and%20Inference%208cd673b199674f048567eb9aaaeba832/Untitled.png)

![Untitled](11b-Joint%20Probability%20and%20Inference%208cd673b199674f048567eb9aaaeba832/Untitled%201.png)

- The Federalist Papers- Natural Language Processing
    
    We have a giant dice which has all the words in english language and each word has a different probability and different times in occurs in the document. 
    
    ![Untitled](11b-Joint%20Probability%20and%20Inference%208cd673b199674f048567eb9aaaeba832/Untitled%202.png)
    
    ![Untitled](11b-Joint%20Probability%20and%20Inference%208cd673b199674f048567eb9aaaeba832/Untitled%203.png)
    
    ![Untitled](11b-Joint%20Probability%20and%20Inference%208cd673b199674f048567eb9aaaeba832/Untitled%204.png)
    
    ![Untitled](11b-Joint%20Probability%20and%20Inference%208cd673b199674f048567eb9aaaeba832/Untitled%205.png)
    
    ![Untitled](11b-Joint%20Probability%20and%20Inference%208cd673b199674f048567eb9aaaeba832/Untitled%206.png)
    
    ![Untitled](11b-Joint%20Probability%20and%20Inference%208cd673b199674f048567eb9aaaeba832/Untitled%207.png)
    
    ![Untitled](11b-Joint%20Probability%20and%20Inference%208cd673b199674f048567eb9aaaeba832/Untitled%208.png)
    
    Taking the ratio gets rid of P(D) which we dont know.
    
    Getting the answer with this expression is tricky since we a multiplying very small numbers in both numerator and denominator and then we divide them the resulting very small numbers. 
    
    So we can take the log and instead of multilpication, it becomes addition and instead of division, it becomes subtraction.  Multiplying and dividing small numbers is difficult for computers. Addition and subtraction is far easier.  
    
    ![Untitled](11b-Joint%20Probability%20and%20Inference%208cd673b199674f048567eb9aaaeba832/Untitled%209.png)
    
    ![Untitled](11b-Joint%20Probability%20and%20Inference%208cd673b199674f048567eb9aaaeba832/Untitled%2010.png)
    
- Inference
    
    PMF changes once conditionality is introduced to a PMF. Once we are told that the student is in junior year, the probabilities of the type of rooms is changed. 
    
    ![Untitled](11b-Joint%20Probability%20and%20Inference%208cd673b199674f048567eb9aaaeba832/Untitled%2011.png)
    
    ![Untitled](11b-Joint%20Probability%20and%20Inference%208cd673b199674f048567eb9aaaeba832/Untitled%2012.png)
    
    P(B) is our prior belief (before observing any evidence) and P(B|E) is our updated belief (after  observing any evidence) knowing that E happened.  
    
    ![Untitled](11b-Joint%20Probability%20and%20Inference%208cd673b199674f048567eb9aaaeba832/Untitled%2013.png)
    
- Example
    
    ![Untitled](11b-Joint%20Probability%20and%20Inference%208cd673b199674f048567eb9aaaeba832/Untitled%2014.png)