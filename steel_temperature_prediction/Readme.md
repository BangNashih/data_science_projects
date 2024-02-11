# Optimization of production costs
In order to optimize production costs, the smelter decided to reduce electricity consumption during the steel processing stage.

**The objective** is to build a predictive model for the final steel melting temperature.

**Stack:** `Pipeline` `Optuna` `pandas` `Catboost` `XGBoost` `Scikit-Learn`

## Conclusion
An analysis of the steel melting process has been conducted, encompassing datasets included electrodes, bulk materials (volume and supply time), gas purging of the alloy, wire materials (volume and time), and temperature measurements of the steel.

During the metal melting process, electrodes play a pivotal role in heating the ladle. The heating power, characterized by active and reactive power, reflects the conversion of electrical energy into useful heat and the loads created in electrical devices due to fluctuations in the electromagnetic field.

To achieve specific steel grades, loose and wire-like materials are added and stirred with gas to achieve targeted composition. The dataset includes 15 bulk materials and 9 wire materials. Notably, there are gaps in the data, as only certain substances are added for a given batch for different composition. The frequency of material additions are vary, certain materials being added more frequently than others.

For model training, a processed dataset was done. Encompassing initial and final steel temperatures, time intervals between temperature measurements, active and reactive power of electrodes, number of electrode heatings, arc heating time, gas volume, and volumes of various bulk and wire materials.

Finally, the most effective model for predicting the final temperature of a steel batch is the CatBoost Regression Model with optimized hyperparameters:

- `'iterations': 955,`
- `'learning_rate': 0.03602696633625084,`
- `'depth': 5,`
- `'l2_leaf_reg': 3,`
- `'border_count': 66,`
- `'random_seed': None`

This model demonstrated a Mean Absolute Error (MAE) of 5.4 in training data and 5.69 degrees on the test sample (indicating a reliable performance).
