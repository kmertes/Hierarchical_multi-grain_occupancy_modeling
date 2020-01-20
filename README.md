# Hierarchical_multi-grain_occupancy_modeling

The characterization of species’ environmental niches - and spatial distribution predictions based on them - are now central to much of ecology and conservation, but implicitly require decisions about the appropriate spatial scale (i.e. grain) of analysis. 

Ecological theory and empirical evidence suggest that range-resident species respond to their environment at two characteristic, hierarchical spatial grains: (i) response grain, the (relatively fine) grain at which an individual uses environmental resources, and (ii) occupancy grain, the (relatively coarse) grain equivalent to a typical home range. 

Here, we present a multi-grain (MG) occupancy model to simultaneously estimate species-environment associations at both grains. 

"OpenBUGS model code" contains code to run an OpenBUGS model that fits hierarchical, multi-grain Bayesian occupancy models to detection and non-detection data. 

The code contains a number of named variables, including: 

1.	sites1km: number of sampling sites at the occupancy grain
2.	sitesxm: number of sampling sites at the use grain
3.	psi: occupancy is either 1 or 0 with probability psi
4.	theta: use is either 1 or 0 with probability theta
5.	p: detection is either 1 or 0 with probability p
6.	Environmental predictor variables
a.	elev: elevation (m)
b.	lcchet: land cover heterogeneity, or the number of land cover classes in a given grid cell
c.	NDVI: Normalized Difference Vegetation Index, a remote sensing index representing vegetation greenness
d.	precip: long-term mean annual precipitation 
e.	dist2water: distance to nearest grid cell classified as water
f.	KTW: remote sensing index representing soil moisture
g.	SCI: index of vegetation structural complexity
h.	prop_grass: proportion of grid cell covered by grass land cover
i.	shrubprop: proportion of grid cell covered by shrub canopies
j.	TAI: mean total annual direct solar radiation intercepted by grid cell
k.	propclosedshrub: proportion of grid cell covered by woody vegetation <2m tall
l.	w (prefix): indicator variable for given environmental predictor variable
