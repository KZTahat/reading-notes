# HTML Tables; JS Constructor Functions
<!-- Chapter 6: “Tables” (pp.126-145) -->
## Tables
There are several types of information that need to be displayed in a grid or table. For example: sports results, stock reports, train timetables.A table represents information in a grid format. Examples of tables include financial reports, TV schedules, and sports results.<br />
- ****Basic Table Structure**:
    The ```<table>``` element is used to create a table. The contents of the table are written out row by row.
    ```<tr>``` : You indicate the start of each row using the opening ```<tr>``` tag. (The tr stands for table row.) It is followed by one or more ```<td>``` elements (one for each cell in that row). At the end of the row you use a closing ```</tr>``` tag. Each cell of a table is represented using a ```<td>``` element. (The td stands for table data.)<br />

- **Table Headings**:
    The ```<th>``` element is used just like the ```<td>``` element but its purpose is to represent the heading for either a column or a row. (The th stands for table heading.) Even if a cell has no content, you should still use a ```<td>``` or ```<th>``` element to represent the presence of an empty cell otherwise the table will not render correctly. (The first cell in the first row of this example shows an empty cell.)Using ```<th>``` elements for headings helps people who use screen readers, improves the ability for search engines to index your pages, and also enables you to control the appearance of tables better when you start to use CSS.You can use the scope attribute on the ```<th>``` element to indicate whether it is a heading for a column or a row. It can take the values: row to indicate a heading for a row or col to indicate a heading for a column.<br />


[Home]( https://kztahat.github.io/reading-notes/)