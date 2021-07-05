# Surfs_up
Analysis of weather of Oahu, to open a business using jupyter notebook and SQLite
---

## Overview

We want to open a surfboard and ice cream shop in Oahu and to get investors to back up this project, we are putting together a business plan that will include an analysis of the weather dataset of the island.

## Results

This data analysis gives us a summary of different statistics for the temperature in the months of June and December in the island of Oahu.

### For June: 
- Total number of data: 1700
- Maximum Temperature: 85
- Minimum Temperature: 64
- Average Temperature: 74

We can see more information here: 

![June_temps](https://user-images.githubusercontent.com/78781719/124515731-c470c800-dda5-11eb-9758-25c60de16e93.PNG)

### For December: 
- Total number of data: 1517
- Maximum Temperature: 83
- Minimum Temperature: 56
- Average Temperature: 71

We can see more information here: 

![Dec_temps](https://user-images.githubusercontent.com/78781719/124515828-ff72fb80-dda5-11eb-9b40-f57ccdd06a39.PNG)




## Summary

Looking at both tables, we can conclude that there is not much difference in temperatures from summer and winter at the island, there is just a slightly decrease of degrees but it won't affect the tourism, with that we can have confidence that there won’t be much decrease in sales on winter.

If we would like to provide a visual report of this analysis, it is convenient to convert this to a dataframe using pandas.
Convert to DataFrame : 
```
df = pd.DataFrame(results, columns=['tobs'])
and create a Histogram to visualize: 
df.plot.hist(bins=12)
plt.tight_layout()
```
As extra analysis, it would be convenient to find what wat the minimum, maximum and average temperature of each month with the following query:  
```
min_max_avg = session.query(func.min(Measurement.tobs), func.max(Measurement.tobs), func.avg(Measurement.tobs))
```

