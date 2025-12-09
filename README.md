# Transfer Learning for Developing Ground-Motion Models: Application to Iran Using NGA-West2 Data


## Table of Contents

+ [Overview](#overview)
+ [Abstract](#abstract)
+ [Install the requirements](#install)
+ [Citation](#citation)


## Overview
This folder contains the saved trained ML models for the paper. The showcase code is provided to as a sample of how to load the saved model and to create the tranfer-learning-based model. Also some examples are provided to show how to plot the distance scaling and response spectra.

## Abstract <a name = "abstract"></a>
Ground‐motion estimation in regions with limited strong‐motion data remains a major challenge in seismic‐hazard analysis in seismic hazard analysis.  Iran, located in an active tectonic region, has relatively sparse high-quality recordings compared to well-instrumented regions such as California or Japan. In this study, we develop a suite of artificial-neural-network-based (ANN) ground-motion models (GMMs) for Iran using transfer learning from models trained on the NGA-West2 database.  We use an ANN with three predictor variables: moment magnitude (M), Joyner–Boore distance (RJB), and time-averaged shear-wave velocity at 30 m (VS30).  The model predicts 13 intensity-measure spectral ordinates, including PGA and pseudo-spectral acceleration (PSA) from 0.05 to 3 s. The main ANN is trained on 14,518 NGA-West2 records, and its learned parameters (source-scaling and distance-attenuation behavior) are transferred to an Iran-specific ANN using 688 Iranian recordings.  During transfer, the first hidden layer is frozen to preserve the learned low-level relationships, whereas the second hidden layer is set to be trained using the Iranian records to learn the regional characteristics of Iran’s seismotectonic environment.
Results show that the trained ANN using the NGA-West2 dataset reproduces the general trends of NGA-West2 GMMs, and the transfer-learning ANN closely matches the Iranian GMMs for both PGA and spectral ordinates.  The transfer-learning model results in lower residual bias than direct Iran-only training, particularly for M > 6 and distances less than 10 km.  This demonstrates that transfer learning is an effective and powerful framework for building regional GMMs when data are sparse.

## Install the requirements <a name = "install"></a>
* Python 3.9 and higher is required
* Create a virtual environment: conda create -n <env_name> python=3.9.13
* Activate the virtual environment: conda activate <env_name>
* Intall all dependencies using pip, run the command: pip install -r requirements.txt
```ShellSession
$ conda deactivate
$ conda create -n GMM python=3.9.13 anaconda
$ conda activate GMM
```
Then, install the requirements:
```ShellSession
$ pip install -r requirements.txt
```

## Citation <a name = "citation"></a>
Sedaghati, F. and S. Pezeshk, (2026). Transfer Learning for Developing Ground-Motion Models: Application to Iran Using NGA-West2 Data, Earthquake Spectra
