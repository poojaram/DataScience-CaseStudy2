# Foundational Stats

## Overview

The purpose of this assignment is to ensure that you have a foundational understanding of probability and statistics such that you can appropriately interpret and perform analyses. The [open-intro-stats](open-intro-stats.pdf) textbook included in this repository is the **strongly suggested** resource for answering questions (i.e., rather than wikipedia / misc. google searches.). You are welcome to use other resources or prior knowledge, but we expect your answers to be consistent (and as **thorough**) as captured in the book. Obviously, we **do not expect** you to read the entire book, but instead to **use it as a reference** to guide you through answering the following questions.

## Probability Basics (Ch. 2)

For each of the following questions, compute the answer. Then, using the appropriate vocabulary, describe how you computed you answer in ~1 - 2 sentences

1. What is the probability of rolling an odd number _or_ a 4 if you roll a (fair) six-sided die? _(7 points)_

**Answer:**
There are totally 6 posible outcomes when we roll a six-sided die and they are - {1, 2, 3, 4, 5, 6}
Let us call rolling an odd number _or_ a 4 a _favourable outcome_. Then we have the following as the possible favourable outcomes.
Favourable outcomes - {1, 3, 5, 4}
Probability(rolling an odd number or a 4) = (No. of favourable outcomes) / (Total Number of outcomes) = 4/6 = 2/3
Thus, **Probability(rolling an odd number or a 4) = 2/3 or 66.667%**.

2. What is the probability of rolling an odd number _or_ a 4 in **two rolls** of a (fair) six-sided die? May require outside reference. _(7 points)_

**Answer:**
There are totally 21 posible outcomes when we roll a six-sided die and they are -
<dd>{(1,1), (1,2), (1,3), (1,4), (1,5),(1,6), </dd>
<dd>(2,2), (2,3), (2,4), (2,5), (2,6), </dd>
<dd>(3,3), (3,4), (3,5), (3,6), </dd>
<dd>(4,4), (4,5), (4,6), </dd>
<dd>(5,5), (5,6), </dd>
<dd>(6,6)} </dd>

Let us call rolling of an odd number or 4 a _favourable outcome_. Then we have the following as the possible outcomes:
Favourable outcomes - {(1,1), (1,2), (1,3), (1,4), (1,5), (1,6), (2,3), (2,4), (2,5), (3,3), (3,4), (3,5), (3,6), (4,4), (4,5), (4,6), (5,5), (5,6)}
Probability(Favourable outcomes) = (No. of Favourable Outcomes) / (Total Number of Outcomes) = 18/21 = 6/7
Thus, **Probability(rolling an odd number or a 4) = 6/7 or 85.71%**.

3. Imagine a bowl with three balls in it: one red, one blue, and one yellow. What is the probability of removing a red ball from the  bowl (without replacing it), _and then_ removing a yellow ball? _(7 points)_

**Answer:**
There are 3 balls in the ball and each of them are unique. So, the probabiity of pick up a red/blue/yellow ball is 1/3. Now, in the first try, the probability of removing a red ball from the bowl is 1/3. Since, the red ball is not replaced, we are left with 2 balls in the bowl, and the probability of choosing a yellow ball is 1/2.

Removing a red ball the red ball and the removal of yellow ball are dependent(inclusive) events, since the red ball is not replaced. So,
**Probability(removing a red ball ball, and then a yellow ball w/o replacing) = (1/3)*(1/2) = 1/6 or 16.67%**

4. Example 2.54 (p.98) walks through the use of **Bayes' Theorem** to answer the question, _what is the probability that a woman has breast cancer given her positive mammogram results_? In addition to the false positive/negative test rate, what other information is necessary to compute this probability? _(7 points)_

**Answer:**

The probability is presented as a table below:

|Mammogram Result |Cancer              |No-Cancer           |
|-----------------|--------------------|--------------------|
|                 | (0.0035)           | (0.9965)           |
|Positive         |0.89                |0.07                |
|                 |0.89x0.0035=0.003115|0.07x0.9965=0.69755 |
|Negative         |0.11                |0.93                |
|                 |0.11x0.0035=0.000385|0.93x0.9965=0.926745|

**Thus, the probability that a woman has breast cancer given her positive mammogram results is 0.31% of the population**
In addition to false positive/negative test rate, we needed the information on what percent of women population in canada over 40 are prone to devolop cancer in any given year. We are given that "In Canada, about 0.35% of women over 40 will develop breast cancer in any given year".

## Probability Distributions (Ch. 3)

1. What are the **parameters** of the normal distribution, and how does changing each one affect the shape of the distribution? _(7 points)_

**Answer:**
The normal distribution can be adjusted using two parameters: _Mean_ and _Standard Deviation_
Changing the mean shifts the bell curve to the left or right, while changing the standard deviation stretches or constricts the curve.

2. If the distribution of a variable is normal (or nearly normal) what does that empower us to do? _(7 points)_

**Answer:**
A variable being normal can empower us to find the normal modal percentiles. This helps us calculate what the chance of someone being above, below, or in-between two values is. For example if if we have the mean and standard deviation of an exam's score, we can find out what the odds are that someone will score above or below a particular given score. Furthermore, if the given data is normally distributed we can perform hypothesis testing by estimating the p-value. This helps us gain some inference regarding the data and the patters/information observed. We can also use the same z-score estimated to find the probability of the occurrence of a part of the data given that they are normally distributed.

3. Imagine two instructors that teach the same course, both of whom have a normal distribution for their students' grades. In the first instructor's course, the mean student grade is 93%, with a standard deviation of 8%. In the second instructor's course, the mean student grade is 90%, with a standard deviation of 5%. For the students below, What **percentile** of performance did each student achieve (and was, therefore, the "better" student)? _(7 points)_

    - Student 1: received a 96% in Instructor 1's class
    - Student 2: received a 93% in Instructor 2's class

**Answer:**
    - Student 1:
        Z = (x-mean)/std.dev. = (96-93)/8 = 0.375
        Percentile = (0.6443 + 0.6480)/2 = **0.6461**
    - Student 2:
        Z = (x-mean)/std.dev. = (93-90)/5 = 0.60
        Percentile = **0.6179**

**Student 1 did better than 64.61% of the class, where as Student 2 did better than 61.61% of the class. Thus, Student 1 performed better than Student 2.**

4. Imagine you have a job registering people to vote, and you need to register one more person before the end of the day. Based on your work thus far, you know that each person you approach has a **4% probability** of registering to vote with you. What is the **expected number of people** you need to approach before you're likely to get someone to register? Please also include the **standard deviation** around your estimate, and describe how you arrive at your answer, making sure to reference the **type of distribution** this event follows. _(7 points)_

**Answer:**
This question can be answered using Geometric Distribution. We first formalize each trial using Bernoulli Distributioin and then use probability tools to construct the geometric distribution. Here,
_probability(success)_ = probability(registering to vote when approached) = 0.04
_probability(failure)_ = 1 - 0.04 = 0.96

When an individual trial only has two possible outcomes, it is called a Bernoulli random variable.
If we label 1 for success and 0 for failure, then
Mean = E(x) = P(X=0) x 0 + P(X=1) x 1 = 0.96x0 + 0.04x1 = 0.04
Variance = P(X=0)(0-p)^2 + P(X=1)(1-p)^2 = p^2(1-p) + p(1-p)^2 = p(1-p)
Standard Deviation = sqrt(p(1-p)) = 0.1960

5. Continuing from the example above, if I approached 100 people to register to vote, what is the probability that **exactly 4** would register?  What is the **expected number** of people to register? _hint: even though this is the same situation, the questions being asked may be of different distributions_. _(7 points)_

**Answer:**
This problem can be solved using Binomial distribution.
The probability of a single trial  being a success = probability(registering to vote when approached) = 0.04
Then, the probability of observing exactly 4 success from 100 trials = (n! x p^k x (1-p)^(n-k))/(k! x (n-k)!)

Here, n is number of trals = 100, p is the probability = 0.04, and k = 4.
Probaility of observing exactly 4 success from 100 trials = 0.19938

**Therefore, the probability that exactly 4 people would register when 100 people are approached is 19.94%.**


## Foundations for Inference (Ch. 4)
1. Define the terms **standard error** and **standard deviation**. Then, using a hypothetical example _not in the textbook_, describe a situation in which you could compute the two, and highlight how they are different (hint: your answer should include a description of how to generate a **sampling distribution**).  _(7 points)_

**Answer:**
Standard Error - The standard deviation associated with an estimate is called the standard error. It describes the typical error or uncertainty associated with an estimate.
Standard Deviation - The variance is roughly the average squared distance from the mean. The standard deviation is the square root of the variance. The standard deviation is useful when considering how close the data are to the mean.

The standard deviation is a measure of the variability of a random variable. For example, if we collect some data on incomes from a sample of 100 individuals, the sample standard deviation is an estimate of how much variability there is in incomes between individuals.

A standard error is a measure of how precise an estimate is. The estimate itself will be of some parameter of interest, such as a mean, or perhaps a regression coefficient. The standard error is the standard deviation of the estimator in repeated samples from the population. As such, the standard error concerns variability in an estimator from sample to sample.

2. Why is the number 1.96 used for calculating confidence intervals? _(7 points)_

**Answer:**
 1.96 is the value of the 97.5th percentile on the normal distribution, this translates to a 95% confidence interval. Arounf 95% of the data will be within 2 standard deviations from the mean. Now about why only 95% is used as the confidence interval and not 90% or 99%: a 90% interval is not used because they are only within 1 standard deviation of the mean, if we were to take 100 different samples and compute a 90% confidence interval for each sample, then approximately 90 of the 100 confidence intervals will contain the true mean value and there would be a 10% of the values wont, this margin is too high; if a 99% confidence level is used then the confidence intervals would increase.

3. Given the statement, "the mean height of a sample of students was 140cm, with a confidence interval of 130 - 150 cm", interpret the **meaning of the confidence interval**. _(7 points)_

**Answer:**
Assuming a 95% confidence level was chosen to compute the confidence interval, we can say that a 95% confidence interval is a range of values that you can be 95% certain contains the true mean of the population. This is not the same as a range that contains 95% of the values.

4. Imagine you want to evaluate the claim, _the average income for Informatics graduates is $40,000_. If a sample of 200 Informatics graduates returns a mean of $42,000 (sd = $10,000), can we _reject the null hypothesis_ that the average income is not $40,000? Assume you're using confidence intervals as a mechanism for evaluating your hypothesis. _(8 points)_

**Answer:**
Since the sample size is small, our confidence intervals will be large. To avoid very large confidence intervals I will choose 95% as my confidence level. Taking a confidence level of 95% and using z as 1.96 we get the confidence interval as +/- 19.600. This means that with 95% confidence we can say that the average say that the income for Informatics graduates is between $61,000 to $22,400, this interval is too hard for us to conclude that the mean is $40,000 and thus we fail to reject the null hypothesis that the average income is not $40,000.

## Statistical Inference (Ch. 5)

1. Define the **t-distribution**, then describe how it is different from the normal distribution, and why it would be used for analysis.  _(8 points)_

**Answer:**
The normal distribution is used when the population distribution of data is assumed normal. It is characterized by the mean and the standard deviation of the data. A sample of the population is used to estimate the mean and standard deviation. The t statistic is an estimate of the standard error of the mean of the population or how well known is the mean based on the sample size.
Which to use in financial data depends entirely on the question you are trying to answer. If the question concerns the entire population as it is distributed, then the normal distribution should be used. If the question concerns the mean of the population then the t statistic may be used. For the use of either, a larger sample size gives a better result.
The decision to use one or the other requires a clear, logical statement and argument to establish whether to use the t-distribution or the normal distribution. Use of either assumes a normally distributed population.

The t-distribution is similar to normal distribution, but shorter and thicker than a normal distribution, since the sample size we have is only 200 which is relatively small, a t-distribution is helpful for small sample sizes because: observations are more likely to fall beyond two standard deviations from the mean than under the normal distribution(like we saw in the above question the standard deviation is $10,000, the upper bound for the CI is $61,000 which almost falls 2 SDs from the mean). While our estimate of the standard error will be a little less accurate when we are analyzing a small data set, these extra thick tails of the t-distribution are exactly the correction we need to resolve the problem of a poorly estimated standard error.
