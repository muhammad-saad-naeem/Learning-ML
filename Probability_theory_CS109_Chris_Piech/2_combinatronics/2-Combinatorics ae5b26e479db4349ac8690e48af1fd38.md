# 2-Combinatorics

Created: June 29, 2024 12:37 PM
Class: Probabability Theory - CS109
AI summary: This document discusses permutations of distinct objects, permutations of indistinct objects, combinations of distinct objects, and the bucketing of distinct items. It provides definitions, examples, and solutions for each concept.

## **Permutations of Distinct Objects**

***Definition***: Permutation Rule

A permutation is an ordered arrangement of n distinct objects. Those 𝑛 objects can be permuted in 𝑛⋅(𝑛–1)⋅(𝑛–2)⋯2⋅1=𝑛! ways.

This changes slightly if you are permuting a subset of distinct objects, or if some of your objects are indistinct. We will handle those cases shortly! Note that unique is a synonym for distinct.

**Example**: How many unique orderings of characters are possible for the string "BAYES"? **Solution**: Since the order of characters is important, we are considering all permutations of the 5 distinct characters B, A, Y, E, and S: 5!=120.

Once you choose the first letter, the next step only has 4 possible options, once you choose one out of those 4, the next one only has 3 options and so on. 5.4.3.2.1= 5!. This is like counting where choosing one leaves one less option for the next step. 

## **Permutations of Indistinct Objects**

***Definition***: Permutations of In-Distinct Objects

Generally when there are 𝑛 objects and: 𝑛1 are the same (indistinguishable) and 𝑛2 are the same and ... 𝑛𝑟 are the same, then the number of distinct permutations is:

𝑛! / n1!. n2! …. nr!

**Example:**

How many *distinct* orderings of characters are possible for the string "MISSISSIPPI"?

---

**Solution:**

In the case of the string "MISSISSIPPI", we should separate the characters into four distinct groups of indistinct characters: one "M", four "I"s, four "S"s, and two "P"s. The number of distinct orderings are:

11!/1!4!4!2!=34,650

**Example:** Consider the 4-digit passcode smart-phone from before. How many distinct passcodes are possible if there are 3 smudges over 3 digits on the screen?

**Example:**

Consider the 4-digit passcode smart-phone from before. How many distinct passcodes are possible if there are 3 smudges over 3 digits on the screen?

---

**Solution:**

One of 3 digits is repeated, but we don't know which one. We can solve this by making three cases, one for each digit that could be repeated (each with the same number of permutations). Let

𝐴,𝐵,𝐶

represent the 3 digits, with

𝐶

repeated twice. We can initially pretend the two

𝐶

's are distinct

[𝐴,𝐵,𝐶1,𝐶2]

. Then each case will have 4! permutations: However, then we need to eliminate the double-counting of the permutations of the identical digits (one

𝐴

, one

𝐵

, and two

𝐶

's):

4!2!⋅1!⋅1!

Adding up the three cases for the different repeated digits gives

3⋅4!2!⋅1!⋅1!=3⋅12=36

---

**Part B:**

What if there are 2 smudges over 2 digits on the screen?

---

**Solution:**

There are two possibilities: 2 digits used twice each, or 1 digit used 3 times, and other digit used once.

4!2!⋅2!+2⋅4!3!⋅1!=6+(2⋅4)=6+8=14

## **Combinations of Distinct Objects**

***Definition***: Combinations

A combination is an unordered selection of r objects from a set of n objects. If all objects are distinct, and objects are not "replaced" once selected, then the number of ways of making the selection is:

Number of unique selections=𝑛!/𝑟!(𝑛−𝑟)!=(𝑛  𝑟)

Here are all the 10=(53) ways of choosing three items from a list of 5 unique numbers:

```python
# Get all ways of chosing three numbers from [1,2,3,4,5]>>> list(itertools.combinations([1,2,3,4,5], 3))
[(1, 2, 3), (1, 2, 4), (1, 2, 5), (1, 3, 4), (1, 3, 5), (1, 4, 5), (2, 3, 4), (2, 3, 5), (2, 4, 5), (3, 4, 5)]Explain

```

Notice how order doesn't matter. Since (1, 2, 3) is in the set of combinations, we don't also include (3, 2, 1) as this is considered to be the same selection. Note that this formula does not work if some of the objects are indistinct from one another.

**Bucketing Distinct Items:**

Suppose you want to place 𝑛 distinguishable items into 𝑟 containers. The number of ways of doing so is:

𝑟𝑛

You have 𝑛 steps (place each item) and for each item you have 𝑟 choices

**Problem:**

Say you want to put 10 distinguishable balls into 5 urns (No! Wait! Don't say that! Not urns!). Okay, fine. No urns. Say we are going to put 10 different strings into 5 buckets of a hash table. How many possible ways are there of doing this?

---

**Solution:** You can think of this as 10 independent experiments each with 5 outcomes. Using our rule for bucketing with distinct items, this comes out to 510.

![Untitled](2-Combinatorics%20ae5b26e479db4349ac8690e48af1fd38/Untitled.png)