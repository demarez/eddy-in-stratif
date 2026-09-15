# Static stability of prescribed three-dimensional eddies

Companion notebook to de Marez et al. study.

`Check-static-stability-isolated-eddy.ipynb` prescribes an idealized axisymmetric
eddy from its vorticity structure, computes the density anomaly required for
gradient-wind and hydrostatic balance, adds it to an arbitrary background density
profile, and diagnoses the static stability of the resulting three-dimensional
density field.

## Quick start

```bash
pip install -r requirements.txt
jupyter lab Check-static-stability-isolated-eddy.ipynb
```
## Requirements

Python ≥ 3.10, `numpy`, `scipy`, `matplotlib`, `pandas`; `xarray` + `netcdf4` for
NetCDF input/output. No compiled or external toolbox.

