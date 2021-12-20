# Credit_Risk_Analysis

<p>**Overview**<p>
<p> The purpose of this analysis is to help a peer-to-peer lending services company LendingClub, use the Loan Stats data to find a model that appropriately predicts credit risk <p>
  
<p> **Results**<p>
  Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.
<p>Naive Random Oversampling<p>
<p>https://github.com/JoePizz/Credit_Risk_Analysis/blob/main/Screenshots/Naive_Random_Oversampling.png<p>
<p>Accuracy score: 64.03%<p>
<p>Precision<p>
    <p>High risk: 0.01<p>
    <p>Low risk: 1.00<p>
<p>Recall<p>
    <p>High risk: 0.62<p>
    <p>Low risk: 0.66<p>
<p>
  
<p>SMOTE Oversampling<p>
<p>https://github.com/JoePizz/Credit_Risk_Analysis/blob/main/Screenshots/SMOTE_Oversampling.png<p>
<p>Accuracy score: 65.15%<p>
<p>Precision<p>
    <p>High risk: 0.01<p>
    <p>Low risk: 1.00<p>
<p>Recall<p>
    <p>High risk: 0.61<p>
    <p>Low risk: 0.69<p>
<p>ClusterCentroids resampler<p>
<p>https://github.com/JoePizz/Credit_Risk_Analysis/blob/main/Screenshots/Undersampling.png<p>
<p>Accuracy score: 65.15%<p>
<p>Precision<p>
    <p>High risk: 0.01<p>
    <p>Low risk: 1.00<p>
<p>Recall<p>
    <p>High risk: 0.69<p>
    <p>Low risk: 0.40<p>
<p>-->Attempts to address the imbalance in the data, however this adjustment does not allow the algorithm to read the data more accurately. The high risk's are identified more accurately, however there is a significant drop in the low risk identification. This would result in less high risk loans being given out improperly, but would also result in less loans overall being given out.<p>
<p>SMOTEENN<p>
<p>https://github.com/JoePizz/Credit_Risk_Analysis/blob/main/Screenshots/Combination(Over_and_Under).png<p>
<p>Accuracy score: 54.44%<p>
<p>Precision<p>
    <p>High risk: 0.01<p>
    <p>Low risk: 1.00<p>
<p>Recall<p>
    <p>High risk: 0.72<p>
    <p>Low risk: 0.57<p>
<p>-->The SMOTEENN algorithm had the lowest balanced accuracy score of all the algorithms. As the minority sample in this dataset and in the population is very small, the SMOTEENN model appears to over represent the high risk population and thus misrepresent the overall results.
<p>BalancedRandomForestClassifier<p>
<p>https://github.com/JoePizz/Credit_Risk_Analysis/blob/main/Screenshots/Balanced_Random_Forest.png<p>
<p>Accuracy score: 78.85%<p>
<p>Precision<p>
    <p>High risk: 0.03<p>
    <p>Low risk: 1.00<p>
<p>Recall<p>
    <p>High risk: 0.70<p>
    <p>Low risk: 0.87<p>
<p>-->The BalancedRandomForestClassifier had slightly better precision results with the High Risk results compared to the Oversampling and SMOTEENN algorithms. The Recall results for Low risk were also better than these algorithms.
<p>AdaBoostClassifier<p>
<p>https://github.com/JoePizz/Credit_Risk_Analysis/blob/main/Screenshots/Easy_Ensemble_AdaBoost.png<p>
<p>Accuracy score: 93.17%<p>
<p>Precision<p>
    <p>High risk: 0.09<p>
    <p>Low risk: 1.00<p>
<p>Recall<p>
    <p>High risk: 0.92<p>
    <p>Low risk: 0.94<p>
<p>-->Highest racall scores for Low Risk and High Risk as well as the highest Accuracy Score of all the algorithms.<p>

<p>**##Summary**##<p>

<p>It appears that the OverSampling had better recall scores than that of the resampling methods.<p>
<p>As this is a peer to peer lending service the company may want to focus more on eliminating high risk credit scores than identifying low risk credit scores. As lending from individuals is already more risky than lending from a financial institution, the less high risk credit scores that are brought in, the more successful the platform will become.<p>I would recommend using the AdaBoostClassifier. This algorithm not only is able to identify low risk credit but is also able to identify high risk credit as well.<p>
