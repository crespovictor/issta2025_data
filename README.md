# Results and replication package for the paper "The Role of Road Features and Vehicle Dynamics in Cost-Effective Autonomous Vehicles Testing: Insights from Instance Space Analysis"


## Description of the data and folder structure

This repository contains the results, list of features for each step, and the compiled dataset used for running Instance Space Analysis (ISA).

### Folder Structure

- `list_of_features`: It contains the list of features for each step of the process of running ISA: Before correlation, after correlation analysis, after clustering, and the final list of impactful features. This folder also contains the file `features_ml.csv`, containing the set of features used for training the Machine learning classifiers for the prediction of test case outcome.
- `results`: It contains the results after running ISA. The folder contains the list of most impactful features, a projection matrix of each feature and its Principal Component, figures of the instance space and feature value distributions, coordinates of each test case in the 2D instance space, and the value of each impactful feature for each test case. This folder is further subdivided in `static_features` and `dynamic features`.
- `replication`: This includes the dataset used for running ISA and the file `options.json` which includes the options used for running ISA. These options can be set before running ISA in the application screen.

## Replication

### Pre-requisites

- [Matlab](https://www.mathworks.com/products/matlab.html)
- [libsvm](https://www.csie.ntu.edu.tw/~cjlin/libsvm/)
- [ISA Toolkit](https://github.com/andremun/InstanceSpace)

### Usage


1. After installing the pre-requisites, move the file `metadata.csv` to the folder of ISA Toolkit, usually `[ISA toolkit root folder]/trial`.
2. Modify the options in `example.m` on the ISA Toolkit Matlab application to match those listed in `options.json`
3. Run the ISA Toolkit

### Results

The results will be generated, including the list of features and figures of the instance space and distribution of feature values. Please note that these figures will vary slightly from the ones presented in the folder `resutls` for we used a different graphics generation tookit (Python matplotlib).

Results after running the ISA Toolkit with the dataset provided will have more than those listed under the folder `results`. We encourage you to read through the different descriptions of each file and option on the ISA Toolkit documentation.