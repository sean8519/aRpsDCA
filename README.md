# aRpsDCA
### an R package for Arps decline-curve analysis

aRpsDCA provides R implementations of functions for carrying out Arps decline-curve analysis on oil and gas production data.  

aRpsDCA currently implements the following decline-curve types:  
* Exponential  
* Hyperbolic (and harmonic)  
* Hyperbolic with terminal exponential (aka "modified hyperbolic", "hyperbolic-to-exponential")  
* Any of the above with initial rate curtailment  
* Any of the above with initial linear buildup periods  

aRpsDCA provides functions for  
* computing rate, cumulative production, and instantaneous decline over time  
* computing EUR and time to economic limit  
* performing best fits of various decline curve types to actual production data  
* rate, decline, and time unit conversions  

aRpsDCA is released under the LGPL v2.1 and is free for commercial and non-commercial use.  

The current "released" version of aRpsDCA is 1.1.0 and is available from [CRAN](https://cran.r-project.org/package=aRpsDCA).  

Several critical issues have since been corrected; until the official release of aRpsDCA 1.1.1 it is recommended to retrieve the current pre-release version from github using the devtools library:  
```R
install.packages('devtools')
devtools::install_github('derrickturk/aRpsDCA')
```

Release notes:  
v1.0.0 (2014-04-03): initial release  
v1.0.1 (2015-06-21): S3 methods for formatting now correctly print curve family; handling of Np for D = 0 is corrected  
v1.0.2 (2016-01-06): evaluation of hyperbolic-to-exponential declines with Di = Df now handled correctly  
v1.1.0 (2016-04-04): Arps declines with linear initial buildup periods, and fitting to interval-volume data; additional bug fixes for daily data and better initial guesses for decline parameters  
v1.1.1 (2016-xx-xx): EUR for declines with buildup now handled correctly; zero results from arps.q and arps.Np when decline with buildup was passed with only post-buildup time values are now corrected  

(c) 2016 [dwt](http://www.github.com/derrickturk) | [terminus data science, LLC](http://www.terminusdatascience.com)
