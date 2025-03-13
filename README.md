# UWB-dataset-from-an-office-industrial-and-university-environment

## --- Update 2025 ---
The CIR link below has been updated with a new version (V2), which fixes the mis-alignment of IIoT19 samples and also includes seperate University CIRs corresponding to the features selected of three environments (hw, 1_hw, esl). The full university corresponds to the full University meta file. In addition, all data is ensured to be de-normalized, which was not the case before for the IIoT19, OfficeLab & University dataset.

## 

This repository contains open UWB localization datasets, captured in industrial, office and university environments and is published by IDLab - Ghent University - imec. 

Three dataset environments are included: (i) IIoT19+20, (ii) OfficeLab, (iii) University. The first two datasets are captured in-house, at iGent, Zwijnaarde, Belgium [1]. The university dataset was made publicly available by [2] of which we selected a subset of ranges. Please refer to the original author's work when using this dataset.

We present three data files, for each environment: (a) _meta\__ files contain metadata of the UWB test setup and contain the ground truth labels ((N)LOS and UWB ranging error), (b) _features\__ contain extracted features from channel impulse responses (CIRs) and additional meta-features, (c) CIRs available [here](https://cloud.ilabt.imec.be/index.php/s/GPSecAzrjSqPK8j).

We recommend reading the _meta_ and _features_ .csv data files using [pandas](https://github.com/pandas-dev/pandas), while the CIRs are formatted using the [HDF5](https://github.com/h5py/h5py) binary data format.

## Example reading the CIR HDF5 file

```python
with h5py.File("CIRsV2.hdf5", "r") as data_file:
    # Load datasets into numpy arrays
    X_IIoT19 = np.array(data_file["IIoT19"]).astype(np.complex128)
    X_IIoT20 = np.array(data_file["IIoT20"]).astype(np.complex128)
    X_OfficeLab = np.array(data_file["OfficeLab"]).astype(np.complex128)
    X_University_full = np.array(data_file["University_full"]).astype(np.complex128)
    X_University_hw = np.array(data_file["University_hw"]).astype(np.complex128)
    X_University_1_hw = np.array(data_file["University_1_hw"]).astype(np.complex128)
    X_University_esl = np.array(data_file["University_esl"]).astype(np.complex128) 
```

## 

More information about the environments, data capture strategy and results can be found in our publication [3].

When using these datasets for future publications, please refer to [3].

I'm happy to answer any questions about this dataset at jaron.fontaine@ugent.be


[1] https://www.ugent.be/ea/idlab/en/research/research-infrastructure

[2] Michael Stocker, Markus Gallacher, Carlo Alberto Boano, and Kay Römer. 2021. Performance of support vector regression in correcting UWB ranging measurements under LOS/NLOS conditions. In Proceedings of the Workshop on Benchmarking Cyber-Physical Systems and Internet of Things (CPS-IoTBench '21). Association for Computing Machinery, New York, NY, USA, 6–11. https://doi.org/10.1145/3458473.3458820

[3] J. Fontaine et al., "Transfer Learning for UWB Error Correction and (N)LOS Classification in Multiple Environments," in IEEE Internet of Things Journal, doi: [10.1109/JIOT.2023.3299319](https://ieeexplore.ieee.org/document/10195942).

