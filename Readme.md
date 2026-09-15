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

Run all cells: the notebook works out of the box with a built-in analytical
stratification, so no data download is required. Only **Section 1** needs to be
edited: background stratification, grid, eddy parameters (polarity, Rossby
number, radius, vertical scale and depth), stability thresholds and output paths.

To use your own stratification, set `BACKGROUND["source"] = "netcdf"` and point it
to a file providing a depth axis, a density profile, the Coriolis parameter and
the first baroclinic Rossby radius — or simply overwrite `z`, `rho_s`, `f0` and
`Rd` after Section 2.1.

## Output

`eddy-static-stability.nc` (and a `.csv` summary) contain, for each experiment,
the parameters, the density anomaly at the eddy centre, the resulting `N²`
profile and the instability flag.

## Requirements

Python ≥ 3.10, `numpy`, `scipy`, `matplotlib`, `pandas`; `xarray` + `netcdf4` for
NetCDF input/output. No compiled or external toolbox.

## License
