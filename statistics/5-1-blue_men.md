[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>>In this problem, given the height distribution of men, we are trying to determine the percentage of males that fall into the height requirements to be in the Blue Man Group. There are approximately 34% of men that are in this range. I calculated this by evaluating the position of the min and max height along the CDF for the height distribution for men. The code and results are below.

```python
# Convert from feet/inches to cm
height_cm_min = (5*12 + 10) * 2.54
height_cm_max = (6*12 + 1) * 2.54

#Determine CDF at given min and max values to calculate range
min_percentile = scipy.stats.norm.cdf(height_cm_min, loc = mu, scale = 7.7)
max_percentile = scipy.stats.norm.cdf(height_cm_max, loc = mu, scale = 7.7)

#Results
print('Min ', min_percentile)
print('Max ', max_percentile)
print('Range ', max_percentile - min_percentile)
```
>>Min  0.489639027865  
>>Max  0.832385865496  
>>Range  0.342746837631  
