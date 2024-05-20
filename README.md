# Movie Correlation Project in Python

This project focuses on finding the highest correlations in movie industry based on the dataset "Movie Industry" retrieved from (https://www.kaggle.com/datasets/danielgrijalvas/movies). These correlations describe relationships between variables such as movie *budget*, *gross earnings*, *rating*, *score*, and *company*.

## Libraries

The Python libraries used are:
-	**_Pandas_**
-	**_Seaborn_**
-	**_Numpy_**
-	**_Matplotlib_**

## Steps: 
1) **Importing Packages and Libraries.**

2) **Loading and cleaning the data:**

- Handling missing data
- Changing data types for the following columns: *budget* (float to integer), *gross* (float to integer), *votes* (float to integer), *score* (float to integer)
- Dropping duplicates

3) **Box Plot with *gross revenue*:**

Creating the Box Plot shows that there are outliers in the industry when it comes to gross earnings. That means *gross revenue* can be highly correlated to other categories.

5) **Scatter Plot with *budget* vs *gross*:**

Next step is to find out what variables are the most correlated to the *gross revenue*. Scatter Plot created in **_Matplotlib_** and **_Seaborn_** illustrates high correlation between *budget* for a film and its *gross earnings*. 

7) **Regplot (*Seaborn*):**

Creating Regplot and drawing a linear regression model shows positive correlation between *budget* and *gross earnings* more distinctively. However, it is still hard to see how strong this correlation is. Therefore, the next step is to look at actual correlation numbers.

9) **Correlation Coefficients:**

Correlation Methods used in this project:
-	**_Pearson_** (default)
-	**_Kendall_**
-	**_Spearman_**

7) **Correlation Matrix (*Seaborn*):**

Correlation Matrix allows to visually demonstrate correlation coefficients between given variables and evaluate relationship between them. Lighter colors show very high correlation (*budget* vs *gross*) while darker colors indicate lower correlation (*budget* vs *score*).

This type of correlation only works on numerical data (“numerical features”). In order to determine correlation between categorical variables like *company*, *director* or *genre*, and create a numeric representation of them in Correlation Matrix I converted these variables into category type using **_for_** loop and **_cat.codes_** function. The new Matrix includes categorical values and shows that *genre* and *rating* have weak correlation to *gross revenue* while *votes* and *gross* are highly correlated as well as *budget* and *gross*.

9) **Filtering data:**

Filtering data using **_unstack_** function allows to find the highest correlation quickly. Another way to easily arrange the data in a meaningful order is using **_sort_values_** function. I included parameter > 0.5 in order to determine pairs with the strongest positive correlation.

## Conclusion:
*Votes* and *budget* have the highest correlation to *gross earnings*. *Genre*, *rating* and *company* have low correlation to *gross earnings*.


 




