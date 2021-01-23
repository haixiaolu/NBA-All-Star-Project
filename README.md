# [NBA-All-Star-Project](https://haixiaolu.github.io/NBA-All-Star-Project/)
predict 2021 NBA all-star game 24 men roster

** Check the HTML Notebook [here](https://haixiaolu.github.io/NBA-All-Star-Project/)
---

  ## Background

  The National Basketball Association All-Star Game is a basketball exhibition game hosted every February by the National Basketball Association (NBA) and showcases 24 of the league's star players. It is the featured event of NBA All-Star Weekend, a three-day event which goes from Friday to Sunday.  

  This project is based on personal interest to predict **the top 12 players from both East and West Conference.** It is compared with previously selected NBA All-Star players in the previous seasons. The goal of this project is to understdand the impact feature selection had on the overall accuracy of the analysis when comparing different models. This model also will predict which team will win between the West and East Conference Team.


  ## Data

  The training dataset used for this project contains 5 seasons data which was from 2015 to 2019. **182812 observations and 90 variables** are collected from this dataset. 


  ### Dealing with data

  - For the purpose of creating a higher performance model, the data was split by each season. To reduce the 90 features, a wrapper feature selection algorithm knows as Borut was used in each dataset to extract the important features. 
  - Some of the new features also added to each dataset, such as sum, average and rank all player;s performance in that particular season. Then the entire data set is categorized by each individual player's name. 
  - In addition, the players are also divided into West and East since I am ultimately choosing plaers from East and West conference separately. 
  - The final training dataset has 202 features for each season dataset. Therefore, there are 10 dataframes (5 seasons, 2 conference teams each) to train the models as training data. 
  - The rest of 2 dataframes which is the data from the 2020-2021 season are used to predict the final results. 


  ##  Modeling Approach

  - Since it is a classification problem, it is broken down to two main modeling approaches, logistic modeling and classification trees. 

  ###  Four different logistic models were created based on the 52 predictors. 

  - First model used the whole dataset to build a basic model.
  - The second model from the tree's variable importance was used. 
  - Third one I used all the important features from Boruta algorithm feature selection. 
  - The last one was created a penalized logistic regression model using important features that were selected from the Boruta algorithm. The model then     went through stepwise optimization for both the Akaike Information Criterion (AIC) and Bayesian Information Criterion (BIC) criterion.   

  ### Two classification tree were created based on the 52 predictors

  - Decision Tree
  - Random Forest 

  ### Approach
  In order to determine the effectiveness of the predictive model created, the model was used to predict the East conference dataset in the 2015 season by using the West conference data model.  Ideally, all the players who were selected previously in the season 2015 should be showing in our predictions.  Several measure metrics were used to evaluate the model performance, such as accuracy, kappa, sensitivity and specificity, etc.. 




  ## Results

  ### West 12 People Roster
  <img src = "https://github.com/haixiaolu/NBA-all-star/blob/main/images/screenshot.png" width = "800" height = "500">
  
  
  ### East 12 People Roster
  
  <img src = "https://github.com/haixiaolu/NBA-all-star/blob/main/images/nba1.png" width = "800" height = "500" >
  
  
  ### Which team will won?
  <img src = "https://github.com/haixiaolu/NBA-all-star/blob/main/images/nba.png" width = "800" height = "500"> 


## Future work
Compare with the real results in Febuary of 2021. 

