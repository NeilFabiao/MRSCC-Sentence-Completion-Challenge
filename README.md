# Unbiased ML tradeoff  #

In recent years the advancement of AI (artificial intelligence) especially ML (machine learning) has increased automation for tasks in different domains. For example, recommender systems, student admission and job recruitment. With such has risen the concern for bias and discrimination created by these systems [3]. For instance, in the US nonwhites (Black, Hispanic, and Asian) are more likely to be convicted for a similar crime committed by Caucasian people. Moreover, Amazon's job recruitment systems demonstrated bias toward female applicants [4]. These challenges inspired the creation of many tools. Such as AIF360 from IBM and Ethicml from the University of Sussex. To overcome existing fairness and accuracy controversy.

![alt-text-1](/Project/img/bongo.gif)

### Understanding the problem ###

* `Size of the dataset` - In this coursework Adult income with two main sensitive features race and sex and is the largest dataset with 48842-row instances. The second dataset is German credit data (Statlog) with age, sex and foreign worker as sensitive features. Machine learning models tend to underperform when data avaliability is limited insrespective of the evaluation metrics and type of model. 

* `Decision Tree classifier` - Applying a decision tree classifier on the training folds without sensitive features produced nonbiased fairness scores. However, Certain variables because of the nature of a problem are correlated to the outcome of the solution provided by the ML method. For instance, highly correlated features such as neighbourhood may be a proxy for a sensitive attribute for instance race [5]. 

* `Gerry Fair Classifier` - produces almost similar results when it comes to the regularization parameter (figure 8 in the appendix of the report). For instance, as the C parameter increases our model is less fair and prioritizes balanced accuracy. On the other hand, for small values of C, the model focuses on fairness. Moreover, as the number of epochs increases, this model tends to better understand the data. The performances of Garry fair and adversarial
debiasing are improved after pre and post-processing techniques are applied

* `Removing sensitive feature` -  Applying a decision tree classifier on the training folds without sensitive features produced nonbiased fairness scores. However, Removing the sensitive feature or known as unawareness is not the best solution. Certain variables because of the nature of a problem are correlated to the outcome of the solution provided by the ML method. For instance, highly correlated features such as neighbourhood may be a proxy for a sensitive attribute for instance race [5].

* `Beyond binary features` - For instance, in the German dataset using the job categorical variable is a protected attribute. With adversarial debiasing, the fairness metrics were favouring the minority with scores ranging from - 0.01 to 0.01. While the accuracy stayed below 0.70 reaching as low as 0.30. Nonetheless, studying the effects of relationship variables on the adult dataset proved to be fruitful. Given the size of the dataset, the accuracy ranged from 0.82 to 0.75 while the fairness score was -0.04 to 0.

### Results ###

![alt-text-1](/Project/img/res1.png)

![alt-text-1](/Project/img/res2.png)

### Repo structure ###

This project was done using python (jupyter-notebook), and in the Project folder there are 3 other subsequent folders namely:

* src - or source code where the different implementations of the knapsack problem are located. 
* pdf - where summary of the work is present. 
* img - has the visualization gif used in the repo 😁.

To run the implementations located in src simply select the '.ipynb' file. 

*Note:* The complete report for this project will be made avaliable for the time being.

### References ###

1. Machine Learning lecturer and TA's @ Sussex uni

2. Github and google

3. Castelnovo, A., Crupi, R., Greco, G., Regoli, D., Penco, I.G. and Cosentini, A.C. (2022). A clarification of the nuances in the fairness metrics landscape. Scientific Reports, 12(1). doi:10.1038/s41598-022-07939-1.

4. Richardson, B. and Gilbert, J. (2021). A Framework for Fairness: A Systematic Review of Existing Fair AI Solutions. Journal of Artificial Intelligence Research,[online] 1. Available at: https://arxiv.org/pdf/2112.05700.pdf.

5. IBM Research Trusted AI (n.d.). AI Fairness 360. [online] aif360.mybluemix.net. Available at:https://aif360.mybluemix.net.


### Who do I talk to? ###

* Repo owner Neil Fabião -> @neilfabiao ✌🏾

![](https://komarev.com/ghpvc/?username=neilyML120&color=red)
