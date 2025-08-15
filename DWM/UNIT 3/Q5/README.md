## **Attribute Selection Measures of Decision Tree Classifier**

## In Decision Tree classification, **attribute selection measures** are used to select the attribute that best splits the data into different classes. Two widely used attribute selection measures are **Gini Index** and **Information Gain**.

### **(1) Gini Index (IBM Intelligent Miner)**

- Suppose all attributes are continuous-valued.
- Assume that each value of attribute has many possible split.
- It can be adapted for categorical attributes.
- An alternative method to information gain is called the **gini index**.
- Gini is used in **CART (Classification and Regression Trees)**, IBM’s Intelligent Miner system, SPRINT (Scalable PaRallelizable INduction of decision Trees).
- If a dataset **T** contains examples from **n** classes, gini index, gini(T) is defined as:

$$
\text{gini}(T) = 1 - \sum_{j=1}^n p_j^2
$$

Where, $p_j$ is the relative frequency of class $j$ in $T$.

- gini(T) is minimized if the classes in T are skewed.

After splitting T into two subsets T₁ and T₂ with sizes N₁ and N₂, the gini index of the split data is defined as:

$$
\text{gini}_{split}(T) = \frac{N_1}{N} \text{gini}(T_1) + \frac{N_2}{N} \text{gini}(T_2)
$$

---

**Example using Gini Index:**

Consider the dataset **D**:

| Outlook  | Temperature | Humidity | Windy | Play? |
| -------- | ----------- | -------- | ----- | ----- |
| Sunny    | Hot         | High     | False | No    |
| Sunny    | Hot         | High     | True  | No    |
| Overcast | Hot         | High     | True  | Yes   |
| Rainy    | Mild        | High     | False | Yes   |
| Rainy    | Cool        | Normal   | False | Yes   |
| Rainy    | Cool        | Normal   | True  | No    |
| Overcast | Cool        | Normal   | True  | Yes   |
| Sunny    | Mild        | High     | False | No    |
| Sunny    | Cool        | Normal   | False | Yes   |
| Rainy    | Mild        | Normal   | False | Yes   |
| Sunny    | Mild        | Normal   | True  | Yes   |
| Overcast | Mild        | High     | True  | Yes   |
| Overcast | Hot         | Normal   | False | Yes   |
| Rainy    | Mild        | High     | True  | No    |

**Total for node D:**

$$
\text{gini}(D) = 1 - \text{sum}(p_1^2, p_2^2, \dots, p_n^2)
$$

Here $n = 2$ classes (Yes, No).
For the above dataset:

$$
\text{gini}(D) = 1 - \left[ \left(\frac{9}{14}\right)^2 + \left(\frac{5}{14}\right)^2 \right] = 0.459
$$

---

### **(2) Information Gain (ID3 / C4.5)**

- All attributes are believed to be categorical.
- It can be adapted for continuous-valued attributes.
- The attribute which has the highest **information gain** is selected for split.
- Assume there are two classes, P and N.

Suppose we have **S** samples, out of these **p** samples belong to class P and **n** samples belong to class N. The amount of information needed to decide if a random example in S belongs to P or N is:

$$
I(p, n) = -\frac{p}{p+n} \log_2 \frac{p}{p+n} - \frac{n}{p+n} \log_2 \frac{n}{p+n}
$$

If attribute A partitions S into subsets $S_1, S_2, \dots, S_v$, and $S_i$ contains $p_i$ examples of P and $n_i$ examples of N, the **expected information** is:

$$
E(A) = \sum_{i=1}^{v} \frac{p_i + n_i}{p + n} \times I(p_i, n_i)
$$

**Entropy (E):**
Expected amount of information (in bits) needed to assign a class under the optimal, shortest-length code.

**Information Gain:**

$$
\text{Gain}(A) = I(p, n) - E(A)
$$

---

✅ **In Decision Trees:**

- **Gini Index** → used in CART, selects the attribute with the **smallest** gini split value.
- **Information Gain** → used in ID3/C4.5, selects the attribute with the **highest** gain value.

---
