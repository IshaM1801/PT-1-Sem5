## **Naïve Bayes Classification Algorithm**

### **4.2.2(A) Bayes Theorem**

- It is also known as **Bayes Rule**.
- Bayes theorem is used to find conditional probabilities.
- The conditional probability of an event is a likelihood obtained with the additional information that some other event has previously occurred.
- **P(X|Y)** is the conditional probability of event X occurring for the event Y which has already occurred.

$$
P(X|Y) = \frac{P(X \text{ and } Y)}{P(A)}
$$

- An initial probability is called as **apriori probability** which we get before any additional information is obtained.
- The probability is called as a **posterior probability** value which we get or revise after any additional information is obtained.

---

### **4.2.2(B) Basics of Bayesian Classification**

- **Probabilistic learning** : Explicit probabilities are calculated for Hypothesis.
- **Incremental** : The probability of a hypothesis whether it is correct can be incrementally increased or decreased by each training example.
- **Probabilistic prediction** : Multiple hypothesis can be predicted by their probability weight.
- **Meta-classification** : The outputs of several classifiers can be combined, e.g., by multiplying the probabilities that all classifiers predict for a given class.
- **Standard** : The computationally intractable Bayesian methods provide a standard of optimal decision making against which other methods can be measured.

Given training data D, posteriori probability of a hypothesis h, **P(h|D)** follows the Bayes theorem,

$$
P(h|D) = \frac{P(D|h) \cdot P(h)}{P(D)}
$$

Where,

- **P(h)** : Independent probability of h; prior probability
- **P(D)** : Independent probability of D
- **P(D|h)** : Conditional probability of D given h; likelihood
- **P(h|D)** : Conditional probability of h given D; posteriori probability

---

### **Practical difficulties**

- Require initial knowledge of many probabilities.
- Significant computational cost.

---

### **4.2.2(C) Naïve Bayes Classifier : Example**

**Training set is given for play-tennis problem**:
We have a dataset containing weather conditions such as **Outlook**, **Temperature**, **Humidity**, and **Windy**, along with a class label “Play” (Yes or No).

The Naïve Bayes algorithm works as follows:

1. From the training set, calculate the **prior probabilities** for each class.
   Example:

   $$
   P(Yes) = \frac{\text{Number of Yes outcomes}}{\text{Total number of instances}}
   $$

   $$
   P(No) = \frac{\text{Number of No outcomes}}{\text{Total number of instances}}
   $$

2. For each attribute value in the new test instance, calculate the **likelihood** for each class.
   Example:

   $$
   P(\text{Outlook=Sunny} | Yes) = \frac{\text{Number of Yes outcomes with Sunny outlook}}{\text{Total Yes outcomes}}
   $$

3. Multiply the likelihoods for all attributes with the prior probability of that class to get the **posterior probability**.

   $$
   P(Yes|X) \propto P(\text{Outlook} | Yes) \cdot P(\text{Temperature} | Yes) \cdot P(\text{Humidity} | Yes) \cdot P(\text{Windy} | Yes) \cdot P(Yes)
   $$

4. Compare the posterior probabilities for each class (Yes and No) and choose the class with the higher probability as the prediction.

---

### **Key Assumption**

- **Conditional Independence**: Naïve Bayes assumes that the effect of a variable value on a given class is independent of the values of other variables.

---
