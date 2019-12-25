# Restaurant-Rating-Predictions
Using data from Zomato to predict the rating (or subjective *tastiness*) of the food in a restaurant based on its cost and popularity.

ACKNOWLEDGEMENTS

The original source of the data can be found here: https://www.kaggle.com/shrutimehta/zomato-restaurants-data
Much of the tools and techniques I used for this project can be found here: https://www.kaggle.com/rochellesilva/simple-tutorial-for-beginners

MOTIVATION & GOALS

As a foodie, I wanted greater insight into how the price and popularity of a restaurant is correlated with its rating, even if the restaurant is lesser-known. This way I could quickly predict by looking at the prices on menu or heuristically by how many friends recommend the restaurant to me. Futhermore, these insights may help Zomato reccommend restaurants that don't get as much love to users, without sacrificing the user-experience.

Furthermore, I wanted to dip my toes into data science and supervised learning. I took this curiosity about food as an opportunity to use jupyter notebooks locally and play with pandas, numpy, seaborn and sci-kit learn. It has definitely left me eager to learn more.

STEP-BY-STEP DESCRIPTION

Due to the nature of Jupyter notebooks, it was quite easy to organize my code and leave ample comments to guide another person through my work. In summary, I first did a multivariate analysis of how cost and popularity correlate to ratings. Unsurprisingly, people like cheap food, and were more likely to leave a rating when they found the food very good to excellent. I made a really beautiful scatterplot using seaborn that I am very proud of.

After data exploration I leveraged similar case imputation to replace missing values. Essentially, food that wasn't rated was given a rating that was the *average* rating of food at similar price points. I also encoded the ratings as discrete numerical values, using sklearn's cool preprocessing methods. It was really cool to see that achieved in one line.

Lastly, I used sklearn's handy cross-validation tools to see which model would be best for my goals. Random Forest was a clear winner, with 100% accuracy which makes me feel I did something wrong (please let me know if you catch what). Naive Bayes was a close second achieving an accuracy of 92%. I would love pointers on whether this suggests overfitting.

FUTURE?

In the future, it would be fun to create a restaurant recommendation engine like how netflix recommends movies based on your past binges. As a foodie, I often feel overwhelmed by choice. When visiting a new city, I want to eat the best food possible ASAP without sacrificing money to a restaurant I won't like. Therefore, this is a tool I would find very handy. Furthermore, I would love to see how cuisine influences the rating to know, once and for all, which culture/country makes the tastiest food and settle the debate.
