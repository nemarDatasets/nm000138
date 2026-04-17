[![DOI](https://img.shields.io/badge/DOI-10.82901%2Fnemar.nm000138-blue)](https://doi.org/10.82901/nemar.nm000138)

# Alex Motor Imagery dataset

Alex Motor Imagery dataset.

## Dataset Overview

- **Code**: AlexandreMotorImagery
- **Paradigm**: imagery
- **DOI**: 10.5281/zenodo.806022
- **Subjects**: 8
- **Sessions per subject**: 1
- **Events**: right_hand=2, feet=3, rest=4
- **Trial interval**: [0, 3] s
- **File format**: fif
- **Data preprocessed**: True

## Acquisition

- **Sampling rate**: 512.0 Hz
- **Number of channels**: 16
- **Channel types**: eeg=16
- **Channel names**: Fpz, F7, F3, Fz, F4, F8, T7, C3, Cz, C4, T8, P7, P3, Pz, P4, P8
- **Montage**: standard_1005
- **Hardware**: g.tec g.USBamp
- **Software**: Matlab/Simulink
- **Reference**: earlobe
- **Sensor type**: EEG
- **Line frequency**: 50.0 Hz

## Participants

- **Number of subjects**: 8
- **Health status**: healthy
- **Species**: human

## Experimental Protocol

- **Paradigm**: imagery
- **Number of classes**: 3
- **Class labels**: right_hand, feet, rest
- **Trial duration**: 3.0 s
- **Study design**: Cue-based motor imagery paradigm (Step B of Brain Switch campaign) for familiarization and algorithm development
- **Feedback type**: none
- **Stimulus type**: visual cue
- **Stimulus modalities**: visual, auditory
- **Primary modality**: visual
- **Synchronicity**: synchronous
- **Mode**: offline
- **Instructions**: Cue-based paradigm without feedback. Subjects perform 20 imagined movements per class (right hand, feet, rest) following a visual cue, lasting 3 seconds each. Total duration approximately 10 minutes.

## HED Event Annotations

Schema: HED 8.4.0 | Browse: https://www.hedtags.org/hed-schema-browser

```
  right_hand
    ├─ Sensory-event, Experimental-stimulus, Visual-presentation
    └─ Agent-action
       └─ Imagine
          ├─ Move
          └─ Right, Hand

  feet
    ├─ Sensory-event, Experimental-stimulus, Visual-presentation
    └─ Agent-action
       └─ Imagine, Move, Foot

  rest
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Rest

```
## Paradigm-Specific Parameters

- **Detected paradigm**: motor_imagery
- **Imagery tasks**: right_hand, feet, rest
- **Cue duration**: 1.0 s
- **Imagery duration**: 3.0 s

## Data Structure

- **Trials**: 60
- **Trials per class**: right_hand=20, feet=20, rest=20
- **Trials context**: 20 trials per class, 3 second duration each

## Preprocessing

- **Re-reference**: earlobe

## Signal Processing

- **Classifiers**: LDA, SVM, MDM, Riemannian, kNN, Naive Bayes, Logistic Regression
- **Feature extraction**: CSP, FBCSP, ERD, ERS, PSD, Covariance/Riemannian, AR, ICA
- **Frequency bands**: alpha=[8.0, 12.0] Hz; mu=[8.0, 12.0] Hz
- **Spatial filters**: CSP, Geodesic filtering

## Cross-Validation

- **Method**: cross-validation
- **Evaluation type**: within_session

## BCI Application

- **Applications**: motor_control
- **Environment**: laboratory
- **Online feedback**: False

## Tags

- **Pathology**: Healthy
- **Modality**: Motor
- **Type**: Research

## Documentation

- **Description**: Motor imagery dataset from the PhD dissertation of A. Barachant. Contains EEG recordings from 8 subjects performing motor imagination tasks (right hand, feet, or rest). Used to validate robust control of an effector via asynchronous EEG-based brain-machine interface.
- **DOI**: 10.5281/zenodo.806022
- **Associated paper DOI**: tel-01196752v1
- **License**: CC-BY-SA-4.0
- **Investigators**: Alexandre Barachant
- **Senior author**: Alexandre Barachant
- **Contact**: alexandre.barachant@gmail.com
- **Institution**: Université de Grenoble
- **Department**: Laboratoire Électronique et système pour la santé CEA-LETI
- **Address**: CEA-LETI Grenoble, France
- **Country**: France
- **Repository**: Zenodo
- **Data URL**: https://zenodo.org/record/806023
- **Publication year**: 2012
- **Keywords**: brain-computer interface, motor imagery, EEG, Riemannian geometry, asynchronous BCI, brain-switch, covariance matrices, Common Spatial Pattern

## Abstract

Motor imagery dataset from the PhD thesis on robust control of an effector via asynchronous EEG brain-machine interface (Barachant, 2012). This shared dataset corresponds to Step B (cue-based imagery without feedback) of the Brain Switch campaign. Contains recordings from 8 subjects performing 3 motor imagery tasks (right hand, feet, rest) with 20 trials per class.

## Methodology

Cue-based paradigm without feedback (Step B of Brain Switch campaign). EEG recorded at 512 Hz with 16 active electrodes using a g.tec g.USBamp amplifier. Reference electrode placed on the ear. Subjects performed imagined movements following visual cues: right hand, feet, and rest, 20 trials per class, 3 seconds each. Recorded in standard office conditions (not shielded laboratory). Software: Matlab/Simulink with g.tec drivers.

## References

Barachant, A., 2012. Commande robuste d'un effecteur par une interface cerveau machine EEG asynchrone (Doctoral dissertation, Université de Grenoble). https://tel.archives-ouvertes.fr/tel-01196752
Appelhoff, S., Sanderson, M., Brooks, T., Vliet, M., Quentin, R., Holdgraf, C., Chaumon, M., Mikulan, E., Tavabi, K., Hochenberger, R., Welke, D., Brunner, C., Rockhill, A., Larson, E., Gramfort, A. and Jas, M. (2019). MNE-BIDS: Organizing electrophysiological data into the BIDS format and facilitating their analysis. Journal of Open Source Software 4: (1896). https://doi.org/10.21105/joss.01896

Pernet, C. R., Appelhoff, S., Gorgolewski, K. J., Flandin, G., Phillips, C., Delorme, A., Oostenveld, R. (2019). EEG-BIDS, an extension to the brain imaging data structure for electroencephalography. Scientific Data, 6, 103. https://doi.org/10.1038/s41597-019-0104-8

---
Generated by MOABB 1.4.3 (Mother of All BCI Benchmarks)
https://github.com/NeuroTechX/moabb
