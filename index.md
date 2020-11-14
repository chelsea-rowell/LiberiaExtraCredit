# Predicting education levels in Liberia based on age, gender, wealth, size, and location

## Overview of data

This data set describes the education, location, size, wealth, gender, and age of a sample of 48,219 people living in Liberia.  By analyzing this data set, we can try to predict the relationships between each of our variables.  In my analysis, I focused on the correlation between location, size, wealth, gender, and age and the education of each person.  

### Pairwise Correlation
To get a brief overview of possible correlations between each of my variables, I made a pairplot, which maps the relationships between each variable represented in the data set.  

<img src="https://user-images.githubusercontent.com/58756714/99138899-31123900-2602-11eb-8757-29e5e298296e.png" width="650">

This pairpot doesn't lead to any immediate conclusions regarding the importance of each covariate, so I made a heatmap as well.  

<img src="https://user-images.githubusercontent.com/58756714/99138950-a120bf00-2602-11eb-9147-88134be538e7.png" width="650">

The heatmap shows weak correlations between wealth and education, and between gender and education.  This result makes sense.  Wealthy people have more time and resources to pursue education, and gender inequality is a significant issue in Liberia.  

### Histograms

Lets take a closer look at our education and wealth data. 

![edu_hist](https://user-images.githubusercontent.com/58756714/99139915-08db0800-260b-11eb-843b-69e2a4a18cd0.png)
![wealth_hist](https://user-images.githubusercontent.com/58756714/99139917-0b3d6200-260b-11eb-9175-0ae64b93b697.png)

Although there are a fair number of data points at all levels of wealth and education, the data is skewed right for both variables.  This means that there are more people in Liberia with lower levels of education and lower levels of wealth than there are with higher levels of education and higher levels of wealth.  Again, this conclusion makes sense, as Liberia is a developing nation.  

### Two types of probability density plots: Kernel density estimation (KDE) and stacked histogram
Kernel density plots smooth the data with a Gaussian kernel in order to produce a single continuous density estimate, and easily allowing the user to see where data is most concentrated. 
The stacked histogram emphasizes the part-whole relationships of the variables, which are vital to consider when analyzing data from a sociological perspective.

These plots provides an interesting view of the relationship between gender and education in Liberia.  
![edu_gender_density_plot](https://user-images.githubusercontent.com/58756714/99140329-f4990a00-260e-11eb-827d-b5c3f019ad22.png)
![edu_gender_prob](https://user-images.githubusercontent.com/58756714/99140567-f6fc6380-2610-11eb-893f-2a77d1a30865.png)

Making the assumption that within the data, gender 1 represents men and gender 2 represents women, we can see that men are more likely to be present in higher levels of education. Additionally, these plots make it clear that Liberia is pretty uneducated overall, as the number of highly educated persons is so small that it is barely visible on the graph.  

![edwealthkde](https://user-images.githubusercontent.com/58756714/99140737-7474a380-2612-11eb-8e38-62cb1ec688a1.png)
![education_wealth_prob](https://user-images.githubusercontent.com/58756714/99140568-f794fa00-2610-11eb-9f05-06b45b46067c.png)

Examining the KDE plot, we again see that the data is skewed right, as it is concentrated at lower levels of education.  It's critical to note that at low levels of wealth, a lack of education is the norm, even though more educated people are not necessarily more wealthy.  We can also see that achieving wealth does not necessesitate high levels of education, as extremely wealthy people are about evenly spread across all education levels.

We can see in the stacked histogram that there is a very small number of highly educated, wealthy persons living in Liberia, and that extremely well educated people are also genereally wealthy. This suggests that high levels of education are only readily available for those who are already richer than their compatriots, which almost certainly has a negative impact on Liberian class mobility.  
