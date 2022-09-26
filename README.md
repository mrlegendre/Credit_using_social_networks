# Project_2_Credit_using_social_networks
This project examines the effects of adding social network attributes on credit scoring

### Group members: Maurice Le Gendre, Abhilesh Gaikwad, James Anderson

This project examines the effects of adding social network attributes on credit scoring. Many
lenders have realised the potential of borrowers with thin financial files who lack sufficient credit
history. To overcome this problem, there has been a trend in examining
the behaviour of borrowers. In many cases, such behaviour is influenced by peers within a social
circles of borrowers. 

We intend to investigate to see if we can find meaningful information on social data of
those who are unbanked or underbanked, and to measure how such data would affect their credit scores.

Excluding and blocking potentially-profitable individuals and small-to-medium
enterprises from accessing banking-type services such as credit would make economies suffer a
huge opportunity cost. Excluded individuals are not, necessarily, limited to low-income earners as
they can be new entrants to the job market such as fresh graduates, immigrants with high skills
and calibre, and many others left out due to a thin or a non-existing financial profile or history

The big data revolution has been a game changer in credit risk scoring and assessment models.  

With the introduction of machine learning and artificial intelligence as advanced models 
many researchers argued their superior suitability, and that machine learning and deep learning
algorithms can make better and faster underwriting decisions in credit

In this project we will use machine learning and neural networks to determine if 
an applicant will be approved for a small loan/credit card based on social network data. 
*[ref2]

## Research Questions

1) Does analysing borrowers’ social networks determine their credit scores more accurately? 
2) Can lenders infer whether a borrower is likely to repay or default based on the type and the size of one’s social network? And, finally, 
3) how can social network data be incorporated within the traditional credit risk assessment?

----------------------------------------------
## 
Originally our project was focused on using API's for Twitter and LinkedIN, and to initially do a sentiment analysis, and data extraction.  Due to limited time and resources we modelled our project off of study [ref1] and decided to use their 'weighting mechanism' for the social variables that we added to our own dataset off of Kaggle.
##
Our target variable (Y) being whether a loan is approved or not ends up being a function of the applicants age, income, education, and social variables only.  Again due to limited time and resources this data had to be slightly bias in order to run any of the machine learning models, and neural network models.

--------------------------------------------



## Hypothesis Development

Hypothesis 1 (H1). Social network quality contains predictability of loan default.
When the borrower applies for a loan, the platform will ask the borrower for permission to access the address book. After
the platform reads the address book, the platform will obtain the borrower’s real social network
information. The platform compares social network information with the platform’s database and
can get the total number of borrowing defaults within the borrower’s social network




Hypothesis 2 (H2). Social network stability contains predictability of loan default.

The longer the mobile phone
number is used, the more people the borrower can contact and the closer relationship there will be in
the network. Once he/she leaves the social network, it takes a lot of effort to rebuild. The replacement of
the mobile number means that the reconstruction of the social network will cause great inconvenience
to the borrower, which is also a shock to the borrower’s default. If the borrower’s mobile phone
number is only used for a short period of time, the borrower’s social conversion cost will be lower, and
the default will have less impact on the borrower’s life.



Hypothesis 3 (H3). Social network exposure contains predictability of loan default

When borrowers apply for loans, they can choose to disclose many kinds of contact information
to the platform. In addition to their mobile phone number, they can also provide home phone number,
work phone number, and emergency phone number. The more contact information the borrower
provides, the more social information the platform can control. In the event of default, 
the platform will have more channels to contact collection, and the information that the borrower cannot pay the
loan on time will be communicated to his social network. *[ref1]

## Definitions of 3 'Social Variables' above

SOCIAL NETWORK QUALITY -counts the number of default borrowers in a borrower’s mobile address book.

When the borrower applies for a loan, the platform will ask the borrower for permission to access the address book. After
the platform reads the address book, the platform will obtain the borrower’s real social network
information. The platform compares social network information with the platform’s database and
can get the total number of borrowing defaults within the borrower’s social network. 

SCORES -> {0 (0.87), 1 (0.10), 2 or above (0.03)}

SOCIAL NETWORK STABILITY - he social network stability means the length of time the borrower’s mobile phone
number has been used. 

The telecom operator knows the customer’s mobile phone number usage
duration, and the platform can obtain the social network stability information of the borrower through
cooperation with the telecom operator. Due to the large volume of social network information, we
used MapReduce to carry out the extraction process.

SCORES -> {1 year or below (0.32), 1–3 years (0.31), >3 years (0.37)}

SOCIAL NETWORK EXPOSURE -> comes from the number of contacts that the borrower fills in on theapp or website when applying for a loan, 
including home phone, work phone, and emergency contact phone number.

The borrower must fill in his or her own phone number when registering on the
platform. In addition, the borrower can also fill in his home phone number, work phone number,
and emergency contact phone number, so that the platform receives the social network exposure
information.

SCORES - > {1 (0.12), 2 (0.56), 3 (0.21), 4 (0.11)}

*[ref1]


-------------------------------------
## RESULTS

## CONFUSION MATRICES

### Random Forest
![](/Images/cm_rf.png)
### Linear Regression
![](/Images/cm_lr.png)
### Support Vector Machine (SVM)
![](/Images/cm_svm.png)

## Features Importance - Random Forest
![](/Images/rf_features_importance_list.png)

## CLASSIFCATION REPORTS

### Random Forest
![](/Images/report_rf.png)
### Linear Regression
![](/Images/report_lr.png)
### Support Vector Machine (SVM)
![](/Images/report_svm.png)


## Gradient Boost Classifier results
![](/Images/grad_cm_acc_report.png)

## Gradient Boost Classifier Tree
![](/Images/grad_boost_tree.png)


## Precision-Recall graph - Logistic Regression vs. Random Forest
![](/Images/pr_lr_rf.png)

## Precision-Recall graph - Gradient Boost vs. SVM
![](/Images/pr_svm_grad.png)



---------------------------------------
Our initial results were not quite the same as what was presented here.  This is due to the data not being 'clean'.  I was able to clean up the data, use the bigger data set which we originally intended on using, and was able to get slightly better results.  Hence, these notebooks' results will differ from the power point presentation.

---------------

## CONCLUSIONS
Modern society is highly interconnected, and social network data can show the credit status of borrowers. Mobile phones are accessible to almost
everyone and hold a lot of social network information.
By extracting that social network data we were able to predict borrowers behaviour in a limited sense.
This is due to our limited data set, and some of the data being somewhat bias, and limited practice in the data science field.
Our machine learning models and neural network model although simple, did prove that once this type of data is captured behaviour can be predicted with a fair degree of accuracy.
Given more time, better data, and more stringent practice with this type of data we feel confident we could have made more realistic models, and even better predictions. 










*References*

*[ref1]
https://www.mdpi.com/2078-2489/10/12/397/htm

Credit Scoring Using Machine Learning by Combing
Social Network Information: Evidence from
Peer-to-Peer Lending
Beibei Niu, Jinzheng Ren * and Xiaotao Li


*[ref2]https://researchportal.port.ac.uk/en/studentTheses/developing-a-credit-scoring-model-using-social-network-analysis

Developing a Credit Scoring Model Using 
Social Network Analysis
Ahmad Abd Rabuh


