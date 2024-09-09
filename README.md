<h1>Problem Statement</h1>

In this problem we are given a dataset from a logistics company where their customers have answered 6 questions in a survey and also given an overall response if they were happy/unhappy.
<br>
The ask is to predict what makes a customer happy or unhappy based on the their responses to the survey (achieving an accuracy of 73%) and also determine if any survey questions can be removed. 
<br>

<h1>Methodology</h1>
After performing exploratory data analysis several machine learning models were trained and their performance evaluated to understand what each model gets right and wrong and why.
<br>
Then feature selection was done using XGBoost feature_importances and RFE (recursive feature elimination). Sets of candidate features were curated and all models were evaluated against all sets of candidate features to determine which model strikes the best trade-off. 
<br>
The best classifier was found to be LgbmClassifier and it was able to achieve the goal of 73% accuracy while also scoring high on other evaluation metrics.

<h1>Findings/Conclusion</h1>
The overall finding has two parts. 
<br>
<br>
First that there are three aspects of company's operations that determine customer happiness/unhappiness. They are 
<ol>
  <li>X1=My order was delivered on time</li>
  <li>X5=I was satisfied with my courier</li>
  <li>X6=The app makes ordering easy</li>
</ol>
It's not about getting one of them right but instead if the company wants happy customers they need to get all 3 of them right i.e. get high responses on all 3. 
<br>
<br>
Secondly, the current problem in their operations explaining why 50% of customers are unhappy is (mostly) X5= I was satisified with my courier. 
<br>
This is what needs to be fixed in addition to improving X1 and X6 to avoid any 3/5 responses on those 2 questions. 
