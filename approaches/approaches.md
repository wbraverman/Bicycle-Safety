# Approaches

## Planning

### Feature Encoding

To try different approaches, we plan to encode our categorical features in different ways to be able to use them in the model. We have the following three ways of encoding our features:

- One-hot encoding, where we obtains n - 1 new columns, where n is the number of different values.
- Encoding most prevalent vs. not prevalent i.e. for BikeSex, we could classify Men vs Not Men.
- Encoding most ideal vs not ideal i.e. for Weather, we could classify Clear vs. Not Clear.

The last two encoding methods could match. One-hot encoding could result in lots of new columns, so we'll mostly try it in columns where there's not lots of different values and each different values appears frequent enough.

### Result Encoding

The goal of our KPIs involves understanding how severe an accident would be (if it happens) based on the conditions provided. We have two columns that could provide that info: BikeInjury and AmbulanceR. Our approaches will encode these columns in different ways to obtain different models:

- Use BikeInjury as is, resulting in 5 categories, from lowest to highest severity: No Injury, Possible Injury, Suspected Minor Injury, Suspected Major Injury, Killed.
- Encode BikeInjury into two values: Severe (grouping Suspected Major Injury and Killed) vs. Not Severe.
- Use AmbulanceR as is, which is already binary, where a true value is equivalent to a Severe Injury.

For the last two columns, we could compare performances more easily as they both have results in binary. Thus, we could compare performances by using accuracy, precision, recall, confusion matrix, etc.

### Model Approach

Since we have lots of categorical features, we concluded that the models that could work for our scenario are the following 3:

- Logistic Regression
- Decision Trees
- Random Forests

We plan to try different approaches on the encoding for each of these models. We'll keep constant the encoding approach and test it on all three different models, to see how each of them perform.

## Results

### Approach 1