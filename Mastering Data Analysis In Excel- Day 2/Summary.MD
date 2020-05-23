## ** Binary Classification And Confusion Matrices ** ##

- A confusion matrix is a table that is often used to describe the performance of a classification model
- The confusion matrix itself is relatively simple to understand, but the related terminology can be confusing.
      
                   n=150   | Predicted : NO (or) c |  | Predicted : YES (or) d | 
                 
 | Actual : NO (or) a |         | 30 (or) e |                    | 17 (or) f |                                 e+f+g+h=1 ; a+b=1 ; c+d=1
         
 |Actual : YES (or) b |         | 3 (or) g |                      | 100 (or) h |
 
- This is a sample of 2x2 Confusion Matrix (a binary classifier)
- There are two possible predicted classes - "Yes" and "No", but the reality also has two classes - "Yes" and "No"
- In the above case, the classifier predicts a person's disease status as"yes"(117 times) whereas it predicts "no"(33 times)
- But in reality, 103 patients have the disease and 47 do not.

- The basic terminology in Confusion matrix are:
[ Positives indicate that our prediction was correct and Negatives imply our predictions were wrong]
 i. True Positives(TP): This means we predicted the person has disease, and the person had the disease. [100]
 ii. True Negatives(TN) : This mean we predicted, the person do not have disease and in reality it was true(he didn't have any disease).[30]
 iii. False Positive(FP) : This means we predicted yes, but they don't actually have the disease.[17]
 iv. False Negative(FN) : This means we predicted no, but they actually have the disease.[3]

This is a list of rates that are often computed from a confusion matrix for a binary classifier:

- The probability that an event is assigned a positive classification, d, is sometimes called the classification incidence or test incidence.
- The probability that the condition is actually present, b, is also called condition “incidence. 
 - ** Accuracy** : Overall, how often is the classifier correct?
 (TP+TN)/total = (100+30)/150 = 0.867
- ** Misclassification Rate ** : Overall, how often is it wrong?
 (FP+FN)/total = (17+3)/150 = 0.133 ; equivalent to 1 minus Accuracy also known as "Error Rate"
- ** True Positive Rate ** : When it's actually yes, how often does it predict yes?
     TP/actual yes = 100/103 = 0.970 ; also known as "Sensitivity" or "Recall"
- ** False Positive Rate ** : When it's actually no, how often does it predict yes?
     FP/actual no = 17/47 = 0.638
- ** True Negative Rate ** : When it's actually no, how often does it predict no?
     TN/actual no = 30/47 = 0.83 ; equivalent to 1 minus False Positive Rate, also known as "Specificity"
- ** Precision ** : When it predicts yes, how often is it correct?
     TP/predicted yes = 100/117 = 0.854
- ** Prevalence ** : How often does the yes condition actually occur in our sample?
     actual yes/total = 103/150 = 0.68

| Probability Distributions | 				| Name |
         | P(X) |		         | p(a,b) | 	   | Marginal Probability of the Condition |
         | P(Y) |		         | p(c,d) |                    | Marginal Probability of the Classification | 
        | p(X,Y) |		       | p(e,f,g,h) |	            | Joint Distribution of X and Y |
       | P(X)P(Y) | 		   | p(ac,ad,bc,bd) |	           | Product Distribution of X and Y |

| Conditional Probabilities |		                        | Name |
 | p(Test POS | "+") |		| h/b |	                  | True Positive Rate |
 | p(Test NEG | "+") |		| g/b |	                  | False Negative Rate |
 | p(Test POS | "-") |		| f/a |	                  | False Positive Rate |
 | p(Test NEG | "-") | 		| e/a |	                  | True Negative Rate |
				
 | p("+" | Test POS) |		| h/d |		| Positive Predictive Value (PPV) |
 | p( "-" | Test POS) |		| f/d |                              | 1- PPV |
 | p("+" | Test NEG) |	                   | g/c |		| 1- NPV |
 | p("-" | Test NEG) |		| e/c |		| Negative Predictive Value (NPV) |

- And they have given an example of Bombers and Seagulls, to explain every term mentioned above in Detail...
- The typical way that we characterize a particular threshold is by its false positive rate and its true positive rate.

## ** Area under Curve[AUC] ** ##

- Its two great strengths are, first, that AUC results do not change with changes in the incidents of the actual condition, 
nor is AUC affected by changes in the relative cost of the two different types of binary classification errors, false positives and false negatives. 
- The AUC metric ranges from a minimum of one-half to a maximum of one. An AUC of one-half indicates total uncertainty about classification. 
An AUC of one-half is a result when guessing outcome are random.
- An AUC of one would be classification with zero errors, a theoretical ideal that no one expects you to meet.
- A normal good to very good area under the curve is typically in the .65 to .85 range. 



