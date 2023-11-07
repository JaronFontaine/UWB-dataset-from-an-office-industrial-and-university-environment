# UWB-dataset-from-an-office-industrial-and-university-environment

This repository contains open UWB localization datasets, captured in industrial, office and university environments and is published by IDLab - Ghent University - imec. 

Three dataset environments are included: (i) IIoT19+20, (ii) OfficeLab, (iii) University. The first two datasets are captured in-house, at iGent, Zwijnaarde, Belgium [1]. The university dataset was made publicly available by [2] of which we selected a subset of ranges. Please refer to the original author's work when using this dataset.

We present three data files, for each environment: (a) _meta\__ files contain metadata of the UWB test setup and contain the ground truth labels ((N)LOS and UWB ranging error), (b) _features\__ contain extracted features from channel impulse responses (CIRs) and additional meta-features, (c) CIRs available [here](https://cloud.ilabt.imec.be/index.php/s/BMF7mZnt4RTsHCL).

We recommend reading the _meta_ and _features_ .csv data files using [pandas](https://github.com/pandas-dev/pandas), while the CIRs are formatted using the [HDF5](https://github.com/h5py/h5py) binary data format.

More information about the environments, data capture strategy and results can be found in our publication [3].

When using these datasets for future publications, please refer to [3].

I'm happy to answer any questions about this dataset at jaron.fontaine@ugent.be


[1] https://www.ugent.be/ea/idlab/en/research/research-infrastructure

[2] Michael Stocker, Markus Gallacher, Carlo Alberto Boano, and Kay Römer. 2021. Performance of support vector regression in correcting UWB ranging measurements under LOS/NLOS conditions. In Proceedings of the Workshop on Benchmarking Cyber-Physical Systems and Internet of Things (CPS-IoTBench '21). Association for Computing Machinery, New York, NY, USA, 6–11. https://doi.org/10.1145/3458473.3458820

[3] J. Fontaine et al., "Transfer Learning for UWB Error Correction and (N)LOS Classification in Multiple Environments," in IEEE Internet of Things Journal, doi: [10.1109/JIOT.2023.3299319](https://ieeexplore.ieee.org/document/10195942).

