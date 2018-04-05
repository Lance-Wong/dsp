[Think Stats Chapter 8 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2009.html#toc77) (scoring)

>> def E_Estimate(n,m=1000):
    def verticals(x,y=1):
        thinkplot.Plot([x,x],[0,y], color='.8', linewidth=3)
    
    lam = 2
   
    means = []
    for _ in range(m):
        xs= np.random.exponential(1.0/lam, n)
        L= 1/ np.mean(xs)
        means.append(L)
      
    print('Standard Error:', RMSE(means, lam))
    
    
    cdf = thinkstats2.Cdf(means)
    ci= cdf.Percentile(5), cdf.Percentile(95)
    print ('Confidence interval for means: ', ci)
    
    thinkplot.Cdf(cdf)
    thinkplot.Config(xlabel='Sample mean',
                     ylabel='CDF',
                    title= 'Sampling Distribution')
    verticals(ci[0])
    verticals(ci[1])
    
    

E_Estimate(10)

Standard Error: 0.776810172362
Confidence interval for means:  (1.298900072611902, 3.6936840494203573)

E_Estimate(10)
E_Estimate(25)
E_Estimate(100)
E_Estimate(1000)

Standard Error: 0.823128450999
Confidence interval for means:  (1.2599012678994577, 3.6709887664371421)
Standard Error: 0.459961501908
Confidence interval for means:  (1.450269519708927, 2.8526956962910788)
Standard Error: 0.209413856208
Confidence interval for means:  (1.7230399218834027, 2.3854325563894885)
Standard Error: 0.0654525250694
Confidence interval for means:  (1.8999712248658385, 2.1173399393331964)

As the n size goes up, Standard error decreases and the 90% confidence interval difference decreases as well. As n goes up, the shape of the the CDF starts looking like a normal distribution