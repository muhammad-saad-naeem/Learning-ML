# 1- Counting

Created: June 29, 2024 12:36 PM
Class: Probabability Theory - CS109
AI summary: This document discusses the Step Rule of Counting and the Or Rule of Counting in the context of probability theory. It explains how to calculate the total number of outcomes using these rules and provides examples. It also mentions the Inclusion-Exclusion Principle for cases where sets may overlap. The document concludes with a brief mention of how to deal with overcounting.

- Step Rule of counting
    
    ***Definition***: Step Rule of Counting (aka Product Rule of Counting)
    
    If an experiment has two parts, where the first part can result in one of 𝑚 outcomes and the second part can result in one of 𝑛 outcomes regardless of the outcome of the first part, then the total number of outcomes for the experiment is 𝑚⋅𝑛.
    
    How many distinct pictures can you generate from (a) a smart phone camera shown with 12 million pixels, (b) a grid with 300 pixels, and (c) a grid with just 12 pixels?
    
    ![https://chrispiech.github.io/probabilityForComputerScientists/img/chapters/digitalPictures.png](https://chrispiech.github.io/probabilityForComputerScientists/img/chapters/digitalPictures.png)
    
    Answer: We can use the step rule of counting. An image can be created one pixel at a time, step by step. Each time we choose a pixel you can select its color out of 17 million choices. An array of 𝑛 pixels produces (17 million)𝑛 different pictures. (17 million)12 ≈ 1086, so the tiny 12-pixel grid produces a million times more pictures than the number of atoms in the universe! How about the 300 pixel array? It can produce 102167 pictures.
    
- Or rule of counting
    
    If you want to consider the total number of unique outcomes, when outcomes can come from source 𝐴 **or** source 𝐵, then the equation you use depends on whether or not there are outcomes which are both in 𝐴 and 𝐵. If not, you can use the simpler "Mutually Exclusive Counting" rule. Otherwise you need to use the slightly more involved Inclusion Exclusion rule.
    
    ***Definition***: Mutually Exclusive Counting
    
    If the outcome of an experiment can either be drawn from set 𝐴 or set 𝐵, where none of the outcomes in set 𝐴 are the same as any of the outcomes in set 𝐵 (called mutual exclusion), then there are |𝐴or𝐵|=|𝐴|+|𝐵| possible outcomes of the experiment.
    
    ***Example***: Sum of Routes. A route finding algorithm needs to find routes from Nairobi to Dar Es Salaam. It finds routes that either pass through Mt Kilimanjaro or Mombasa. There are 20 routes that pass through Mt Kilimanjaro, 15 routes that pass through Mombasa and 0 routes which pass through both Mt Kilimanjaro and Mombasa. How many routes are there total?
    
    ---
    
    ***Solution***
    
    : Routes can come from either Mt Kilimanjaro
    
    **or**
    
    Mombasa. The two sets of routes are mutually exclusive as there are zero routes which are in both groups. As such the total number of routes is addition: 20 + 15 = 35.
    
    ***Definition***: Inclusion Exclusion Counting
    
    If the outcome of an experiment can either be drawn from set 𝐴 or set 𝐵, and sets 𝐴 and 𝐵 may potentially overlap (i.e., it is not the case that 𝐴 and 𝐵 are mutually exclusive), then the number of outcomes of the experiment is |𝐴or𝐵|=|𝐴|+|𝐵|−|𝐴and𝐵|.
    
    Note that the Inclusion-Exclusion Principle generalizes the Sum Rule of Counting for arbitrary sets 𝐴 and 𝐵. In the case where 𝐴and𝐵=∅, the Inclusion-Exclusion Principle gives the same result as the Sum Rule of Counting since |𝐴and𝐵|=0.
    
    How do deal with overcounting 
    If you can argue that you have over-counted each element the same multiple number of times, you can simply correct by using division. If you can count exactly how many elements were over-counted you can correct using subtraction.
    
-