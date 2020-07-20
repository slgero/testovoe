### Task:
Create and train a network to predict day price direction of Amazon.com, Inc. (AMZN).

### Input:
Previous price candlesticks.

### Data:
You can get daily candlesticks [here](https://finance.yahoo.com/quote/AMZN/history?period1=863654400&period2=1589932800&interval=1d&filter=history&frequency=1d).
Period from 2019-01-01 to present will be used for testing, the rest you can split into train and validation as you would like.

### Target:
Binary classification, whether next day close will be higher than open.

### Deliverables:
-   Training script: should be able to train the model from scratch in less than one hour on a modest GPU.
-   Prediction script: predict direction for a given date.
 
### Expected time required:
3 hours, please don’t spend much longer than that.

We are interested more in the way the code is structured rather than the final metrics. ROC AUC > 0.515 will be enough.

You can submit code either as a zip archive or link to public git repository (GitHub/GitLab)