# Research Ideas: Fairness of Software Engineering
## Base Research by Joymallya Chakraborty on Fair-SMOTE [(Paper)](https://www.researchgate.net/figure/Many-tools-try-to-find-or-explain-or-mitigate-bias-Fair-SMOTE-addresses-all-three_fig1_351892971)

## Option A
The Fair-SMOTE data balancing method does perfect balance. That means training data contains 25% examples of each subgroup (Male-Positive, Male-Negative, Female-Positive, Female-Negative). We could maybe show the change of bias scores with respect to different balancing ratios.

What happens when you have 70% Male-Positive, 10% Male-Negative, 10% Female-Positive, 10% Female-Negative?
What happens when you have 10% Male-Positive, 70% Male-Negative, 10% Female-Positive, 10% Female-Negative?

## Option B
Joy uses situation testing to remove biased data points. Joy used logistic regression. Our question is, will different families of algorithm used in situation testing change the bias in the result?
We will choose one type of algorithm in each family and run situation testing on the same set of data.

We then will compare the bias score on each family of algorithm and see if there are significant changes in the scores. 

## Joy's paper

The paper postulates that:
* The root causes of bias are the prior decisions that affect- What data was selected and 
* The labels assigned to those examples

Fair-SMOTE algorithm removes biased labels; and rebalances internal distributions such that based on sensitive attribute, examples are equal in both positive and negative classes. On testing, it was seen that this method was just as effective at reducing bias as prior approaches. Further, models generated via Fair-SMOTE achieve higher performance (measured in terms of recall and F1) than other state-of-the-art fairness improvement algorithms.

## Critique on Fair-SMOTE
- How does it compares with other algorithims that also try to remove bias?
- Does the algorithm behaves the same when presented with different set of data that has different characteristics?
- Is there any way to improve the algorithm to make the output more accesible for non-technical persons?
- **Situation Testing**: Is this the only reliable tactic to detect discrimination, is there any other method that we could compare to?
- **Situation Testing**: Chakraboty uses logistic regression model but could we use different model and compare its effectiveness?

## Supporting Research [Fairness in Machine Learning Survey](literature/Fairness-in-ML-Survey.pdf)
- with automated decision using AI become more prevalent, fairness consideration needs to be investigated further
- Fairness in ML key methodological components:
  - Pre-processing, in-processing, post-processing. We need a fairness metrics
  - For metrics, we have individual and group fairness. Increasing fairness often results in lower accuracy.
- Pre-processing: Argued as the modt flexible as it makes no assumption with respect to the choice of subsequently applied modeling technique. 

## Supporting Research [Impact of Data Preparation on the Fairness of Software Systems](literature/Role-of-Preprocessing.pdf)
- This paper asses the impact of widely adopted data preparation procedures on AI model performance and fairness.
- Data preparation is key in any machine learning pipelines, but its effect on fairness is yet to be studied in detail. The development of AI model could raises societal and legal concerns, as their decision may lead to unfair treatment of individuals based on attributes such as race and gender. 
  - Removal of Sensitive Attributes
  - Encoding of Categorical Attributes
  - Instance Selection Method using Cross validation and random undersampling
- **Experiment:**
1. conduct the experiment with 2 dataset, and performed a
70/30 stratified split to maintain the distributions of
the true labels and the sensitive attribute on each set. 
2. discretise .the numerical
attributes into 4 bins with the boundaries corresponding to those of the interquartile ranges.
3. rebalance the dataset using sampling.
4. performed experiments with Decision Trees and
Random Forests. Assert with five-fold cross-validation with the help of
the methods provided by Scikit-learn."

