# **Types of Attributes**

- An **attribute** is a data field representing a characteristic or feature of a data object.
- Terms such as _attribute_, _dimension_, _feature_, and _variable_ are often used interchangeably:

  - **Data warehousing:** dimension
  - **Machine learning:** feature
  - **Statistics:** variable
  - **Databases:** attribute

- Example: attributes describing a **customer object** → customer ID, name, address.
- Observed values for a given attribute are called **observations**.
- A set of attributes describing an object is an **attribute vector** (or feature vector).
- The type of an attribute is determined by the set of possible values it can have.

---

## **1. Nominal Attributes**

- Values are symbols or names representing categories, codes, or states.
- No meaningful order among values (**categorical attributes**).
- Values are also known as **enumerations**.
- Examples:

  - Hair color → black, brown, blond, red, pink, gray, white.
  - Occupation → professor, dentist, programmer, farmer.

- Numbers may be used to represent categories, but have no mathematical meaning (e.g., black = 0, brown = 1).
- Mean and median cannot be computed; **mode** is meaningful.

---

## **2. Binary Attributes**

- Nominal attributes with **only two categories/states**: 0 or 1.
- 0 = attribute absent, 1 = attribute present.
- **Boolean** if states correspond to _true_ and _false_.
- **Symmetric binary:** both states equally important (e.g., gender: male, female).
- **Asymmetric binary:** outcomes not equally important; rare event coded as 1 (e.g., positive medical test = 1, negative = 0).

---

## **3. Ordinal Attributes**

- Values have a **meaningful order or ranking**, but differences between values are unknown.
- Can be derived from discretization of numeric quantities.
- Examples:

  - Drink size → small, medium, large.
  - Grades → A+, A, A-, B+.
  - Professional rank → assistant, associate, full professor.
  - Survey ratings → 0 (very dissatisfied) to 4 (very satisfied).

- **Mode** and **median** are meaningful; mean is not defined.
- Useful for subjective assessments in surveys.

---

## **4. Numeric Attributes**

- Quantitative, measurable, and represented as integers or real numbers.
- Two subtypes:

### **a) Interval-Scaled Attributes**

- Measured on a scale of equal-size units.
- Values have order and can be positive, zero, or negative.
- Meaningful differences can be compared.
- Examples:

  - Temperature → 20°C is 5°C higher than 15°C.
  - Calendar dates → 2002 and 2022 are 20 years apart.

- Mean, median, and mode are meaningful.

### **b) Ratio-Scaled Attributes**

- Numeric with a **true zero-point**.
- Allow multiplicative comparisons (e.g., one value can be twice another).
- Values are ordered; differences, mean, median, and mode are all meaningful.
- Examples: Height, weight, age, length.

---

## **Summary Table**

| Attribute Type | Ordered? | Meaningful Difference? | True Zero? | Example             |
| -------------- | -------- | ---------------------- | ---------- | ------------------- |
| Nominal        | No       | No                     | No         | Hair color          |
| Binary         | No       | No                     | Sometimes  | Gender, test result |
| Ordinal        | Yes      | No                     | No         | Drink size          |
| Interval       | Yes      | Yes                    | No         | Temperature         |
| Ratio          | Yes      | Yes                    | Yes        | Weight              |

---
