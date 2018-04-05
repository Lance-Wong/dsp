[Think Stats Chapter 6 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2007.html#toc60) (household income)

>> import hinc
income_df = hinc.ReadData()
log_sample = InterpolateSample(income_df, log_upper=6.0)
log_cdf = thinkstats2.Cdf(log_sample)
thinkplot.Cdf(log_cdf)
thinkplot.Config(xlabel='Household income (log $)', ylabel='CDF')
sample = np.power(10, log_sample)
cdf = thinkstats2.Cdf(sample)
thinkplot.Cdf(cdf)
thinkplot.Config(xlabel='Household income ($)', ylabel='CDF')


Median(sample), Mean(sample), Skewness(sample),PearsonMedianSkewness(sample)

(51226.454478940461,
 74278.707531187334,
 4.9499202444295829,
 0.7361258019141782)

cdf.Prob(74278.707531187334)
0.66000587956687196

The sample is skewed right, as Skewness and Pearson Skewness are both positive. If the upperbound increases to 10 million dollars, the mean will increase dramatically while the median will stay relatively same.