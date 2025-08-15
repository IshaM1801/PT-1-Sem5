# **Normalization Techniques**

Normalization is a technique often applied as part of **data preprocessing** in data mining.
It is used to scale the values of numeric attributes into a specific range, improving the accuracy and efficiency of mining algorithms.
When attributes are measured on different scales, normalization ensures that no attribute dominates simply because of its scale.

The main types of normalization techniques are:

---

## **1. Min–Max Normalization**

- **Definition:**
  Performs a linear transformation on the original data.
  Values are mapped to a specified range $[new_{min}, new_{max}]$.

- **Formula:**

  $$
  v' = \frac{v - min_A}{max_A - min_A} \times (new_{max} - new_{min}) + new_{min}
  $$

  where:
  $v$ = original value
  $min_A$, $max_A$ = minimum and maximum values of attribute A

- **Example:**
  Suppose the range of age is 20 to 60.
  To map age = 30 to the range \[0, 1]:

  $$
  v' = \frac{30 - 20}{60 - 20} \times (1 - 0) + 0 = 0.25
  $$

- **Uses:**
  Preserves relationships among the original data values.
  Works well when the minimum and maximum are known and fixed.

---

## **2. Z–Score Normalization (Zero–Mean Normalization)**

- **Definition:**
  Normalizes values based on the **mean** and **standard deviation** of the attribute.
  The resulting attribute values have a mean of 0 and a standard deviation of 1.

- **Formula:**

  $$
  v' = \frac{v - \bar{A}}{\sigma_A}
  $$

  where:
  $v$ = original value
  $\bar{A}$ = mean of attribute A
  $\sigma_A$ = standard deviation of attribute A

- **Example:**
  If mean ($\bar{A}$) = 54, standard deviation ($\sigma_A$) = 5, and value $v$ = 50:

  $$
  v' = \frac{50 - 54}{5} = -0.8
  $$

- **Uses:**
  Appropriate when the minimum and maximum values are unknown or when the attribute contains outliers.

---

## **3. Decimal Scaling Normalization**

- **Definition:**
  Moves the decimal point of attribute values.
  The number of decimal points moved depends on the maximum absolute value of the attribute.

- **Formula:**

  $$
  v' = \frac{v}{10^j}
  $$

  where $j$ is the smallest integer such that $|v'| < 1$.

- **Example:**
  If the maximum absolute value of A is 986, then $j = 3$.
  For value 986:

  $$
  v' = \frac{986}{10^3} = 0.986
  $$

- **Uses:**
  Simple method; good for attributes with known bounded values.

---

## **Summary Table**

| Technique       | Formula                                                                | Preserves?            | When to Use                       |
| --------------- | ---------------------------------------------------------------------- | --------------------- | --------------------------------- |
| Min–Max         | $\frac{v - min}{max - min} \times (new_{max} - new_{min}) + new_{min}$ | Value relationships   | Known min & max                   |
| Z–Score         | $\frac{v - mean}{std.dev}$                                             | Relative distribution | Unknown min/max, outliers present |
| Decimal Scaling | $\frac{v}{10^j}$                                                       | Magnitude order       | Bounded numeric values            |

---
