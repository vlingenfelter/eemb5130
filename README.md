# Measuring the effects of statistical downscaling on climate change induced plant-pollinator plant extinction and network co-extinction rates

The project proposal for this work is below: 

## Introduction and Background

Understanding how climate change will affect ecological networks is of interest to both climate scientists and ecologists alike. Predictions have been shown to be a useful tool in estimating ecological extinction due to climate change. Extinction of one species in a network can cause destabilization of the entire network, making it further vulnerable to future extinctions and perturbations. Climate envelope models are common practice in ecological modeling to predict species distributions under past and future climate scenarios, and they typically rely on granular climate data, both for calibrating the model with current species distributions and for predictive output.

## Questions and Goals

I will test the effects of two different downscaling methods on the same climate envelope model for the same plant-pollinator network. The overall goal is to determine whether different downscaling methods contribute enough variation to predictive ecological models to warrant further investigation at a larger scale. Future work will hopefully involve evaluation of more statistical downscaling methods with more plant-pollinator networks, following the same methodology described below.

## Methodological Approach

I will first create my two climate datasets, with which I will calibrate my climate envelope model. I will downscale CMIP6 climate data using two common statistical downscaling methods: the statistical downscaling model (SDSM) and bias-correction and spatial disaggregation (BCSD) approach used by WorldClim. For this project I will focus on these downscaling methods both for computational ease and because these are well-understood and widely used approaches for climate model downscaling.

Then I will create my species distributions dataset, following the work done by J. Bascompte. I will use one plant-pollinator network from the Mediterranean region, M_PL_016, from the Web of Life database. I will create a simple species distribution presence spatial dataset for each plant in the network using data from GBIF and Anthos. I will use the  sre  function of the  biomod2  package in R to create an absence/presence dataset for each plant species in the network. I will use the consensus method with six distribution models found in  biomod2: generalized linear model, generalized boosting model, artificial neural network, random forest, and Maxtent. I will run 10 repetitions of each model. I will then project each species’ occurrence probabilities under current and future climate scenarios.

I will simulate plant species extinction by linking it to the probability of occurrence given current and future climate at its network location. I will end up with a likelihood of extinction for each plant species for each timestep for each downscaling technique. I will also measure network connectance, and simulate co-extinction of pollinators. My final dataset will be the connectance of the network, the number of extinct species, and the number of co-extinguished species at each timestamp for each downscaling method, which I will compare statistically.

## Expected Results and Implications

I expect to find significant differences in ecological results between the two downscaling methods. Previous studies have shown that different downscaling methods applied to the same global climate model can introduce as much variation in individual species distribution model results as using entirely different global climate models. It would logically follow that we can expect significant variation in predictions for networks as well.

High resolution, granular climate data is integral to useful species distribution models. Downscaling is therefore an essential step in climate envelope models for ecological prediction. Understanding how downscaling methods affect extinction probabilities will help in efforts to quantify uncertainty in climate envelope models for species distribution. It is important to know how much uncertainty each step in a modelling process adds, and it is well known that downscaling methods can generate different results.