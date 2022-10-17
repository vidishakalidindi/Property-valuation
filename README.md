# Property-valuation

Case Overview:

CCAO had a history of incorrectly valuing property (and thus collecting the wrong amount of taxes) so severely that the public demanded transparency and reform that eventually came in the form of a newly elected assessor. As Fritz Kaegi took office, he made allCCAO’s methodology and data public. Our objective is to use the public data to predict the value of a home as close to its actual value as possible. To do this, we are utilizing the “historic_property_data.csv” to train models that predict the value of homes listed in “predict_property_data.csv”with a low MSE.  

Methodology:

As historic_property_data.csv contained 50,000 entries with 63 variables. The first step was to trim the data. To do this, we used linear regression to determine which variables were statistically significant and only use the statistically significant variables in our models. It is important to note that most variables are categories, characters, or logical values, instead of numerical and therefore factor ()was applied to those variables, so the models  did  not  interpret  those  numbers  as  if  they  had  numerical relationships.Weplanned  on  training  four different types of models: Linear, lasso, random forest, and boosting. The idea was to use the model with the lowest MSE to predict home value in “predict_property_data.csv”. Random Forest ended up being the model with the lowest MSE, which is most likely because random forests  can  find  non-linear  relationships  along  with  beinglow  bias  and  only  moderate  in  variance.Post performing the Linear Regression Model, we have chosen the attributesthat turned out to be significant for the linear model in Random Forest.The result is an MSE of Random Forest 2,409,052,969. which is much lower than that of boosting’svalue12,786,505,366.

Methodologyis as follows:
1.Handling the missing valuesa.Out of the 63 variables in the “data” dataset, the following variables have more than 50 % missingvalues that are not filled “meta_cdu","char_apts","char_tp_dsgn", char_attic_fnsh”, “char_renovation", “char_porch"We also remove variablesnot relevant by referring to the content from codebook..char_site, char_cnst_qlty, char_repair_cndb.

2. Replacing the missing values with Mean:Tohandle the missing values for the numeric columns, wehave decided to replace them with their respective Mean.

3. Plotting the correlation of Numeric Values:
It is observed thatthere are very few variables, that are greater than 90% correlated with each other

4. Skewnesscheck of categorical variables:
To analyzethe data further, we consideredchecking the skewness for all the categorical variables

Modeling: 

We have used the following methods to estimate the sale price.
We convert all categoricalvariablesto factor data typea.

Linear Regression:

We are  using  Linear  regression as  it allows  you to   understand   the   strength   of   relationships between  variables.  this  will  help  us  further  for building other models. p value < 0.05. We opted thefromthe  output  we  choose  statisticallysignificantvariablesthat  havep  value  < 0.05.We reduced theattributesto 37 variables.

Lasso Regression: 
Since  we  have  the  variables  withhigh  levels  of multicollinearity,  this  helps  when  we  want  to automate  certain  parts  of  model  selection,  like variable selection/parameter elimination.

Boosting:
 We  grow  the  trees  sequentially,  using  the information  from  the  previous  tree,  using modified versions of the same dataset.
 
 Random Forest:
 Using  this  method,  we builddecision  trees  based on  bagging,  and  force  the  trees  to  be  different. 
 
 
