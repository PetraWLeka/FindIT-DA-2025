# My competition solution for Data Analytics Competition - Find It 2025
https://www.kaggle.com/competitions/data-analytics-competition-find-it-2025/overview

Public Score: 0.89509
Private Score: 0.89154

## Strategy:
The label class is imbalanced, with the proportion between the "True" and "False" labels being around 1:9. To address this, my proposed solution is to break the "False" label into 9 parts and pair each part with a "True" label. This approach results in a 1:1 label distribution for each subset. Since there are 9 parts of data, I trained 9 models.
I applied three different models: LightGBM, XGBoost, and CatBoost. I fine-tuned the parameters using Optuna and evaluated the results. Then, I combined the predictions from all the models and averaged them, which is essentially a voting approach for the 27 models (9 parts × 3 models = 27).

## Future improvements:
- More comprehensive data processing.

- Explore other ensemble methods such as bagging, meta-learning, and boosting.

- Longer parameter fine-tuning process.
![Uploading image.png…]()
