# BAM Landbird Models - Version 4

## A generalized modeling framework for spatially extensive species abundance prediction and population estimation

BAM's landbird models bridge the gap between local studies and large-scale management needs by compiling and harmonizing data from many sources to predict avian abundance at a fine resolution and broad extent.

## Version 4

Version 4 of BAM's landbird models (Stralberg et al. 2025) can be reproduced using the data object stored on Zenodo (DOI [10.5281/zenodo.4018335](https://doi.org/10.5281/zenodo.4018335)) and the generalized model script available in this repository. Please see Version 5 below for additional steps in the modelling and interpretation workflow.

Please note, in late March 2025, we discovered and fixed a bug in the code for calculating QPAD offsets that dated back approximately ten years. The bug was within the code used to adjust time zones and therefore affects QPAD offsets used for

1. [species with time since sunrise in the top model](https://github.com/borealbirds/QPAD-offsets-correction/blob/main/qpad_tssr_species.csv) and
2. in areas outside the mountain time zone.

Since QPAD offsets only adjust the intercept of model estimates, this bug will only affect model outcomes if

1. models were built for density or population estimates per se, or
2. models were compared or integrated across time zones. Relative patterns of density (e.g., habitat coefficients) within time zones should be unaffected.

If you have been affected by this bug, please see the [`QPAD-offsets-correction`](https://github.com/borealbirds/QPAD-offsets-correction) repository for further details or email `bamp@ualberta.ca` for assistance.

Citing v4:

- Stralberg, D., Sólymos, P., Docherty, T. D. S., Crosby, A. D., Van Wilgenburg, S. L., Knight, E. C., Drake, A., Boehm, M. M. A., Haché, S., Leston, L., Toms, J. D., Ball, J. R., Song, S. J., Schmiegelow, F. K. A., Cumming, S. C., Bayne, E. M., 2025. A generalized modeling framework for spatially extensive species abundance prediction and population estimation. _Ecosphere_, in press.
- Sólymos, P., D. Stralberg, and E. C. Knight. 2025. BAM Generalized National Models Documentation, Version 4.0 (Version 4.0) [Data set]. _Zenodo_, DOI [10.5281/zenodo.4018335](https://doi.org/10.5281/zenodo.4018335).


## Version 5

Version 5 of the modelling workflow is currently under active development and is available in [this repository](https://github.com/borealbirds/LandbirdModelsV5).

New developments to BAM's Landbird Models for Version 5 include:

* Expanded study area to include hemi-boreal regions of the continental United States using natural biographic boundaries rather than political boundaries to delineate regions
* Expanded list of environmental covariates including time-matched variables for vegetation biomass, human disturbance, and annual climate
* Acquisition and inclusion of new datsets for data-sparse regions, including appropriate eBird data
* Predictions for five year intervals from 1985 to 2020
* More rigorous model tuning and covariate thinning

## Cite
Stralberg, D., P. Solymos, T.D.S Docherty, A.D. Crosby, S.L. Van Wilgenburg, S. Hache, E.C. Knight, L. Leston, J.D. Toms, J. Ball, S. Song, F. Schmiegelow, S.G. Cumming, and E.M. Bayne. *In Review*. A generalized modeling framework for spatially extensive species abundance prediction and population estimation: an example for landbirds in subarctic Canada. Submitted to Ecosphere.
