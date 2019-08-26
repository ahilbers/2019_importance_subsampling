# 2019_importance_subsampling
Data, model files, example code and supplementary material related to the paper _Importance subsampling: improving power system planning under climate-based uncertainty (2019)_.




## Contains

### Modelling & data files

- `model_files/`: contains all model files for employed PSM in open source model generator `Calliope` (see acknowledgements), version 0.6.4
- `data/`: contains data (demand and weather time series) files
  - `demand_wind.csv`: demand and wind timeseries used in paper
  - `demand_wind_national_grid.csv`: demand and wind timeseries used in supplementary material


### Code

Code for executing the _importance subsampling_ methodology on the PSM used in the paper. Designed to run with `Python 3.6` with `numpy` and `pandas` and `Calliope 0.6.4`. Runs as follows from a unix command line. Note that you need have installed `Calliope` via Anaconda (see [this link](https://calliope.readthedocs.io/en/stable/user/installation.html) for download instruction). The default solver is `cbc` but this can be changed in `model_files/model.yaml`.

    $ conda activate calliope       # start Calliope environment
    (calliope) $ python3 main.py    # run code

A directory `results` is created with all relevant PSM outputs.


### Supplementary material

- `supplementary_material.pdf`: PDF file with results of applying _importance subsampling_ to the `demand_wind_national_grid.csv` timeseries data instead of `demand_wind.csv` as in the original paper





## Contact

Adriaan Hilbers. Department of Mathematics, Imperial College London. aph416@ic.ac.uk.




## Acknowledgements

Models are constructed in the modelling framework `Calliope`, created by Stefan Pfenninger and Bryn Pickering. See [callio.pe](callio.pe) or the following paper for details:

- Pfenninger et al., (2018). Calliope: a multi-scale energy systems modelling framework. Journal of Open Source Software, 3(29), 825, doi:10.21105/joss.00825.

The demand and wind dataset is based on work by Hannah Bloomfield et al. Details can be found in the following papers:

- Bloomfield, H. C., Brayshaw, D. J., Shaffrey, L. C., Coker, P. J. and Thornton, H. E. (2016) Quantifying the increasing sensitivity of power systems to climate variability. Environmental Research Letters, 11 (12). 124025. ISSN 1748­ 9326 doi: 10.1088/1748­9326/11/12/124025

- Cannon, D. J., Brayshaw, D. J., Methven, J., Coker, P. J., & Lenaghan, D. (2015). Using reanalysis data to quantify extreme wind power generation statistics: A 33 year case study in Great Britain. Renewable Energy, 75 , 767 – 778. doi:10.1016/j.renene.2014.10.024

- Drew, D. R., Cannon, D. J., Brayshaw, D. J., Barlow, J. F., & Coker, P. J. (2015). The impact of future offshore wind farms on wind power generation in Great Britain. Resources, 4 , 155–171. doi:10.3390/resources4010155.
