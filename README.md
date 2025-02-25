# Description
The tool determines the average irradiation value for each suitable surface (roof parts, parking lots, etc).

# Input data requirements

* Suitable surfaces (such as segmented roof parts, parking lots, etc
* Raster irradiation map 

# Output data requirements

Suitable surfaces dataset with additional attribute:

* stima_kwhm2anno: average yearly irradiation (KWh/m2/year)

# Objective
Providing a rough estimation of the yearly amount of energy that could be collected by PV panels per surface.

# Use of resource

* Run zonal statistics between the input vector layer ‘Suitable surfaces’ and the raster layer ‘Irradiation’ to calculate the average value of annual solar irradiation in Ferrara
* Run the field calculator, creating a new field of type 'Decimal (double precision)' called ‘stima_kwhm2anno’ valued according to the formula: (stima_kwhm2anno_mean)/1000
* Run the “Delete field” tool to eliminate the 'stima_kwhm2anno_mean' field present in the output of the previous tool

--------------------------------------------------------------------------------------------------------
