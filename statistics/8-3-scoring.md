[Think Stats Chapter 8 Exercise 3](http://greenteapress.com/thinkstats2/html/thinkstats2009.html#toc77)

---

>> def SimulateGame(lam):
    goals = 0
    t = 0
    while True:
        time_between_goals = random.expovariate(lam)
        t += time_between_goals
        if t > 1:
            break
        goals += 1

    L = goals
    return L

SimulateGame(10)
14

def Estimator(lam,m=1000):
    estimates = []
    for _ in range(m):
        estimates.append(SimulateGame(lam))
    print("Standard Error:",RMSE(estimates,lam))
    print("Mean Error:", MeanError(estimates, lam))    
    
    
Estimator(4) 
Standard Error: 2.06905775656
Mean Error: 0.075

As m gets larger and larger the mean error decreases. I would say this is an unbiased way of estimating


---