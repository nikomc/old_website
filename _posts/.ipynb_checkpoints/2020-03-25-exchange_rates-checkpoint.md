---
layout: post
title: "Exchange Rate Viewer"
author: "Niko McCarty"
categories: blog
tags: [blog,exchange,rates,country,data]
image: data_unsplash.jpg
sect: home
mathjax: true

---
Explanation of data. Explain my practice of Python and cleaning data in particular. 

{% include 2020_03_25_exchange_rates.html %}

{% include 2020_03_25_exchange_rates_dropdown.html %}

Data was pulled from [Kaggle](https://www.kaggle.com/brunotly/foreign-exchange-rates-per-dollar-20002019) and tidied in Python. Dates were converted to datetime format, columns were melted, and data (which was given by day) was aggregated into weekly means for the exchange rates.

The full Jupyter notebook is available from [GitHub](https://github.com/nikomc/Interactives_Python/blob/master/notebooks/2020-03-20_exchange_rates.ipynb).

