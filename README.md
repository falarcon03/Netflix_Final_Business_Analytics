# Netflix_Final_Business_Analytics
Final Project Business Analytics
Analyzing Netflix's Data to Differentiate Movies from TV Shows

The primary objective of my research was to determine if the available Netflix data could help predict whether a given title was a movie or a TV show.

Data Preparation and Cleaning

My first step involved preparing the dataset for analysis. I encountered entries listing multiple countries per title, which complicated an accurate count of titles per country. To resolve this, I expanded these entries so that each country associated with a title became a separate data point, consequently increasing the dataset's size. An interesting observation arose during this process: despite titles being repeated across different countries, they often simultaneously exist in various regions, which can be expected considering content distribution practices.

Next, I transformed categorical data into a numerical format the model could interpret, using encoding techniques for countries, weekdays, and ratings. The target variable, the type of program (movie or TV show), was also encoded. In retrospect, the random assignment of numerical values to countries may not have been the most strategic choice for the model's predictors, and a more thoughtful sorting could potentially have yielded different insights.

Model Evaluation and Limitations

Surprisingly, the model displayed high accuracy levels, which initially brought its validity into question. However, the confusion matrix revealed that a significant data imbalance existed between the number of movies and TV shows in the dataset, which led the model to predominantly classify titles as movies. This was reflected in the high accuracy score. The application of alternative models such as Decision Trees and K Nearest Neighbors (KNN) confirmed this bias, with these models also showing low precision and recall for TV shows, culminating in a near-zero F1 score. The Decision Tree model slightly outperformed others, achieving a modest F1 score of 0.111, which, despite being low, was not zero.

Insights from Logistic Regression Coefficients

Further analysis of the Logistic Regression coefficients revealed a preference for titles added later in the week, particularly from Friday to Sunday, which aligns with the distribution shown in the histogram where Friday emerged as the most popular day for Netflix to update its catalog.

Conclusion

In conclusion, while the model struggles to accurately distinguish TV shows due to the disparity in the number of titles, the data cleaning process was crucial. It enabled the identification of content preferences across different countries and pinpointed the weekdays when titles are more likely to be added. This analysis underscores the importance of a balanced dataset and thoughtful feature selection in predictive modeling.
