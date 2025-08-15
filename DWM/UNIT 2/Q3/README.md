# **Handling Missing Values in Real-World Data**

In real-world data, tuples with missing values for some attributes are a common occurrence. Choosing an appropriate method to handle missing data depends on the data mining goal and the domain context.
Following are the **different ways for handling missing values in databases**:

---

## **1. Ignore the Data Row**

- In case of classification, suppose a class label is missing for a row, such a data row could be ignored.
- If many attributes within a row are missing, the row can be ignored.
- If the percentage of such rows is high, it will result in poor performance.

**Example:**
Suppose we have to build a model for predicting student success in college.

- A student’s database may have information about age, score, address, etc., and a column classifying their success in college as “LOW”, “MEDIUM” and “HIGH”.
- In this data, rows in which the success column is missing are of no use in the model; therefore, they can be ignored.

---

## **2. Fill the Missing Values Manually**

- This involves manually entering missing attribute values by checking original sources.
- **Not feasible** for large datasets and also time-consuming.

---

## **3. Use a Global Constant to Fill in Missing Values**

- When missing values are difficult to predict, a global constant value like `"unknown"`, `"N/A"` or `"minus infinity"` can be used to fill all the missing values.

**Example:**
In the students database, if the address attribute is missing for some students, it may not make sense to predict these values.

- Instead, a global constant can be used.

---

## **4. Use Attribute Mean**

- For missing values, the **mean** or **median** of the attribute’s existing values can be used as a replacement.

**Example:**
In a database of family incomes, missing income values can be replaced with the **average income**.

---

## **5. Use the Most Frequent Value**

- Replace missing values with the **most common (mode)** value of the attribute in the dataset.
- Works well for nominal or categorical attributes.

**Example:**
If “city” is missing in a customer database, and most customers live in “New York”, then the missing city value can be replaced with “New York”.

---

## **6. Predict the Missing Value**

- Use **predictive models** such as regression, decision trees, or k-nearest neighbor algorithms to estimate missing values.
- The prediction is based on other known attribute values in the same tuple.

**Example:**
If “age” is missing for a customer, but their “income” and “education level” are known, a predictive model can estimate the most probable age.

---

**Summary:**
The method chosen for handling missing data depends on:

- Dataset size
- Importance of the missing attribute
- Feasibility of accurate replacement
  While ignoring data is sometimes acceptable, more often **imputation techniques** like constants, statistical measures, or predictive modeling are used to preserve as much information as possible.

---
