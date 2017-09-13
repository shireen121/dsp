[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>>In this exercise we demonstrate the bias that exists depending on who you survey to extract observations. To demonstrate this, we will look at how many children are in a household and compare observations from the NSFG respondents to observations from hypothetically asking each child how many kids are in their family. The graphical results and means of the two surveys are below showing how the biased results will make it seem as if a larger number of families have a larger number of kids than in actuality.See below for the code, graph and mean calculations.

```Python
# Graph actual and observed results
pmf = thinkstats2.Pmf(resp.numkdhh, label='numkdhh')
biased_pmf = BiasPmf(pmf, label='observed')

thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, biased_pmf])
thinkplot.Config(xlabel='Number of Kids', ylabel='PMF')
```

![graph](https://github.com/shireen121/dsp/blob/master/img/Actual_vs_Bias_Graph.png)

```python
#calculate actual and observed means
print('Actual mean', pmf.Mean())
print('Observed mean', biased_pmf.Mean())
```

>>Actual mean 1.02420515504  
>>Observed mean 2.40367910066  
 
