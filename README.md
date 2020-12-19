# Social Connectedness and COVID-19 Spread

#### Project Status: [Completed]

## Table of Contents 
1) Project Obective & Description
2) Methods Used
3) Technologies
4) Background and Motivation
5) Data Exploration
6) Hypothesis Testing
7) Conclusions and Next Steps



## Project Objective
I explored the relationship between social connectedness and COVID-19 spread. 

### Hypothesis: 
U.S. counties with greater social connectedness have higher rates of COVID-19 spread. 

### Methods Used
    - Exploratory Data Analysis
    - Network Analysis
    - Geospacial Information Systems
    - Hypothesis Testing


### Technologies 
    - Python
    - NetworkX
    - GeoPandas
    - SciPy
    - NumPy
    - Matplotlib
    - Plotly
    - Pandas

## Background and Motivation
I was curious about whether any relationship exists between county social connectedness and rates of COVID-19 spread. I'm particularly interested in social network analysis, and wanted to layer in COVID-19 spread to better understand if more socially connected counties have higher cases of COVID-19 per capita.

## Data Exploration
I used the Social Connectedness Indicator dataset from Facebook which contains county<>county connections along with a relative probability of an individual from those two counties being connected on Facebook, the Social Connectedness Indicator (SCI). Since the SCI ranges from 1 to 1 billion, I took the log transformation of the SCI to better enable visualizations.

Figure 1: Distribution of log SCI
![](images/0_log_SCI_distribution.png "Distribution of log Social Connectedness Indicator")

To better understand this SCI dataset, I modeled each county-county pair across the United States, and used two contrasting examples to illustrate the difference in how one county's scores are different from another.

Figure 2 illustrates the Facebook connections to individuals living in San Francisco County. Quite noticeable is the density of connections in urban areas in the West including Seattle and Denver, Austin, Texas, Miami, and throughout the Northeast.

Figure 2: County-County Connections to San Francisco County, California
![](images/1_SF_county_SCI_map.png "Counties Connected to San Francisco County, CA")


The difference is notable when compared to Figure 3, which illustrates the county connections to individuals living in Kern County, California, a more rural area than San Francisco County. Here, individuals in Kern County are more likely to be connected to people living in the West including Nevada, western Texas, across the Great Plains, and the Southeast.

Figure 3: County-County Connections to Kern County, California
![](images/2_Kern_county_SCI_map.png "Counties Connected to Kern County, CA")

Taking the SCI dataset, I layered on a dataset of COVID-19 cases per capita and plotted network maps to illustrate the degree of COVID-19 across these county pairs. Figure 4 illustrates a sample of these connections, with each node scaled for the number of COVID-19 cases per capita. For the purposes of this project, I expected counties in this group to exhibit fewer COVID-19 cases per capita than a random sample drawn from the upper 25% group, Figure 5.

Figure 4: Lower 25% of SCI counties, with nodes sized for COVID-19 cases per capita
![](images/3_network_map_lower_25.png "Random Sample of 2000 Counties from Lower 25%")

Interestingly, the average number of cases per capita in the upper 25% sample was fewer than the sample from the lower 25%. To dig into this more, I ran a hypothesis test.

Figure 5: Upper 25% of SCI counties, with nodes sized for COVID-19 cases per capita
![](images/5_network_map_upper_25.png "Random Sample of 2000 Counties from Upper 25%")

## Hypothesis Testing
I ran a two sample one-sided test that compared a sample from the lower 25% to the higher 25%. I hypothesized that counties with 


## Conclusion and Next Steps


## Contact
anthonyschultz@gmail.com