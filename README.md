# Exoplanet Atmospheres

This repository contains tutorials to model exoplanet atmospheres using publicly available data, models, and tools. Each tutorial is intended to run as [Google Colab Jupyter Notebooks](https://colab.research.google.com/) so users *do not* need to install Python or any associated packages on their own computers! All that is required is a free Google account.

To run a tutorial, click on the link above, then click the *Open in Colab* button at the top of the notebook and follow along with the instructions. The two currently available tutorials are *Exoplanet Archive Atmospheric Forward Model Fitting* and *Exoplanet Archive Atmospheric Retrieval with PLATON*. Both codes interface with [Transmission Spectroscopy](https://exoplanetarchive.ipac.caltech.edu/cgi-bin/TblView/nph-tblView?app=ExoTbls&config=transitspec) and [Planetary Systems Composite Data](https://exoplanetarchive.ipac.caltech.edu/cgi-bin/TblView/nph-tblView?app=ExoTbls&config=PSCompPars) from the [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu).

### Notes

The forward model fitting tutorial uses the ATMO models from [Goyal, J. M. et al., 2019](https://ui.adsabs.harvard.edu/abs/2019MNRAS.482.4503G/abstract). The ATMO grid is a set of pre-computed physically/chemically self-consistent (forward) models. The tutorial compares spectrophotometry to this model grid and identifies the top three models that most closely match the data using a process similar to chi-squared minimization. This process is very quick and can give a general sense of atmospheric properties.

The retrieval tutorial uses the open source [PLATON](https://github.com/ideasrule/platon) code as described by [Zhang, M. et al., 2019](https://ui.adsabs.harvard.edu/abs/2019PASP..131c4501Z/abstract) and [Zhang, M. et al., 2020](https://ui.adsabs.harvard.edu/abs/2020ApJ...899...27Z/abstract), and is adapted from [this example](https://github.com/ideasrule/platon/blob/master/examples/retrieve_emcee.py) to work with data from the Exoplanet Archive. Atmospheric retrieval codes attempt to estimate atmospheric parameters (and uncertainties) from parametric atmosphere models, typically using statistical inference algorithms. Due to the statistical inference, and depending on how many atmospheric parameters are being considered, retrievals can be very slow. PLATON is not necessarily the most accurate retrieval code, but it is optimized to minimize computational time, and it is very simple to install.

### Retrieval Codes

This is a list of currently available open source atmospheric retrieval codes. (Out of date as of 2024!)

Code | Paper(s)
---- | --------
[CHIMERA](https://github.com/mrline/CHIMERA) | [Line, M. R. et al., 2013](https://ui.adsabs.harvard.edu/abs/2013ApJ...775..137L/abstract)
[TauREx](https://github.com/ucl-exoplanets/TauREx_public) | [Waldmann, I. P. et al., 2015a](https://ui.adsabs.harvard.edu/abs/2015ApJ...802..107W/abstract), [Waldmann, I. P. et al., 2015b](https://ui.adsabs.harvard.edu/abs/2015ApJ...813...13W/abstract)
[BART](https://github.com/exosports/BART) | [Cubillos, P. E., 2016](https://ui.adsabs.harvard.edu/abs/2016arXiv160401320C/abstract), [Harrington, J. et al., 2021](https://ui.adsabs.harvard.edu/abs/2021arXiv210412522H/abstract), [Cubillos, P. E. et al. 2021](https://ui.adsabs.harvard.edu/abs/2021arXiv210412524C/abstract), [Blecic, J. et al., 2021](https://ui.adsabs.harvard.edu/abs/2021arXiv210412525B/abstract)
[PLATON](https://github.com/ideasrule/platon) | [Zhang, M. et al., 2019](https://ui.adsabs.harvard.edu/abs/2019PASP..131c4501Z/abstract), [Zhang, M. et al., 2020](https://ui.adsabs.harvard.edu/abs/2020ApJ...899...27Z/abstract)
[petitRADTRANS](https://gitlab.com/mauricemolli/petitRADTRANS) | [Mollière, P. et al., 2019](https://ui.adsabs.harvard.edu/abs/2019A%26A...627A..67M/abstract)
[Helios-r2](https://github.com/exoclime/Helios-r2) | [Kitzmann, D. et al., 2020](https://ui.adsabs.harvard.edu/abs/2020ApJ...890..174K/abstract)
[Pyrat Bay](https://github.com/pcubillos/pyratbay) | [Cubillos, P. E. & Blecic, J., 2021](https://ui.adsabs.harvard.edu/abs/2021arXiv210505598C)
