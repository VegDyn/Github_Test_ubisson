Reproducibility in github
================

## Git as a metadata creator

In this repo, an analysis will be done and then the results should be
filled in the `Metadata.Rmd` file. This will simulate a sampling
analysis were each one would go out to the field or get data from a
dataset, and each one would do an analysis. Then the GitHub group
administrator, will pull the dataset you created to make an analysis of
the metadata you created.

## Read in the data

``` r
Data <- read.csv("AlroyData.csv")
```

This dataset, has 3,410 sites where the species Richness, Number of
individuals, some derived statistics are also there. In the next table
we can see the fist 20 entries:

| Richness | count | Fishers\_Alpha | Goods\_U | Shannons\_H |
| -------: | ----: | -------------: | -------: | ----------: |
|       55 |   462 |         16.267 |   0.9524 |      3.0522 |
|       69 |   460 |         22.513 |   0.9457 |      3.2839 |
|       79 |   603 |         24.301 |   0.9653 |      3.5530 |
|       90 |   773 |         26.385 |   0.9651 |      3.6363 |
|       59 |   918 |         14.070 |   0.9858 |      3.0444 |
|       24 |   327 |          5.968 |   0.9725 |      1.9781 |
|       37 |   440 |          9.625 |   0.9660 |      2.4573 |
|       50 |   265 |         18.225 |   0.9210 |      2.9796 |
|       34 |   295 |          9.928 |   0.9594 |      2.7015 |
|       30 |   126 |         12.457 |   0.8896 |      2.7975 |
|       25 |   165 |          8.194 |   0.9701 |      2.7007 |
|       27 |   163 |          9.225 |   0.9511 |      2.8537 |
|       26 |   173 |          8.490 |   0.9657 |      2.7701 |
|       29 |   153 |         10.596 |   0.9481 |      2.9745 |
|       26 |   166 |          8.652 |   0.9640 |      2.8155 |
|       32 |   199 |         10.780 |   0.9602 |      2.9705 |
|       29 |   186 |          9.630 |   0.9680 |      2.8610 |
|       31 |   167 |         11.205 |   0.9644 |      3.0762 |
|       30 |   214 |          9.499 |   0.9769 |      2.8855 |
|       84 | 12552 |         12.093 |   0.9990 |      1.7760 |

## Simulation of sampling

Now on the next step each one of you will sample some of those sites, we
will assign the number of sites and which sites you sample at random,
for reproducibility you will choose a set.seed number.

``` r
set.seed(2021)
NumberOfSites <- sample(20:200, 1)
SiteIndex <- sample(x = 1:nrow(Data), NumberOfSites)

MySample <- Data[SiteIndex,]
```

## Graph the data

Add here a graph of your dataset

## Analysis of data

Make a linear model where your independent variable is species richness
and add the results to the Metadata.Rmd, then push your README.MD and
Metadata.Rmd to your github repository
