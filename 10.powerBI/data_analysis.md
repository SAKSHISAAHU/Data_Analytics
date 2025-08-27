# **Data Analysis in PowerBI**

## **1.extract data**
- can load data using "get data" option in power BI desktop from there to what ever sourse you wanna load data, you can choose and load.

## **2.Data understanding**
-  understanding each and every column is done in Table view.

## **3.data modeling**
- in power BI database schema is called data modeling, which can be seen by model view.

- when we load data which is stored in multiple tables from, 
    - databse then there will be connection between tables automatically most of the time in power BI's model view.
    - excel we may or may not get the connection

- if the tables are not connected but they have relation between them, then we can manually connect them by choosing the specific column from one table that need to connect to their desired table and select 'manage relationship' on the top bar.
    - then click on 'new relationship', then fill all the details to which table's column to which should connect and choose cardinality also.


## **4.Data exploration**
- **1. For unique value & value count & missing value :-**
    - we do data exploration in power BI's power query window's view section, where we have to check the box of **column quantity, distribution and profile**.

        - Column distribution : 
            - tells how many unique value are there.

        - Column profile :
            - it is equal to **df[ ].describe** in python.
            - it will tell total count, total error value, total empty value, total distinct, total unique, empty string, min and max values.
            - for categorical column, by clicking the arrow after the column_name can also show the total no. of unique value.

        - Column quantity :
            - it tell the percent of valid value (other than error value), error and empty value (or missing value)
            - values like '1' comes under error value.

- **2. For wrong data :-**
- **3. For wrong datatype :-**
_ **4. For duplicate record :-**
- **5. For outliers :-**


## **5.Data transformation**
- Combining different tables,
    - combining comes under transform_data's power query editor window.
    - there is seperate area for combining, merge/join and concat/append which lie under combine section of the bar.

    1. **merge table**
        - for merging column there is an option under combine section on the bar under the home tab called merge quries.
        - if we click on 'merge quries' then it will do merging on the same table.
        - if we click on 'new merge quries' it will create new table for merging.
        - the merging will be same as we do in python merge()

        - **left merge :**
            - click on 'merge query as new'
            - select the table where you wanna merge to.
            - select the table where you wanna merge from.
            - on join kind option select left
            - a comple new column was creted.
            - same we can do in python, **pd.merge(df1,df2, on='', how='left')**

        - **right merge :**
            - same all the step but instead choosing left choose right.

        - **inner merge :**
            - same all the step choose inner when selecting join

        - **outer merge :**
            - same all the step choose outer when selecting join

    2. **append tables**
        - it basically mean concat.
        - it also have two option 'append quries' and 'append quries as new' which create a seperate table 
        - it will combine or do union tables, when they have same column_name and same number of columns.
        - same we do python as, **pd.concat([list_of_dataframe])**
        
    - **which ever table have relation in database schema that only will able to get combine to do data analysis.**

## **6.Data cleaning**

