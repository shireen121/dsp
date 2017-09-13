[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> Using Downey's CohenEffectSize function (see below), I calculated the Cohen's D effect size to help determine if first babies are lighter or heavier than others. The Cohen D's effect size is -0.089 which is a fairly small difference in means although still more significant than the difference in pregnancy length for first babies vs. others. First babies on average were slightly lighter (7.20 lb) than others (7.33 lbs) but not by a significant amount. 

```python
def CohenEffectSize(group1, group2):
    diff = group1.mean() - group2.mean()
    
    var1 = group1.var()
    var2 = group2.var()
    n1, n2 = len(group1), len(group2)

    pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
    d = diff / np.sqrt(pooled_var)
    return d
    
CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb) 
```

