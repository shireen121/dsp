[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>>In this problem, we generate 1,000 random numbers between 0 and 1 using the numpy random number generator and plot the results as a PMF and a CDF. These show that the sample is a uniform distribution, although the PMF seems to have a few holes it is simply because the PMF is graphing every unique value as a separate line and would have been impossible for every number between 0 and 1 to result in a sample. The CDF more clearly shows that it is a uniform distribution.

>>
```python 
# Generate 1000 random numbers
random_nums = np.random.random(1000)

# Plot as PMF
pmf = thinkstats2.Pmf(random_nums, label='first')
thinkplot.Pmf(pmf, linewidth=0.1)
thinkplot.Show(xlabel='random num', ylabel='PMF')
```
![pmf](https://github.com/shireen121/dsp/blob/master/img/pmf.png)
>>
```python
# Plot as CDF
cdf = thinkstats2.Cdf(random_nums, label='random_num')
thinkplot.Cdf(cdf)
thinkplot.Config(xlabel='random num', ylabel='CDF', loc='upper left')
```

![cdf](https://github.com/shireen121/dsp/blob/master/img/cdf.png)
