## Recruit Restaurant Visitor Forecasting

### Description

This repository is a summary of my personal solution and EDA of the Kaggle Competition[Recruit Restaurant Visitor Forecasting](https://www.kaggle.com/c/recruit-restaurant-visitor-forecasting). The task is to predict how many future visitors a restaurant will receive in a certain day.


### My Rude Strategy

I entered the competition very late when there was only 12 days left. So the first thing I did was to explore all the most-voted EDA kernels... There are pretty fantastic EDA kernels and I have wrapped up them in the EDA folder(with my note). You can also access [here](https://www.kaggle.com/c/recruit-restaurant-visitor-forecasting/kernels). The EDAs gave me practical insights about the underlying **overfitting** problem, which is very **serious** in this competition! Generally, one thing is that reservation data are complete in training set, but mostly missing in testing set; the other thing is Japan's Golden Week with high-peak population of visitors are in the private testing set.

I started from the _Suprise me_ kernels, which was a good beginning of feature selection, engineering and model ensembling.  What I did was mainly four things:

1. _Remove reservation info within 4 weeks to avoid overfitting_
2. _Add weather features. Take average of weather stations within 20km to avoid missing value._
3. _Take feature indicating new year and Golden Week_
4. _Further feature selection, parameter tuning and cross validation(I didn't do enough on this part because little time and submission left for me)_


As a result : My public LB is 0.478 and private LB is 0.518, which ranks top 10%.


### How to use them

1. You need to install python3 and anaconda with jupyter notebook. More detail is [here](http://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/install.html)
2. `cd` to the cloned repository and run `jupyter notebook`
3. Access datasets. [Competition data](https://www.kaggle.com/c/recruit-restaurant-visitor-forecasting/data) and a summarized [weather data](https://www.kaggle.com/gedoumaru/weather-store)
3. Instruction for files. _Modeling.ipynb_ is my solution file. I've also collected other solutions from kernel such as _H2OAutoML.ipynb_, which is interesting to learn how to use H20AutoML. More information about the dataset can be found in the EDA folder.

### Summary

It's not a hard competition considering the formulation of the problem and the scale of the data, but avoiding overfitting is pretty tricky(You can take a look at the rank shake-up...). Good luck for the next competition...


