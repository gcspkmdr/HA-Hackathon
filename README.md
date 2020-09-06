# HA-Hackathon

Some of the amazing work by the fellow kagglers that i explored:

* https://www.kaggle.com/cdeotte/xgb-fraud-with-magic-0-9600

* https://www.kaggle.com/c/ieee-fraud-detection/discussion/108575

* https://www.kaggle.com/c/cat-in-the-dat-ii/discussion/140465

* https://www.kaggle.com/cdeotte/how-to-choose-cnn-architecture-mnist (used this for CV with nnets)

* https://www.kaggle.com/c/siim-isic-melanoma-classification/discussion/175614

# Feature Engineering
https://www.kaggle.com/gcspkmdr/lets-get-rid-of-the-patients-feature-engineering

# Algorithms Used
1. All variants have used the same features

2. Explicitly telling the classifier that a certain feature is categorical gave boost to performance

LGBM Classifier
https://www.kaggle.com/gcspkmdr/lets-get-rid-of-the-patients

XGB Classifier
https://www.kaggle.com/gcspkmdr/lets-get-rid-of-the-patients-xgboost

CatBoost
https://www.kaggle.com/gcspkmdr/lets-get-rid-of-the-patients-catboost

Various NN architecture via DeepTables (https://github.com/DataCanvasIO/deeptables/blob/master/docs/source/models.md)

https://www.kaggle.com/gcspkmdr/a-model-built-on-garbage-deeptables-pnn

https://www.kaggle.com/gcspkmdr/a-model-built-on-garbage-deeptables-dcn

https://www.kaggle.com/gcspkmdr/a-model-built-on-garbage-deeptables

https://www.kaggle.com/gcspkmdr/a-model-built-on-garbage-deeptables-opnn

# Findings

1. LGBM is very slow. GPU usage didn't help much(Also you have to build it every time you open the notebook)

2. GPU hurt the performance also in case of LGBM. The multi log loss didn't decrease to same level as compared to CPU

3. XGB also didn't sped up much with GPU

4. CatBoost was the best among gradient tree based methods

5. CatBoost was performed well in terms of performace and speed with GPU

6. NN architecture with the capabilty of converting tabular categorical features to emeddings performed the best

7. There was corelation between the validation loss and validationn accuracy. This was most likely because of the poor quality of dataset

Things to explore

RapidAI for feature enginering(Pandas dataframes are too slow. RapidAI uses GPU to speed up the proces)

Dask Dataframes for feature engineering

# Ensembling

https://www.kaggle.com/gcspkmdr/let-s-get-rid-of-the-patients-ensemble

2 X NN are used(DCN and PNN)

# Adversarial Validation
For sanity check

https://www.kaggle.com/gcspkmdr/adversarial-validation-on-garbage
