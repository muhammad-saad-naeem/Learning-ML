# 12- Inference

Created: July 20, 2024 1:08 PM
Class: Probabability Theory - CS109

![Untitled](12-%20Inference%20b313a8a6aa224c408d382002fc21f9ea/Untitled.png)

- Eye Test
    
    ![Untitled](12-%20Inference%20b313a8a6aa224c408d382002fc21f9ea/Untitled%201.png)
    
- Solving Joint Probability with Bayes including a discrete and a continuous Random variable.
    
    ![Untitled](12-%20Inference%20b313a8a6aa224c408d382002fc21f9ea/Untitled%202.png)
    
    ![Untitled](12-%20Inference%20b313a8a6aa224c408d382002fc21f9ea/Untitled%203.png)
    
    ![Untitled](12-%20Inference%20b313a8a6aa224c408d382002fc21f9ea/Untitled%204.png)
    
    ![Untitled](12-%20Inference%20b313a8a6aa224c408d382002fc21f9ea/Untitled%205.png)
    
    ![Untitled](12-%20Inference%20b313a8a6aa224c408d382002fc21f9ea/Untitled%206.png)
    
- Bayes with two continuous random variables- A better eye test
    
    
    ![Untitled](12-%20Inference%20b313a8a6aa224c408d382002fc21f9ea/Untitled%207.png)
    
    ![Untitled](12-%20Inference%20b313a8a6aa224c408d382002fc21f9ea/Untitled%208.png)
    
    ![Untitled](12-%20Inference%20b313a8a6aa224c408d382002fc21f9ea/Untitled%209.png)
    
    Two ways to represent the PMF. In code, we can store it as a dictionary
    
     
    
    ![Untitled](12-%20Inference%20b313a8a6aa224c408d382002fc21f9ea/Untitled%2010.png)
    
    ![Untitled](12-%20Inference%20b313a8a6aa224c408d382002fc21f9ea/Untitled%2011.png)
    
    ![Untitled](12-%20Inference%20b313a8a6aa224c408d382002fc21f9ea/Untitled%2012.png)
    
    P(A=a) is our prior belief, some prior ability of the user that we know of or have derived from historical data. P(A=a|Y=0), probability of certain ability given that user failed the question. P(Y=0|A=a) is what we need to find. This is the probability og user getting the answer wrong given that we know something about thier ability. 
    
    ![Untitled](12-%20Inference%20b313a8a6aa224c408d382002fc21f9ea/Untitled%2013.png)
    
    ![Untitled](12-%20Inference%20b313a8a6aa224c408d382002fc21f9ea/Untitled%2014.png)
    
    ![Untitled](12-%20Inference%20b313a8a6aa224c408d382002fc21f9ea/Untitled%2015.png)