# Shoppers
# Online Shoppers Purchasing Intention: Statistical Analysis

This is a full statistical analysis (business questions, hypothesis tests,
descriptive and inferential statisticsand a logistic regression model) on
e-commerce session data, that examines what makes a browsing session end
with a purchase so the business can optimize

## my data source:

Online Shoppers Purchasing Intention Dataset, made by Akash Ram on Kaggle:
https://www.kaggle.com/datasets/imakash3011/online-shoppers-purchasing-intention-dataset

It has 12,330 online shopping sessions, each one described by page-visit
counts and durations, engagement metrics (`BounceRates`, `ExitRates`,
`PageValues`), visitor/session metadata (`Month`, `VisitorType`, `Weekend`,
`TrafficType`, ...), and a binary outcome `Revenue` that shows if the
session ended in a purchase or not.

## files

- `analysis.Rmd`: the full, executed analysis (R Markdown source)
- `analysis.pdf`: the knitted report (text + R code + output)
- `data/online_shoppers_intention.csv`: the source dataset

## reproduce

Inside this folder, using R:

```r
install.packages(c("tidyverse", "car", "pROC", "broom", "knitr", "rmarkdown", "scales"))
tinytex::install_tinytex()  # first time only, needed for PDF output
rmarkdown::render("analysis.Rmd")
```

the notebook uses a fixed random seed (42) for the stratified 80/20
train/holdout split, which is used to evaluate the logistic regression
model.
