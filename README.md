# Machine Learning Workshop — September 23, 2026

Welcome to the repository for the **Machine Learning Workshop** held on **September 23, 2026**.

This workshop is part of an ongoing machine learning training series focused on building practical intuition for machine learning methods used in scientific research. Previous sessions introduced foundational machine learning concepts, terminology, regression, decision trees, neural networks, and active learning.

This session shifts from theory to practice.

Participants will work through hands-on examples involving:

* Neural networks using **PyTorch**
* Model training and evaluation
* Scientific machine learning workflows
* Active learning
* The **FALCON** active-learning framework

---

## Workshop Structure

The workshop is divided into two main sections.

### Part I — Introduction to Neural Networks with PyTorch

The first portion of the workshop provides a short practical introduction to implementing neural networks using PyTorch.

Topics include:

* PyTorch tensors
* Building a neural network
* Forward propagation
* Loss functions
* Optimizers
* Training loops
* Evaluating model predictions

The goal is not to provide a complete introduction to deep learning, but rather to connect the neural-network concepts discussed in previous meetings with an actual working implementation.

---

### Part II — Active Learning with FALCON

The second and larger portion of the workshop focuses on a hands-on active-learning workflow using **FALCON**.

Participants will work through the process of using training data, constructing a machine-learning model, and exploring how active learning can be used to efficiently improve a model by identifying configurations where additional training data are most useful.

This section connects the machine-learning concepts discussed throughout the workshop series with workflows relevant to atomistic simulations and machine-learned interatomic potentials.

---

## Repository Structure

The repository will contain all materials needed for the workshop.

```text
MLWorkshop-09232026/
│
├── README.md
│
├── notebooks/
│   ├── pytorch_nn_intro.ipynb
│   └── falcon_tutorial.ipynb
│
├── training_data/
│   └── ...
│
├── docs/
│   └── hellbender_jupyter_tutorial.md
│
└── scripts/
    └── ...
```

### `notebooks/`

Contains the Jupyter notebooks used during the hands-on portions of the workshop.

### `training_data/`

Contains datasets and example configurations used during the exercises.

### `docs/`

Contains additional workshop documentation, including instructions for launching Jupyter Notebook sessions on Hellbender through OnDemand Remote Resources.

### `scripts/`

Contains any supporting scripts used by the workshop exercises.

---

## Getting Started

Workshop participants should clone this repository onto **Hellbender** before beginning the exercises.

```bash
git clone https://github.com/cdzk97/MLWorkshop-09232026.git
```

Then enter the repository:

```bash
cd MLWorkshop-09232026
```

You can confirm that the repository was cloned successfully with:

```bash
ls
```

The workshop materials should then be available locally in your Hellbender working directory.

---

## Running Jupyter on Hellbender

The workshop notebooks must be run through the Hellbender OnDemand Remote Resources system.

Jupyter Notebook should not be launched directly from the Hellbender login node, and participants should not attempt to start Jupyter manually from a command-line compute-node session.

Instead, Hellbender's OnDemand interface is used to request the required resources and launch the Jupyter Notebook environment.

After cloning this repository onto Hellbender, follow the dedicated setup guide:

docs/hellbender_jupyter_tutorial.md

The guide will walk through:

Logging into Hellbender
Cloning the workshop repository
Opening OnDemand Remote Resources
Requesting a Jupyter Notebook session
Selecting the appropriate computational resources
Launching the interactive Jupyter session
Navigating to the workshop repository
Opening and running the workshop notebooks

For this workshop, OnDemand Remote Resources is the required method for launching Jupyter Notebook on Hellbender.

## Prerequisites

This workshop assumes basic familiarity with:

* Linux command-line navigation
* Python
* Jupyter notebooks
* Basic machine-learning terminology

Some familiarity with the following concepts will also be helpful:

* Linear regression
* Decision trees
* Neural networks
* Training and validation data
* Loss functions
* Optimization
* Active learning

These concepts were introduced during previous sessions in this workshop series.

No extensive prior experience with PyTorch is required.

---

## Workshop Goals

By the end of the session, participants should be able to:

* Understand the basic structure of a neural network implemented in PyTorch
* Identify the main components of a machine-learning training workflow
* Train and evaluate a simple neural-network model
* Understand the motivation behind active learning
* Follow a basic FALCON workflow
* Run machine-learning calculations interactively on Hellbender
* Modify and experiment with the provided Jupyter notebooks

---

## Important HPC Reminder

Hellbender uses a batch scheduling system to manage computational resources.

The **login node should primarily be used for tasks such as**:

* Editing files
* Managing directories
* Git operations
* Submitting jobs
* Requesting interactive computational resources

Training machine-learning models or running resource-intensive notebooks should be performed on an allocated **compute node**.

---

## Workshop Instructors

**Carlos Garcia**
**Carson D. Ziemke**


University of Missouri

---

## About This Repository

This repository is intended to provide a reproducible set of materials for the September 23, 2026 machine-learning workshop.

The materials may continue to be updated as the workshop exercises, datasets, and documentation are refined.

Participants are encouraged to clone the repository before the workshop and use `git pull` to retrieve any updates made before the session.

```bash
git pull
```

---

## Questions or Issues

If you encounter problems with the repository, Jupyter setup, or workshop materials, please ask during the workshop or contact one of the workshop instructors.

When reporting an issue, it is helpful to include:

* The command you ran
* The complete error message
* The directory you were working in
* Whether you were on the Hellbender login node or a compute node

This information makes troubleshooting much easier.
