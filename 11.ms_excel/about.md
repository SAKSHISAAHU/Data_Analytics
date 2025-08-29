# **Excel**
- It is mainly used for data storage.
- To create a table in excel, atleast one column or record is required without that it is not possible.
- The cell nomenclusture is done using "column + row" and each cells have values inside them.
- There are various tabs in excel like Home, Insert, Page Layout, Formulas etc.
- When we move from left to right alphabet increases and on top to bottom number increases of the cells.
- 'Paste Special' is used for special pasting,
    - like a column is creted by adding up two column when we copy and paste it to differnt place then the values of that created column shows error because it dosent support the addition as the cell name is change.
- In **home tab**,
    - **"Font section"** is used for changing or modifying the size, color and style of the cell and value of the cell.
    - **"alignment section"** is used for modifying the cell's size, alignment and value's position.
    - **"style section"** is used for conditional formating mean based upon condition highlighting  the cell.

### **Data exploration**
1. *renaming column*
    - any column name is wrong, we rename it just by double clicking on that cell.

2. *unique value*
    - to check the unique value of a column,
        - select that column, then select filter on drill down all the unique value will be shown.

3. *value count*
    - select the column then select 'sort & filters', then on drill dowm on column_name tick mark on specifc category whose value count you want to see then call the records of that category will be seperated and on the bottom right corner we can see the count of that specific category.

4. *missing value*
    - select a cell then write a function '=countblank()' inside that give the column values
    - to extract the missing value first select the column then click on conditional formating then new rule then select 'format that contains' then on format option choose any color then apply and then on drill down of that column click 'choose filter by color'.

5. *wrong data*
    - from unique value we check if a column have wrong data or not.
    - to extract wrong value, on seeing unique just tick only on wrong data it will be seperated then.

6. *wrong data type*
    - there is no concept of data type in excel.

7. *duplicate records*
    - Select your data range, then go to Data tab click on Remove Duplicates and select the columns you want to check.
    
8. *outliers*

### **Functions for data exploration**
1. count() -- only count the column which contains numbers
2. counta() -- count the no. of cells that are not empty
3. countblank() -- count blank cells only
4. len() -- count the no. of character a string have
5. average()
6. mode()
7. median()
8. min()
9. max()
10. stdev() -- calculate sample std dev
11. stdevp() -- calculate population std dev
12. percentile(range,k) -- k= 0.25, 0.50, 0.75, 1 

### **Data cleaning**
1. *wrong data*
    - to fill with different values,
        - first extract the cells or records where values are suppose to be fill then manually fill the values.
    - to fill with same value,
        - first extract the cells or records where values are suppose to be fill then fill value at one cell then drag the cursor till where you want to fill same value.
    - extraction is done by highlighting cells then filter them based on highlight.

2. *duplicates*
    - if the whole record is same with other record then we call one of the record duplicated, that we simply delete by right clicking over that record and delete.

3. *missing values*
    - same as filling data

4. *outliers*
    - first calculate the upper and lower limit of column
    - then apply conditional formating and highlight the cell based upon the upper and lower limit values
        - on conditional formating choose highlight cell then, choose greater than and give upper limit's cell's value name then, choose less than and give lower limit's cell's value name, as it will be adaptable if the columns value change.
    - then filter those cells then, replace the value which are less than the lower limit to lower limit value and if values are greater than the upper limit then to upper limit value.

5. *unimportant column*
    - on column name right click then choose delete.


### **Pivot table**
- It is same as,
    - crosstab & groupby in pandas
    - table & matrix in PowerBI
- applied on the clean data.

- First we have to select the table (by selecting any value and doing cntrl + A) which we want to pivot then, on 'Insert Tab' select 'Pivot Table' then under that click on 'new worksheet' then the pivot table will be created on the new worksheet.

- In the pivot table,
    - whcih ever column we want as the row we drag that column to the 'row labels'. E.g - Region
    - which ever column we want to have values for the row we drag them to the 'value section'. E.g - Sales
    - we can add more than one column in value section. E.g - Sales, Profit
    - we can also add more than one column in 'row lables'. E.g - Region, Segment

        <pre>
        |    Row labels    |     Values     |
        | ---------------- | ---------------|
        | Region | Segment | Sales | Profit |
        |--------|---------|-------|--------|
        | West   | Office  |  ...  |  ...   |
        |        | Home    |  ...  |  ...   |
        |------------------|----------------|
        | East   | Office  |  ...  |  ...   |
        |        | Home    |  ...  |  ...   |
        <pre>

    - We called it Table when we add multiple column in the value section.
    - We called it Matrix, when we add muliple column row label which basically suppose to be sun caegories of one category. 

    - In 'report filter' option we can add that column which we want based upon filter for row labels in pivot table.

### **Calculated measure**
- This will be created using, measures + operators.
    - E.g for a column we calculated the min and max measure, then we want to calculate the range of that column then we will do that as, on a selected cell write **= max value cell's name - min value cell's name**

### **Calculated Field**
- We will first calculate the calculated measure for column's 1st cell then by using the cursor we drag it to the end of that column.

### **Excel function**
- Either,
    - we can manually write function by on a selected cell starting with = then writing function's name and inside that all the value of a column where you wanna apply function.
    - or by clicking the function name on the formula tab directly.

- *Functions for counting*
    1. count()
    2. counta()
    3. countblank()
    4. len()
    5. valuecount()
    6. unique()
    7. nunique()
    8. mode()

- *Functions for continous variable*
    1. sum()
    2. average()
    3. median()
    4. min()
    5. max()
    6. var()
    7. varp()
    8. stdev()
    9. stdevp()
    10. percentile()
    11. sqrt()
    12. power()
    13. exp()
    14. log()
    15. log10()

- *Functions for categotical variable*
    1. upper()
    2. lower()
    3. proper()
    4. left()
    5. right()
    6. mid()
    7. substitute()
    8. concat()
    9. trim()
    10. len()
    11. split()

- *Functions for time-series variable*
    1. today()
    2. day()
    3. date()
    4. month()
    5. year()
    6. weekday()
    7. days()
    8. now()

- *Functions for condition extraction*
    1. countif()
    2. sumif()
    3. averageif()
    4. if()

### **Data Tansformation**
1. **vlookup()**
    - It is used to add/join one column from one table to another table with reference to one common column between them.
    - syntax, **vlookup(lookup_value, table_array, col_index_no., match_mode)**

        - lookup_value = value that we want to look in another table.
        - table_array = whole table where you want to look that value.
        - col_index_no. = if lookup value matches which numbered column you want join.
        - match_mode = either 'True' or 'False'
            - True means approx match of lookup value 
            - False means exact match of lookup value.
            - E.g - if lookup value is S001, then True means S01 and False means S001
    - we have to lock the 'table_array' using F4 key because when we drag the resulted vlookup cell from remaining cell then according to the vlookup function arguments, lookup value needs to be increase not the whole col where lookup value supposed to be looked.
    - there is one limitation with vlookup(),
        - it will only work when whatever value we are looking of one table should be present in first column of another table.

2. **xlookup()**
- To overcome the limitation of vlookup(), we use xlookup()
- syntax, **xlookup(lookup_value, lookup_range, result_range, missing_value, match_mode)**
    - lookup_value = value that we want to look in another table.
    - lookup_range = lookup_value's value's column
    - result_range = if lookup value matches which column you want join.
    - missing_value = if there are gonna have any missing value what you wanna see instead of blank.
    - match mode = same as vlookup()
- we have to lock 'lookup_range' and 'result_range'

### **Data Visulisation**
- For creating plots we always require 'pivot table' first, because they do summarization for column that are required for plots.
- Then from 'insert tab' we choose plots for that specific pivort table and apply formating on plot.


