# Research Ideas: Fairness of Software Engineering

## Base Research by Joymallya Chakraborty on Fair-SMOTE [(Paper)](https://www.researchgate.net/figure/Many-tools-try-to-find-or-explain-or-mitigate-bias-Fair-SMOTE-addresses-all-three_fig1_351892971)
The paper postulates that:
* The root causes of bias are the prior decisions that affect- What data was selected and 
* The labels assigned to those examples

Fair-SMOTE algorithm removes biased labels; and rebalances internal distributions such that based on sensitive attribute, examples are equal in both positive and negative classes. On testing, it was seen that this method was just as effective at reducing bias as prior approaches. Further, models generated via Fair-SMOTE achieve higher performance (measured in terms of recall and F1) than other state-of-the-art fairness improvement algorithms.

## Critique on Fair-SMOTE
- How does it compares with other algorithims that also try to remove bias?
- Does the algorithm behaves the same when presented with different set of data that has different characteristics?
- Is there any way to improve the algorithm to make the output more accesible for non-technical persons?
- **Situation Testing**: Is this the only reliable tactic to detect discrimination, is there any other method that we could compare to?
- - **Situation Testing**: Chakraboty uses logistic regression model but could we use different model and compare its effectiveness?
