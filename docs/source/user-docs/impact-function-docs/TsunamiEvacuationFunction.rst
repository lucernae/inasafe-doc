Tsunami Evacuation Function
===========================

Overview
--------

**Unique Identifier**: 
Tsunami Evacuation Function

**Author**: 
AIFDR

**Rating**: 
4

**Title**: 
Need evacuation

**Synopsis**: 
To assess the impacts of tsunami inundation in raster format on population.

**Actions**: 
Provide details about how many people would likely need to be evacuated, where they are located and what resources would be required to support them.

**Hazard Input**: 
A hazard raster layer where each cell represents tsunami depth (in meters).

**Exposure Input**: 
An exposure raster layer where each cell represent population count.

**Output**: 
Raster layer contains population affected and the minimum needs based on the population affected.

**Limitation**: 
The default threshold of 0.7 meter was selected based on consensus, not hard evidence.

Details
-------

The population subject to inundation exceeding a threshold (default 0.7m) is calculated and returned as a raster layer. In addition the total number and the required needs in terms of the BNPB (Perka 7) are reported. The threshold can be changed and even contain multiple numbers in which case evacuation and needs are calculated using the largest number with population breakdowns provided for the smaller numbers. The population raster is resampled to the resolution of the hazard raster and is rescaled so that the resampled population counts reflect estimates of population count per resampled cell. The resulting impact layer has the same resolution and reflects population count per cell which are affected by inundation.

Doc String
----------

Impact function for tsunami evacuation.

    :author AIFDR
    :rating 4
    :param requires category=='hazard' and                     subcategory=='tsunami' and                     layertype=='raster' and                     unit=='m'

    :param requires category=='exposure' and                     subcategory=='population' and                     layertype=='raster'
    