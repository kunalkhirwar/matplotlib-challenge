**Instructions**

This project is broken down into the following tasks:
- Prepare the data.
- Generate summary statistics.
- Create bar charts and pie charts.
- Calculate quartiles, find outliers, and create a box plot.
- Create a line plot and a scatter plot.
- Calculate correlation and regression.

**Prepare the Data**

1. Ran the provided package dependency and data imports, and then merged the '*mouse_metadata*' and '*study_results*' DataFrames into a single DataFrame.
2. Displayed the number of unique mice IDs in the data, and then checked for any mouse ID with duplicate time points. Displayed the data associated with that mouse ID, and then created a new DataFrame where this data is removed. Used this cleaned DataFrame for the remaining steps.
3. Displayed the updated number of unique mice IDs.


**Generate Summary Statistics**

Created a DataFrame of summary statistics.

My summary statistics includes:
  - A row for each drug regimen. These regimen names are contained in the index column.
  - A column for each of the following statistics: mean, median, variance, standard deviation, and SEM of the tumor volume.


**Create Bar Charts and Pie Charts**

1. Generated two bar charts. Both charts are identical and show the total total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study.

    - Created the first bar chart with the Pandas '*DataFrame.plot()*' method.
    - Created the second bar chart with Matplotlib's '*pyplot*' methods.

2. Generated two pie charts. Both charts are identical and show the distribution of female versus male mice in the study.

    - Created the first pie chart with the Pandas '*DataFrame.plot()*' method.
    - Created the second pie chart with Matplotlib's '*pyplot*' methods.


**Calculate Quartiles, Find Outliers, and Create a Box Plot**

1. Calculated the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculated the quartiles and IQR, and determined if there were any potential outliers across all four treatment regimens. Used the following substeps:
     - Created a grouped DataFrame that shows the last (greatest) time point for each mouse. Merged this grouped DataFrame with the original cleaned DataFrame.
     - Created a list that holds the treatment names as well as a second, empty list to hold the tumor volume data.
     - Looped through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Appended the resulting final tumor volumes for each drug to the empty list.
     - Determined outliers by using the upper and lower bounds, and then printed the results.

2. Using Matplotlib, generated a box plot that shows the distribution of the final tumor volume for all the mice in each treatment group. Highlighted any potential outliers in the plot by changing their color and style.


**Create a Line Plot and a Scatter Plot**

1. Selected a single mouse that was treated with Capomulin, and generated a line plot of tumor volume versus time point for that mouse.
2. Generated a scatter plot of mouse weight versus average observed tumor volume for the entire Capomulin treatment regimen.


**Calculate Correlation and Regression**

1. Calculated the correlation coefficient and linear regression model between mouse weight and average observed tumor volume for the entire Capomulin treatment regimen.
2. Plotted the linear regression model on top of the previous scatter plot.
