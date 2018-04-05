[Think Stats Chapter 7 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2008.html#toc70) (weight vs. age)

>> import first

live, firsts, others = first.MakeFrames()
live = live.dropna(subset=['agepreg', 'totalwgt_lb'])

age, weight= live.agepreg, live.totalwgt_lb
thinkplot.Scatter(age, weight, alpha=.1)
thinkplot.Show(xlabel='Age (years)',
             ylabel= 'Weight (lbs)')

bins = np.arange(10, 45, 5)
indices= np.digitize(age, bins)
groups = live.groupby(indices)

ages=[group.agepreg.mean() for i, group in groups]
cdfs= [thinkstats2.Cdf(group.totalwgt_lb) for i, group in groups]

for percent in [75,50,25]:
    weights = [cdf.Percentile(percent) for cdf in cdfs]
    label= '%dth'% percent
    thinkplot.Plot(ages, weights, label=label)

Corr(age, weight)
'0.068833970354109097'

SpearmanCorr(age, weight)
'0.094610041096582262'

based off the two correlation numbers, I would say that there is a very low correlation between a mother's age and the weight of her newborn.
