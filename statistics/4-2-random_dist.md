[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> import numpy as np  
randomlist=[]  
for x in range(1,1000):  
    randomlist += [np.random.random()]  
cdf_random = thinkstats2.Cdf(randomlist)  
pmf_random = thinkstats2.Pmf(randomlist)  

thinkplot.Pmf(pmf_random)  
thinkplot.show(xlabel='percentile rank', ylabel= 'PMF')  

thinkplot.Cdf(cdf_random)  
thinkplot.show(xlabel='percentile rank', ylabel= 'CDF')  

In the PMF distribution, it looks like a solid block because if there are a 1000 samples in a truly random sample, each sample should have a .1% chance of showing up (1000) * .001=1.   

In the CDF distribution, the graph is accumulating the probabilities, so each sample beyond the first will be .1% higher.  

As the sample size increases (n=100,000), we see the graph smooth out to a straight line.  
