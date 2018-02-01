# SDV - Clone Project of the MIT Synthetic Data Vault for AFMS Analytics

Original Paper
https://hdi-dai.lids.mit.edu/projects/synthetic-data-vault/
Borrowed Python Code
https://github.com/ewvanwinkle/SyntheticDataVault


![SDV](images/SDVlogo.png?raw=true "SDV")

## Introduction

Increasingly, the MHS is generating large amounts of valuable data related to the care of our beneficiaries, but are unable to use this data to its full potential due to privacy-related considerations. The Synthetic Data Vault enables ours to sidestep data-sharing concerns and expand the pool of possible problem participants by generating synthetic data. By learning a generative model that accounts for dependence and relationships, the SDV creates new data that resembles the original set statistically, formally, and structurally—and therefore is easily used in its place. 

It is an end-to-end system that models and synthesizes data automatically such that the synthetic data is virtually indistinguishable from the original. The organization can then store the original privacy restricted data internally, and only allow employees with special clearance to view this sensitive data. The synthetic data, however, can be widely spread. The team can share it freely with others, use it to run predictive analytics, or display it for training purposes openly.

## Goals

* Generalizability: The SDV should be able to work on all relational databases without any modifications. It should automate as much of the modeling and synthesizing as possible.

* Usability: The SDV should expose a simple API that allows users to specify an input and then perform synthesis to their specification. It should be able to synthesize data for individual cells, columns, tables, or the entire database.

* Accuracy: The SDV should synthesize output that can realistically replace the original data. This will require us to formulate metrics to measure differences between the synthesized data and the original data.

## Workflow

![Workflow](images/workflow.PNG?raw=true "workflow")

The user collects and formats the data, specifies the structure and data types, runs the modeling system, and then uses the learned model
to synthesize new data.