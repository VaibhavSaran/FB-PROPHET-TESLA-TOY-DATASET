
# PRODUCT FORECASTING USING FB PROPHET

## Acknowledgements
I take this opportunity to express my sincere thanks to [Data Science Dojo](https://www.youtube.com/watch?v=wXS9IzDjuZQ&t=321s) and Mr. Nicholas Renotte for conducting an amazing webinar on FB prophet where I got to learn about this amazing framework by Facebook. Following the instructions I worked on the same dataset as in the webinar and got a thorough understanding of many concepts.
This small project was an amazing journey of learning and I have enclosed some of the links which have helped me during my journey to make this project with some resource guides for future improvements and learnings.
- [Nicholas Renotte](https://github.com/nicknochnack)
- [FB PROPHET](https://facebook.github.io/prophet/)
- [TIME SERIES FORECASTING WITH PYTHON](https://machinelearningmastery.com/time-series-forecasting-with-prophet-in-python/)
- [GENERATE QUICK AND ACCURATE TIME SERIES FORECAST](https://www.analyticsvidhya.com/blog/2018/05/generate-accurate-forecasts-facebook-prophet-python-r/)
- [TIME SERIES ANALYSIS WITH FACEBOOK PROPHET](https://towardsdatascience.com/time-series-analysis-with-facebook-prophet-how-it-works-and-how-to-use-it-f15ecf2c0e3a)
- [STAN](https://mc-stan.org/)
- [TIME SERIES PREDICTION WITH LSTM RNN](https://machinelearningmastery.com/time-series-prediction-lstm-recurrent-neural-networks-python-keras/)
- [DEVELOP LSTM MODEL FOR TIME SERIES FORECASTING](https://machinelearningmastery.com/how-to-develop-lstm-models-for-time-series-forecasting/)
- [LSTM FRAMEWORK FOR UNIVARIATE TIME SERIES PREDICTION](https://towardsdatascience.com/lstm-framework-for-univariate-time-series-prediction-d9e7252699e)
- [MULTIVARIATE TIME SERIES FORECASTING](https://machinelearningmastery.com/multivariate-time-series-forecasting-lstms-keras/)
- [MULTIVARIATE MULTI-STEP TIME SERIES FORECASTING](https://www.analyticsvidhya.com/blog/2020/10/multivariate-multi-step-time-series-forecasting-using-stacked-lstm-sequence-to-sequence-autoencoder-in-tensorflow-2-0-keras/)
- [STOCK PREDICTION USING FB PROPHET](https://towardsdatascience.com/time-series-forecasting-predicting-stock-prices-using-facebooks-prophet-model-9ee1657132b5)
- [KAGGLE NOTEBOOK ON PROPHET](https://www.kaggle.com/kashnitsky/topic-9-part-2-time-series-with-facebook-prophet)
- [HOW DOES FB PROPHET WORK](https://medium.com/tokopedia-data/hacking-time-series-forecasting-like-a-pro-with-fbprophet-76f276f0a058)
- [ABOUT FB PROPHET](https://research.fb.com/prophet-forecasting-at-scale/)

## About Facebook Prophet
According to Sean Taylor, a research scientist at Facebook and Stan user told that, Prophet uses Stan for optimization (and sampling if the user desires) in order to fit a non-linear additive model and generate uncertainty intervals. The advantages they got by using STAN was:
1) STAN does a great job of letting a user separate optimization from the model code.<br>
2) It could share the same core implementation in both python and R.<br>
Prophet is automatically detect changepoints in the time series by specifying a sequence potential parameter changes and shrinking the shifts using a Laplace prior. The user is allowed to adjust the flexibility of the model by tuning precision of priors, which is intuitive for most users.
At its core, the Prophet procedure is an additive regression model with four main components:
-   A piecewise linear or logistic growth curve trend. Prophet automatically detects changes in trends by selecting changepoints from the data.
-   A yearly seasonal component modeled using Fourier series.
-   A weekly seasonal component using dummy variables.
-   A user-provided list of important holidays.
In layman terms, we can understand it as follows:
FBProphet uses decomposable time series model with 3 main components: seasonal, trends, holidays or events effect and error which are combined into this equation:

                                    f(x) = g(x) + s(x) + h(x) + e(t)

FBProphet uses time as a regressor and tries to fit several linear and nonlinear function of time as components. By default, FBProphet will fit the data using a linear model but it can be changed to the nonlinear model (logistics growth) from its arguments.

## Minimum Requirements
I would recommend using Google Colab or Kaggle notebook because installing FB Prophet on your local PC can be quite a hassle

## Executing Project
Run all the cells of the notebook **FB_PROPHET.ipynb** to see prophet working on the dataset.

## Data Collection
I have used a toy tesla data set which has been highly curated for starters in FB Prophet.

## Future Scope and Improvements
1) Adding more data to perform better predictions.
2) Adding parameters to take care of holidays and seasons.