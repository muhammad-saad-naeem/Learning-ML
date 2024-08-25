# 3- Definition of Probability

Created: June 29, 2024 12:37 PM
Class: Probabability Theory - CS109

### 

![Untitled](3-%20Definition%20of%20Probability%2028597290c45f49709a5b70012c61eb4e/Untitled.png)

![Untitled](3-%20Definition%20of%20Probability%2028597290c45f49709a5b70012c61eb4e/Untitled%201.png)

![Untitled](3-%20Definition%20of%20Probability%2028597290c45f49709a5b70012c61eb4e/Untitled%202.png)

![Untitled](3-%20Definition%20of%20Probability%2028597290c45f49709a5b70012c61eb4e/Untitled%203.png)

![Untitled](3-%20Definition%20of%20Probability%2028597290c45f49709a5b70012c61eb4e/Untitled%204.png)

lets say you perform 𝑛 trials of an "experiment" which could result in a particular " [Event](https://chrispiech.github.io/probabilityForComputerScientists/en/part1/probability/#events) " occurring. The probability of the event occurring, P(Event) , is the ratio of trials that result in the event, written as count(Event) , to the number of trials performed, 𝑛. In the limit, **as your number of trials approaches infinity, the ratio will converge to the true probability.**

- **Two Interpretations of Probability**
    
    **Natural Randomness:** This view sees probability as reflecting inherent randomness in the world. Like flipping a coin, some outcomes are truly random and chance determines the result.
    
    **Limited Knowledge:** This view proposes that the world might be deterministic (not random), but our knowledge is limited. Probability becomes a way to express our **belief** about an event happening, given what we **don't know**. → This is more useful 
    
    **Example: Weather Prediction**
    
    Imagine predicting tomorrow's weather. If we knew the exact position and motion of every air molecule (super unlikely!), we could theoretically predict the weather perfectly. But we don't have that information. So, we use probability. The chance of rain tomorrow is a statement about our **uncertainty** based on the limited weather data we have.
    
- **Origins of Probabilities**
    
    There are different ways probabilities are determined:
    
    1. **Analytical Calculations:** Using math and established formulas, we can calculate exact probabilities for some situations. For example, the probability of rolling a specific number on a fair die can be calculated analytically.
    2. **Data and Experiments:** We can gather data from experiments or observations to estimate probabilities. For instance, tracking historical weather patterns might help us estimate the probability of rain tomorrow based on similar past conditions.
    3. **Subjective Beliefs:** Sometimes, probabilities are simply educated guesses based on our knowledge or experience. For example, you might assign a high probability to your friend showing up on time if they are usually punctual.
    4. **Combined Approach:** Most real-world probabilities come from a combination of these methods. We might start with a subjective belief (prior probability) and then update it based on new data or evidence.
- **Axioms/Identities of Probability**
    
    ![Untitled](3-%20Definition%20of%20Probability%2028597290c45f49709a5b70012c61eb4e/Untitled%205.png)
    
    1. All probabilities are numbers between 0 and 1. As you perform trials of an experiment it is not possible to get more events than trials (thus probabilities are less than 1) and its not possible to get less than 0 occurrences of the event (thus probabilities are greater than 0).
    2. All outcomes must be from the [Sample Space](https://chrispiech.github.io/probabilityForComputerScientists/en/part1/probability/#sampleSpace). If your event is the sample space, then each trial must produce the event. This is sort of like saying; the probability of you eating cake (event) if you eat cake (sample space that is the same as the event) is 1.
    3. The probability of event E not happening
        
        
        | **Axiom 3**: If 𝐸 and 𝐹 are mutually exclusive, then P(𝐸 or 𝐹)=P(𝐸)+P(𝐹) | The probability of "or" for mutually exclusive events |
        | --- | --- |
        | It applies to events that have a special property called "mutual exclusion": the events do not share any outcomes. |  |
- Equally likely outcomes
    
    Because every outcome is equally likely, and the probability of the [sample space](https://chrispiech.github.io/probabilityForComputerScientists/en/part1/probability/#sampleSpace) must be 1, we can prove that each outcome must have probability:
    
    P(an outcome)=1/|𝑆|
    
    Where |S| is the size of the sample space, or, put in other words, the total number of outcomes of the experiment. Of course this is only true in the special case where every outcome has the same likelihood.
    
    ***Definition:*** Probability of Equally Likely Outcomes
    
    ![Untitled](3-%20Definition%20of%20Probability%2028597290c45f49709a5b70012c61eb4e/Untitled%206.png)
    
    There is some art form to setting up a problem to calculate a probability based on the equally likely outcome rule. 
    
    (1) The first step is to explicitly define your sample space and to argue that all outcomes in your sample space are equally likely. 
    
    (2) Next, you need to count the number of elements in the sample space 
    
    (3) finally you need to count the size of the event space. 
    
    The event space must be all elements of the sample space that you defined in part (1). The first step leaves you with a lot of choice! For example you can decide to make indistinguishable objects distinct, as long as your calculation of the size of the event space makes the exact same assumptions.
    
    Always assume your objects to be distinct. Assuming unordered makes it simpler and allows us to use n choose k
    
    ![Untitled](3-%20Definition%20of%20Probability%2028597290c45f49709a5b70012c61eb4e/Untitled%207.png)
    
    **The sample space must be equally likely outcomes. For that it is important to treat all entities as distinct. B**ecause then every item is different and the probability of it happening becomes 1/S
    
    ![Untitled](3-%20Definition%20of%20Probability%2028597290c45f49709a5b70012c61eb4e/Untitled%208.png)
    
    B