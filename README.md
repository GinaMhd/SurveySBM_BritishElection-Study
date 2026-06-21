# SurveySBM Analysis of the British Election Study

This repository contains code for applying SurveySBM to selected waves of the British Election Study (BES). The aim of the analysis is to represent survey responses as a bipartite network of respondents and questions, and to use stochastic block modelling to identify groups of respondents and groups of questions with similar response patterns.

The analysis uses three selected BES waves: wave 16, wave 20, and wave 25. A subset of 4,000 respondents and 20 repeated socio-political questions was used. Survey responses were converted into a respondent-question network, where respondents and questions are represented as vertices and valid survey responses are represented as weighted edges. Multiple MCMC runs are performed for each wave to reduce dependence on a single random initialisation. The best run is selected using the lowest model description length.

The notebook also includes code for evaluating model results, including entropy trajectories, pairwise overlap between repeated runs, cross-wave overlap of respondent partitions, and block-level response predictability using Simpson and Shannon entropy scores. These analyses are used to assess the stability of inferred respondent groups, compare partitions across survey waves, and evaluate how predictable responses are within the inferred respondent-question block structure.
