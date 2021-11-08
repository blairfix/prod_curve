# prod_curve

`prod_curve` is an R function for calculating monthly production curves for individual oil wells using data that is typically reported by the oil industry.


### Inputs

`prod_curve` accepts the following vectors of production data

* `well_id`: numbered ID's for individual wells
* `prod_first_6`: cumulative production during the well's first 6 months
* `prod_first_12`: cumulative production during the well's first 12 months
* `prod_first_24`: cumulative production during the well's first 24 months
* `prod_first_60`: cumulative production during the well's first 60 months
* `prod_last_year`: total production during the well's last recorded year
* `prod_daily_last_year`: average daily production during the well's last recorded year
* `prod_cumulative`: total cumulative production
* `prod_peak_daily`: peak daily production
* `date_start`: start date of the well's records. *Must be in decimal form*: 2012-03-01 = 2012.16
*  `date_end`: end date of the well's records. *Must be in decimal form*: 2012-03-01 = 2012.16
date_end
* `peak_month`: month number of peak production. Example: if well peaked 20 months after the start of production, `peak_month=20`
* `decline_3`: the percentage decline in production 3 months after peak production
* `decline_12`: the percentage decline in production 3 months after peak production
* `decline_24`: the percentage decline in production 3 months after peak production
* `decline_60`: the percentage decline in production 3 months after peak production

For an example of this type of production data, see this github repo: <https://github.com/magerton/drillinginfo-data-import>


### Output

`prod_curve` returns a list with estimated monthly production data for each well.

* `well_id`: a vector of well IDS
* `production`: a vector of production months for each well
* `cumulative_production` a vector of cumulative production for each well



### Installation

To use `prod_curve`, install the following R packages:

* [Rcpp](https://cran.r-project.org/web/packages/Rcpp/index.html) 
* [RcppArmadillo](https://cran.r-project.org/web/packages/RcppArmadillo/index.html)
* [BH](https://cran.r-project.org/web/packages/BH/index.html)

Put the source code (`prod_curv.cpp`) in the directory of your R script. Then source it with the command `sourceCpp('prod_curv.cpp')`.








