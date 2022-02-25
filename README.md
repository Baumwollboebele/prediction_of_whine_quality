# Prediction of Wine Quality

[Summary](#summary)
[Dataset](#dataset)
[Results](#results)

**Note: The actual work is written in german, though it can be read in english since the majority of the work consists of python code and statistical analysis.**

## Summary

The Jupyter Notebook in this repository is dedicated to predicting wine quality of Vinho Verde.
Vinho Verde, or the green wine, is a young Portuguese wine that comes from the growing areas between the Douro and Minho rivers in northern Portugal.
The grape varieties used include Alvarinho, Avesso, Loureiro and Trajadura. Occasionally, the grape variety Sercial is also used.

>Life is too short to drink bad wine. - Johann Wolfgang von Goethe.


## Dataset

The dataset is from UCI's Machine Learning Repository and was entered there on 10/07/2009.
 It contains data for white wine and red wine of Vinho Verde, whereas only the data set of white wines is relevant for this Jupyter Notebook.
The dataset contains 12 different attributes, for this work the first 11 attributes were declared as features and the last attribute - Quality - as a target variable.
For the white wine dataset there are 4898 data points.
It should be noted that the quality was evaluated by wine experts. This means that the wine quality was determined based on subjective perceptions of the experts.

| **Attribut** | **Summary** | **Unit** |
|-----------|---------------|-------------|
| Fixed Acidity | Tartaric acids, which occur in solid and non-volatile states.|g/dm^3|
| Volatile Acidity | Acetic acid, which in high concentrations lead to a vinegar taste.|g/dm^3|
|Citric Acid| Citric acid, which give freshness to wines in small quantity.|g/dm^3|
|Residual Sugar|Sugar, which remains after fermentation.| g/dm^3|
|Chlorides| Salinity of the wine. | g/dm^3|
|Free Sulfur Dioxide| Sulfur dioxide which occurs as a dissolved gas and bisulfite ion. It prevents microbial growth and oxidation of the wine.|g/dm^3|
|Total Sulfur Dioxide|Total amount of sulfur dioxide in free and bound form. | g/dm^3|
|Density| Density | g/cm^3|
|pH|Gibt die Säure bzw. Base der Lösung an. 1 = sehr sauer bis 14 = sehr basisch.|Discrete value between 1-14|
|Sulphates| Sulphates, which are added to the wine and contribute to the content of sulfur oxides, which have antimicrobial and antioxidant effects. | g/dm^3|
|Alcohol|Alcohol content of the wine.|Volume percent|
|Quality| Median der Weinqualität aus 3 Evaluationen gegeben von Weinexperten. 1 = Schlecht zu 10 = Sehr Gut. |Discrete value between 1-10|

Source:
[Cortez et al., 2009]

## Results

A **random forest regressor** model achieved the best results. The feature selection led to a strong loss of information in this data set and thus to significantly worse results.
The poorer results for the less represented classes were to be expected and acceptable, since they occur only in very small numbers in the entire data set. Weighting or oversampling these groups to degrade the precision of the more frequently occurring classes. This can lead to models on future data preferring the prediction of the less frequent classes and thus the class distribution of the prediction and that of the real values differ.
In principle, this data set must be treated critically, since the subjective classification by wine experts is not a scientifically based classification and poorer results of models could also be attributed to an inconsistency of this classification.


Translated with www.DeepL.com/Translator (free version)
