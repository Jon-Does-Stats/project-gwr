## Primary project objective
- This project serves as an introduction to Geographically Weighted Regression and illustrates a straightforward application of the method.

- Geographically Weighted Regression (GWR) is an exploratory data analysis technique for investigating nonstationary relationships in spatial data using regression analysis. GWR adds a level of modeling sophistication to ordinary least squares regression (OLS) by moving a weighted window over the data, estimating a set of coefﬁcient values at every chosen ‘ﬁt’ point. The ﬁt points can be at observed locations, but do not have to be. If the local coefﬁcients vary in space, it can be taken as an indication of non-stationarity.

## Primary languages
- R

## Highlighted visualizations

- (below) OLS residuals exhibit obvious spatial patterning. A possible explanation is that the standard OLS regression model is too inflexible to capture local variation in the relationships between the response and predictors.

<img src="https://raw.githubusercontent.com/Jon-Does-Stats/project-gwr/main/figures/spatial_residuals_ols.png" width=675>

- (below) A potential problem in the application of GWR with fixed bandwidth kernels is that for some regression points, where data are sparse, the local models
might be calibrated on very few data points, giving rise to parameter estimates with large standard errors. To mitigate this, the spatial kernels in GWR can be made to adapt themselves in size to variations in the density of the data so that the kernels have larger bandwidths where the data are sparse and have smaller bandwidths where the data are plentiful. This plot demonstrates the adaptive kernel bandwidth selection algorithm of GWR.  The algorithm ﬁnds an optimal bandwidth for a given geographically weighted regression model by optimizing its root mean square prediction error using leave-one-out cross-validation (LOOCV). The result is a proportion between 0 and 1 of observations to include in the weighting scheme for each local regression equation. 

<img src="https://raw.githubusercontent.com/Jon-Does-Stats/project-gwr/main/figures/adaptive_bandwidth.png" width=675>

- (below) Regression coefficients associating building code violations with African American composition, now able to vary spatially. Darker regions indicate areas where the relationship between the percentage of black residents and building code violations is more strongly positive.

<img src="https://raw.githubusercontent.com/Jon-Does-Stats/project-gwr/main/figures/spatial_coeff_black.png" width=675>

- (below) Regression coefficients associating building code violations with older home composition, now able to vary spatially. Darker regions indicate areas where the relationship between the percentage of older housing units and building code violations is more strongly positive.  Only in the darkest green areal units is there a positive relationship between older home composition and building code violations.

<img src="https://raw.githubusercontent.com/Jon-Does-Stats/project-gwr/main/figures/spatial_coeff_oldhomes.png" width=675>

- (below) Regression coefficients associating building code violations with vacant home composition, now able to vary spatially. Darker regions indicate areas where the relationship between the percentage of vacant housing units and building code violations is more strongly positive. Vacant housing composition almost universally increases building code violations in the region.

<img src="https://raw.githubusercontent.com/Jon-Does-Stats/project-gwr/main/figures/spatial_coeff_vacancy.png" width=675>

- (below) Residuals from the GWR model show much less spatial distinction (e.g., appear more random) than the residuals from the OLS model. The GWR residuals are also less extreme. Provides evidence that the effect of some predictor variables is non-stationary, or exhibits spatial variation and spatial patterning.

<img src="https://raw.githubusercontent.com/Jon-Does-Stats/project-gwr/main/figures/spatial_residuals_gwr.png" width=675>
