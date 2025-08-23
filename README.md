# Parkinson's Disease Detection Using Voice Analysis

A machine learning project that uses acoustic features from voice recordings to detect Parkinson's disease with high accuracy. This non-invasive approach leverages speech patterns and voice characteristics that are commonly affected in Parkinson's patients.

## What is Parkinson’s disease?
Parkinson’s disease (PD) is a progressive neurodegenerative disorder in which dopamine-producing neurons of a brain structure called the substantia nigra (a part of the brain that contains high number of dopamine-producing neurons), are damaged and die over time, leading to a number of motor problems and mental disabilities1. Substantia nigra is located in a part of the brain (basal ganglia/ basal nucleus) that is responsible for motor control where all the involuntary movements are controlled. In healthy person, this part of the brain is filled with dopamine neurons which play a critical role in brain cell communication. Dopamine neurons produces dopamine to help our body in making normal movements. This disease has affected approximately **7.5 million** people worldwide with 0.3% of the patients is in the population of 40 years old and above2.

![Image Description](https://sdmntprwestus2.oaiusercontent.com/files/00000000-3fac-61f8-a8b6-5c7bbcc602da/raw?se=2025-08-23T17%3A31%3A29Z&sp=r&sv=2024-08-04&sr=b&scid=55f8b69f-d4d9-558c-af19-b9def0b50251&skoid=f71d6506-3cac-498e-b62a-67f9228033a9&sktid=a48cca56-e6da-484e-a814-9c849652bcb3&skt=2025-08-22T20%3A25%3A47Z&ske=2025-08-23T20%3A25%3A47Z&sks=b&skv=2024-08-04&sig=KBHJsOq9hBnxBxgoIJ%2BnuipfuQJeJIWcxaTSWOE1qhM%3D)

## Comparison of dopamine levels in normal vs Parkinson's disease

![Image Description](https://sdmntprwestus2.oaiusercontent.com/files/00000000-f748-61f8-9333-0e73b5b7da48/raw?se=2025-08-23T16%3A47%3A38Z&sp=r&sv=2024-08-04&sr=b&scid=6d646224-b768-5312-b22e-577bad092096&skoid=f71d6506-3cac-498e-b62a-67f9228033a9&sktid=a48cca56-e6da-484e-a814-9c849652bcb3&skt=2025-08-22T20%3A30%3A48Z&ske=2025-08-23T20%3A30%3A48Z&sks=b&skv=2024-08-04&sig=hPvRiUTRbK/9DM9StPQuOPfY5zdHZqHo52zCSvn2zy0%3D)

## Project Overview

Parkinson's disease affects speech and voice production, causing distinctive acoustic changes that can be measured and analyzed. This project implements various machine learning algorithms to classify voice samples as either healthy or indicative of Parkinson's disease.
