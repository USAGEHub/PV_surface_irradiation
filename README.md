# Description
The tool determines the average irradiation value per roof part.

# Input data requirements

* Segmented roof parts 
* Raster irradiation map 

# Output data requirements

Segmented roof parts with additional attribute:

* stima_kwhm2anno: average yearly irradiation (KWh/m2/year)

# Objective
Providing a rough estimation of the yearly amount of energy that could be collected by PV panels per roof part.

# Use of resource

* Run zonal statistics between the input vector layer ‘Roof parts’ and the raster layer ‘Irradiation’ to calculate the average value of annual solar irradiation in Ferrara
* Run the field calculator, creating a new field of type 'Decimal (double precision)' called ‘stima_kwhm2anno’ valued according to the formula: (stima_kwhm2anno_mean)/1000
* Run the “Delete field” tool to eliminate the 'stima_kwhm2anno_mean' field present in the output of the previous tool

--------------------------------------------------------------------------------------------------------
