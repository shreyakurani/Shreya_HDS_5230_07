## Week 12 – Deep Learning vs XGBoost Model Comparison

## What I Did:-

In this week’s assignment, I built a few with deep learning and compared them with the XGBoost ones from last week. (I was also interesting to see how you would trade off with these different approaches.) All of the code and analysis files that I have used for the assignment are in this folder.

## My Deep Learning Models
Two different neural network setups were tested:

A model with just 1 hidden layer (4 nodes)
thus, a slightly more complex model with 2 hidden layers (4 nodes each)

I ran both models on 1,000, 10,000 and 100,000 rows to see what impact data had on the result. For each run, I tracked:

Training error
Using a holdout set to validate error
How long it took to train

Since the models initially outputted accuracy scores, I calculated the error values as error = 1 - accuracy.

## Comparing with XGBoost:- 
I used my new deep learning models and compared the results with the XGBoost results from Week 11’s assignment. The comparison was on both prediction performance (which one is more accurate) and computational efficiency (which one is faster to train).

## Files in This Folder:- 

Week12_DeepLearning_vs_XGBoost_Report_SaumilKurani.docx: My written report with analysis and conclusions
Week12_Neural_Network_Modeling.ipynb: The Jupyter notebook with all my code and outputs
synthetic_data_1000.rds: The small dataset (1k rows)
synthetic_data_10000.rds: The medium dataset (10k rows)
synthetic_data_100000.rds: The large dataset (100k rows)

## Key Takeaways :- 

What I Found The most interesting of all was that the deep learning model with 2 hidden layers trained on 100k rows gave the best overall performance. However, XGboost is much faster if the datasets are smaller.

The choice to use deep learning is such that if you need maximum accuracy and if you have time go with deep learning. However, if the speed is something that is important, then XGBoost may be your choice.

I also learnt how to apply them in every context and how the dataset size affects the performance.
