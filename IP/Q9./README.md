In HTML tables, cells are created using <td> (table data) or <th> (table header) elements. By default, each cell occupies exactly one column and one row. However, sometimes we need a single cell to stretch over multiple columns or multiple rows to logically group related data. This is achieved using the colspan and rowspan attributes.

colspan Attribute
Purpose: Merges two or more columns into a single cell.

Working: When colspan="n" is applied to a <td> or <th>, the cell extends horizontally to span n columns.

Example Use Case: In a table header where the label “Grades” applies to two separate columns (e.g., Exam 1 and Exam 2), colspan="2" combines them under one heading.

rowspan Attribute
Purpose: Merges two or more rows into a single cell.

Working: When rowspan="n" is applied to a <td> or <th>, the cell extends vertically to span n rows.

Example Use Case: In a student table where “Undergraduates” is a category for two different students, rowspan="2" merges those two rows into one cell in the first column.

Example Code:

<table border="5">
<caption>COSC 400 Student Grades</caption>
<tr>
    <td>&nbsp;</td><td>&nbsp;</td><th colspan="2">Grades</th>
</tr>
<tr>
    <td>&nbsp;</td><th>Student</th><th>Exam 1</th><th>Exam 2</th>
</tr>
<tr>
    <th rowspan="2">Undergraduates</th><td>Kim</td><td>100</td><td>89</td>
</tr>
<tr>
    <td>Sandy</td><td>78</td><td>92</td>
</tr>
<tr>
    <th>Graduates</th><td>Taylor</td><td>83</td><td>73</td>
</tr>
</table>

Explanation of the Example:

In the first row, <th colspan="2">Grades</th> merges the two columns Exam 1 and Exam 2 under a single heading “Grades.”
In the third row, <th rowspan="2">Undergraduates</th> merges the category cell for Kim and Sandy so that the label “Undergraduates” appears only once but applies to both rows.
The use of &nbsp; in empty <td> cells ensures that borders and rules remain visible even in otherwise blank cells.
Advantages:
Helps group related information in tables, improving readability.
Reduces repetition of headings or labels.
Allows complex table structures without increasing the number of rows or columns unnecessarily.
