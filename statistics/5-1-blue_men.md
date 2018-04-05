[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>> import scipy.stats  
   mu = 178  
   sigma = 7.7  
   dist = scipy.stats.norm(loc=mu, scale=sigma)  

dist.cdf(73 * 2.54)-dist.cdf(70 * 2.54) #upperbound CDF-lower bound CDF
