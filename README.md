# Uber-Rides-Data-Analysis

_**We will use Python and its different libraries to analyze the Uber Rides Data.**_

Dataset Link: https://media.geeksforgeeks.org/wp-content/uploads/20240919115958/UberDataset.csv

**1. Importing Libraries**

The analysis will be done using the following libraries : 

(i) _**Pandas:**_  This library helps to load the data frame in a 2D array format and has multiple functions to perform analysis tasks in one go.

(ii) _**Numpy:**_ Numpy arrays are very fast and can perform large computations in a very short time.

(iii) _**Matplotlib / Seaborn:**_ This library is used to draw visualizations.

**2. Importing Dataset**

After importing all the libraries,  download the data using the link. Once downloaded, you can import the dataset using the pandas library.

(i) To find the shape of the dataset, we can use dataset.shape

(ii) To understand the data more deeply, we need to know about the null values count, datatype, etc. So for that we will use dataset.info().

**3. Data Preprocessing**

(i) As we understood that there are a lot of null values in PURPOSE column, so for that we will me filling the null values with a NOT keyword. You can try something else too.

(ii) Changing the START_DATE and END_DATE to the date_time format so that further it can be use to do analysis.

(iii) Splitting the START_DATE to date and time column and then converting the time into four different categories i.e. Morning, Afternoon, Evening, Night.

(iv) Once we are done with creating new columns, we can now drop rows with null values.

(v) It is also important to drop the duplicates rows from the dataset.

**4. Data Visualization**

In this section, we will try to understand and compare all columns.

(i) Let's start with checking the unique values in dataset of the columns with object datatype.

(ii) we will be using matplotlib and seaborn library for countplot the CATEGORY and PURPOSE columns.

(iii) Let's do the same for time column, here we will be using the time column .

(iv) Now, we will be comparing the two different categories along with the PURPOSE of the user.

_**Insights from the above count-plots:**_

_-> Most of the rides are booked for business purpose._

_-> Most of the people book cabs for Meetings and Meal / Entertain purpose._

_-> Most of the cabs are booked in the time duration of 10am-5pm (Afternoon)._

(v) As we have seen that CATEGORY and PURPOSE columns are two very important columns. So now we will be using OneHotEncoder to categories them.

(vi) We can now find the correlation between the columns using heatmap.

_**Insights from the heatmap:**_

_-> Business and Personal Category are highly negatively correlated, this have already proven earlier. So this plot, justifies the above conclusions._

_-> There is not much correlation between the features._

(vii) We need to visualize the month data. This can we same as done before (for hours). 

_**Insights from the above plot:**_

_-> The counts are very irregular._

_-> Still its very clear that the counts are very less during Nov, Dec, Jan, which justifies the fact that  time winters are there in Florida, US._

(viii) Visualization for days data.

(ix) Now, let's explore the MILES Column .We can use boxplot to check the distribution of the column.

(x) we can use distplot for values less than 40.

_**Insights from the above plots:**_

_-> Most of the cabs booked for the distance of 4-5 miles._

_-> Majorly people chooses cabs for the distance of 0-20 miles._

_->For distance more than 20 miles cab counts is nearly negligible._
