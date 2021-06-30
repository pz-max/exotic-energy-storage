# Beyond cost reduction: Improving the value of energy storage

## Abstract
An energy storage technology is valuable if it makes energy systems cheaper. Traditional ways to improve storage technologies are to reduce their costs; however, the cheapest energy storage is not always the most valuable in energy systems.
This paper reviews techno-economic storage valuation methods and expands them by the new ‘market potential method’ which derives a system-value by examining the capacities obtained from a long-term investment planning optimisation. We apply and compare this method to other cost metrics in a renewables-based European power system model, covering diverse energy storage technologies.
We find that characteristics of high-cost hydrogen storage can be equally or even more valuable than low-cost hydrogen storage. Additionally, we show that modifying the freedom of storage sizing and component interactions can make the energy system 10\% cheaper and impact the value of technologies.
The results suggest to look beyond the pure cost reduction paradigm and focus on developing technologies with value approaches that can lead to cheaper electricity systems in future. One practical and useful value method to guide energy storage innovation could be the 'market potential method'.

## This GitHub repo includes:
- PyPSA-Eur model and its required code and data adjustments to reproduce the results
- Jupyter notebook with plotting and analysis scripts

### PyPSA-Eur model to reproduce the results
The workflow to reproduce is the following:
1. Choose one scenario to model (fix-ratio, var-ratio, H2-Hub)
2. Copy the code and data adjustments files for the respective scenario (see folder *PyPSA-adjustments-for-scenarios*) 
3. Replace the equally named files in PyPSA (see folder: *PyPSA-eur-branch*)
4. Let the model run (Instruction can be found [HERE](https://pypsa-eur.readthedocs.io/en/latest/)) 
5. The result will be a data file (.nc) containing the European energy data for instance "elec_s_181_ec_lv1.25_Co2L0.0-1H-EQ0.8c.nc"

### Jupyter notebook with plotting and analysis scripts
The original European networks files used for this study can be found in [Zenodo](http://doi.org/10.5281/zenodo.4421538). 
These datafiles can be processed with the Jupyter notebook scripts provided in folder *Jupyter-plotting-and-analysis-scripts*.
The workflow is the following:
1. Open the Jupyter script
2. Change the following code element:
```
From 
n = pypsa.Network("C:/Users/Max/OneDrive/Fix-ratio_elec_s_181_ec_lv1.25_Co2L0.0-1H-EQ0.8c.nc")
to 
n =  = pypsa.Network("YOUR_DIRECTORY/THE_RELEVANT_SCENARIO_NC_FILE.nc")
```
