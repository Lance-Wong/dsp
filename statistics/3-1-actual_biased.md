[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> resp = nsfg.ReadFemResp()
    under18= thinkstats2.Pmf(resp.numkdhh,label='observed')

    def BiasPmf(pmf,label):
        new_pmf = pmf.Copy(label=label)  
        for x, p, in pmf.Items():  
            new_pmf.Mult(x,x)  
        new_pmf.Normalize()  
        return new_pmf  

    thinkplot.Pmf(under18)  
    thinkplot.Pmf(biased_under18)  

    thinkplot.PrePlot(2)  
    thinkplot.Pmfs([under18,biased_under18])  
    thinkplot.Show(xlabel='Family Size', ylabel='PMF')  

    def mean_pmf(pmf):  
        d=0  
        for key, prob in pmf.Items():  
         d += (key * prob)  
        return d

    mean_pmf(under18)  
    mean_pmf(biased_under18)

    1.02420515504  
    2.40367910066

