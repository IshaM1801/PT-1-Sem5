# Different Data Visualization Techniques

## (i) Dimensional stacking

- In dimension stacking, partition the n-dimensional attribute space in 2-dimensional subspaces.
- Attribute values are partitioned into various classes.
- Each element is a two dimensional space as an xy plot.
- Mark the important attributes and are used on the outer levels.

---

## (ii) Mosaic plot

- Mosaic plots give a graphical illustration of the successive decompositions.
- Rectangles are used to represent the count of categorical data and at every stage rectangles are split parallel.
- To draw a mosaic plot, a contingency table of data and chosen ordering of variable with the response variable is required.

**Example:**  
In Titanic example, out of all women, 67% survived which is coded as 1 and 33% died which is coded as 0.

- The women bar shows as 67/33 split.
- Among men, only 17% survived, so this bar shows a 17/83 split.

---

## (iii) Worlds-within-worlds

- Worlds within worlds are useful to generate an interactive hierarchy of display.
- Innermost world must have a function and two most important parameters.
- Remaining parameters fix with constant value.
- Through this N-vision of data are possible like data glove and stereo displays, including rotation, scaling (inner) and translation (inner/outer).
- Using queries static interaction is also possible.

---

## (iv) Tree-map

- Tree maps’ visualization techniques are well suited for displaying large amounts of hierarchical structured data.
- The visualization space is divided into multiple rectangles that are sized and ordered according to a quantitative variable.
- The levels in the hierarchy are seen rectangles containing other rectangles.
- Each set of rectangles on the same level in the hierarchy represents a column or an expression in a data set.

**Example:**  
In Fig. 3.10.9, a rectangle representing "global" below which there are rectangles representing continents, which contain several rectangles representing countries in that continent.

- Each rectangle representing a country may in turn contain rectangles representing states in these countries.

---

## (v) Visualizing complex data and relations

- This technique is useful to visualize non-numeric data such as text, pictures, blog entries, and product reviews.
- A tag cloud is a visualization method which helps to understand the information of user generated tags.
- Arrange the tags alphabetically or with the user preferences with different font sizes and colors.
- Tag clouds are used in two ways:
  1. With the size of tag, we can find out how many times that tag is applied on that item by different users.
  2. Or that tag has been applied to how many items.
