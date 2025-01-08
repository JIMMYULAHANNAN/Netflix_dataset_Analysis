# Netflix_dataset_Analysis

This project involves exploratory data analysis (EDA) on a Netflix dataset using Python and libraries like pandas, seaborn, and matplotlib to extract insights such as identifying duplicates, handling missing values, filtering records, and visualizing trends. Tasks include analyzing movie and TV show releases, director contributions, ratings, and other key attributes. Here's a detailed breakdown:

1. **Dataset Overview**:  
   - The dataset is loaded and its structure is examined (`data.head()`, `data.tail()`, `data.shape`, etc.).  
   - Information about columns, data types, and memory usage is provided using `data.info()`.

2. **Duplicate Records**:  
   - Duplicate records are identified using `data.duplicated()` and removed permanently with `data.drop_duplicates(inplace=True)`.

3. **Handling Null Values**:  
   - Null values are detected using `data.isnull()` and visualized with a heatmap using `sns.heatmap(data.isnull())`.

4. **Task-Based Analysis**:
   - **Q1**: Identify the `Show ID` and director of "House of Cards" using filtering (`data[data['Title'].str.contains('House of Cards')]`).  
   - **Q2**: Determine the year with the highest number of releases using `data['Date_N'].dt.year.value_counts()` and visualize it with a bar chart.  
   - **Q3**: Count the number of Movies and TV Shows using `data.groupby('Category').Category.count()` and a seaborn count plot.  
   - **Q4**: Filter movies released in 2000 using conditional filtering.  
   - **Q5**: Display TV Shows released in India using a similar filter.  

5. **Advanced Analysis**:  
   - **Top Directors**: Identify the top 10 directors by output using `data['Director'].value_counts().head(10)`.  
   - **Conditional Queries**: Filter movies of type "Comedies" or content from the UK.  
   - **Actor Analysis**: Count how many movies/TV shows feature Tom Cruise by dropping nulls and using `str.contains()`.  
   - **Unique Ratings**: List all unique ratings with `data['Rating'].unique()`.  
   - **Specific Ratings**: Count movies with TV-14 ratings in Canada using multiple conditions.  
   - **Post-2018 Ratings**: Count TV Shows with R ratings after 2018.  

6. **Duration and Sorting**:
   - **Maximum Duration**: Split the `Duration` column into minutes and units using `str.split()` and find the maximum value.  
   - **Country with Most TV Shows**: Identify the country with the highest number of TV Shows using `value_counts()`.  
   - **Sort by Year**: Sort the dataset by year in ascending or descending order.

7. **Complex Filtering**:
   - Find instances where the category is "Movie" and type is "Drama" or the category is "TV Show" and type is "Kids."

### Conclusion:
This analysis leverages pandas for data manipulation and seaborn for visualization, offering insights such as content trends, top contributors, and rating distributions on Netflix. 

Code:
