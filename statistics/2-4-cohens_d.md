[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> import thinkstats2  
    import thinkplot  
    import math   

    preg= nsfg.ReadFemPreg()  
    live= preg[preg.outcome == 1]   

    firsts= live[live.birthord == 1]  
    others= live[live.birthord != 1]  

    def CohenEffectSize(group1, group2):  
        diff = group1.mean() - group2.mean()  
        var1= group1.var()  
        var2= group2.var()  
        n1, n2= len(group1),len(group2)  
        pooled_var= (n1 * var1 +n2 * var2)/ (n1+n2)  
        d= diff /math.sqrt(pooled_var)  
        return d

    print(CohenEffectSize(firsts.prglngth,others.prglngth))    
    print(CohenEffectSize(firsts.totalwgt_lb,others.totalwgt_lb))    
    First babies will tend to be lighter than others.    
    Cohen's _d_ for overall weight is -.089 standard deviations, which suggests that there may not be a strong difference in    weight when comparing weights of first-borns vs others.
