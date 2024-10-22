
### 2. **Random Variables and Distributions**

- **Random Variables**: Variables that represent outcomes of a probabilistic experiment.
  
  - **Discrete Random Variable**: Takes on a countable number of distinct values (e.g., number of heads when flipping a coin three times).
  
    - **Example**: Let \( X \) be the number of heads in three coin flips. Possible values of \( X \) are 0, 1, 2, 3.
    - **Interview Question**: *"What is the expected number of heads when flipping a fair coin three times?"*
      - **Solution**: $\( E(X) = \sum_{x} x \cdot P(X = x) \)$. Calculate this using the probabilities of getting 0, 1, 2, or 3 heads.
  
  - **Continuous Random Variable**: Takes on an uncountable number of values (e.g., the exact time a bus arrives).
  
    - **Example**: Let \( Y \) represent the height of students in a school, which can take any value within a range.
    - **Interview Question**: *"If the height of students is normally distributed with a mean of 170 cm and a standard deviation of 10 cm, what is the probability that a randomly selected student is taller than 180 cm?"*
      - **Hint**: Use the standard normal distribution and Z-scores.

- **Probability Mass Function (PMF)**: Describes the probability of each possible value of a discrete random variable.
  
  - **Example**: The PMF of rolling a fair 6-sided die is:
    $\[
    P(X = x) = \frac{1}{6} \quad \text{for } x \in \{1, 2, 3, 4, 5, 6\}
    \]$

- **Probability Density Function (PDF)**: Describes the probability of a continuous random variable falling within a certain range.
  
  - **Example**: If \( Y \) is normally distributed, its PDF is:
    $\[
    f(y) = \frac{1}{\sqrt{2 \pi \sigma^2}} e^{-\frac{(y - \mu)^2}{2 \sigma^2}}
    \]$
    where $\( \mu \)$ is the mean and $\( \sigma \)$ is the standard deviation.
  
  - **Interview Question**: *"Explain the difference between PMF and PDF."*

### 3. **Common Probability Distributions**

- **Binomial Distribution**: Models the number of successes in \( n \) independent Bernoulli trials (e.g., flipping a coin \( n \) times).

  - **Example**: The probability of getting exactly 3 heads in 5 flips of a fair coin:
    $\[
    P(X = 3) = \binom{5}{3} \cdot (0.5)^3 \cdot (0.5)^2 = 10 \cdot 0.125 = 0.3125
    \]$
  
  - **Interview Question**: *"A factory produces 95% non-defective items. If a sample of 10 items is taken, what is the probability that exactly 9 of them are non-defective?"*

- **Poisson Distribution**: Models the number of events in a fixed interval of time or space.

  - **Example**: The number of customer arrivals at a bank per hour.
    - If the average number of arrivals per hour is 5, the probability of getting exactly 3 arrivals in an hour is:
      $\[
      P(X = 3) = \frac{5^3 e^{-5}}{3!} = 0.1404
      \]$

  - **Interview Question**: *"If a website gets an average of 2 user signups per minute, what is the probability of getting exactly 5 signups in a given minute?"*

- **Normal Distribution**: Characterized by its bell-shaped curve; many natural phenomena follow this distribution.

  - **Example**: Heights of people, test scores, measurement errors.
    - If $\( X \sim N(\mu = 0, \sigma = 1) \)$, find $\( P(X > 1.96) \)$.
    - **Solution**: Use the standard normal table or calculator to find the area under the curve.
  
  - **Interview Question**: *"Why is the normal distribution important in statistics?"*

### 4. **Expectation and Variance Rules**

- **Expected Value (Mean)**: The average or mean value of a random variable \( X \).

  - **Example**: The expected number of heads when flipping a fair coin twice.
    - If \( X \) is the number of heads, then:
      $\[
      E(X) = 0 \cdot \frac{1}{4} + 1 \cdot \frac{1}{2} + 2 \cdot \frac{1}{4} = 1
      \]$
  
  - **Interview Question**: *"Calculate the expected value of rolling a fair 6-sided die."*
    - **Solution**: $\( E(X) = \sum_{x=1}^6 x \cdot \frac{1}{6} = 3.5 \)$.

- **Variance and Standard Deviation**: Measure the spread or variability of a random variable.
  
  - **Example**: The variance of rolling a fair 6-sided die is:
    $\[
    \text{Var}(X) = E(X^2) - (E(X))^2 = \frac{1^2 + 2^2 + 3^2 + 4^2 + 5^2 + 6^2}{6} - 3.5^2 = 2.92
    \]$
  
  - **Interview Question**: *"Explain why variance is important and how it differs from standard deviation."*

### 5. **Central Limit Theorem (CLT)**

- States that the sum (or average) of a large number of independent, identically distributed random variables is approximately normally distributed, regardless of the original distribution.

  - **Example**: The average height of 100 randomly selected people is approximately normally distributed, even if individual heights are not.
  
  - **Interview Question**: *"Why is the Central Limit Theorem important in statistical inference?"*
    - **Answer**: It allows us to use normal distribution techniques for constructing confidence intervals and hypothesis tests, even for non-normal populations.

### 6. **Hypothesis Testing and p-values**

- **Hypothesis Testing**: Method for testing a claim about a population.

  - **Example**: Testing if a coin is fair based on 100 flips.
    - Null hypothesis (\( H_0 \)): The coin is fair (\( p = 0.5 \)).
    - Alternative hypothesis (\( H_1 \)): The coin is biased (\( p \neq 0.5 \)).
  
  - **Interview Question**: *"What is a p-value and how do you interpret it in hypothesis testing?"*
    - **Answer**: The p-value indicates the probability of obtaining a test statistic at least as extreme as the one observed, assuming \( H_0 \) is true. A low p-value (e.g., < 0.05) suggests rejecting \( H_0 \).

### 7. **Maximum Likelihood Estimation (MLE)**

- A method for estimating parameters of a distribution by finding the parameter values that maximize the likelihood function.

  - **Example**: Estimating the mean of a normal distribution given a set of samples.
  
  - **Interview Question**: *"What is Maximum Likelihood Estimation, and how is it used in parameter estimation?"*

