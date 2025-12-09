# ParticleEventClassification

## Descripción del proyecto

En este proyecto se diseñan dos modelos reproducibles para la clasificación binaria de eventos de física de partículas con el objetivo de separar eventos raros de señal (s) de los eventos de fondo o background (b). The main goal is to:

-Classify rare signal (s) events from abundant background (b) events.
-Explore physics-motivated kinematic variables.
-Implement cleaning and preprocessing strategies.
-Train machine learning models (Logistic Regression Model/ANN).
-Evaluate model performance using weighted metrics.

Distinguishing signal from background is a central challenge in particle physics. This project demonstrates how data science and machine learning techniques can be adapted to real experimental constraints through event weighting, domain-specific features, and physics-aware evaluation.

## Dataset
The dataset simulates collider-style events.
It contains 250,001 rows and 33 columns, including kinematic variables and event-level metadata.

-Target: ```Target ∈ {s, b}```
-Weight: continuous importance factor used as ```sample_weight```
-Features: reconstructed physics variables (mass, energy, angles, jets, MET)

### Key Feature Groups
-Identifiers & Labels: ```EventId```, ```Target```, ```Weight```
-Derived Physics Features: ```DER_mass_MMC```, ```DER_mass_vis```, ```DER_pt_h```, ```DER_mass_transverse_met_lep```, ```DER_deltaeta_jet_jet```, ```DER_mass_jet_jet```, ```DER_lep_eta_centrality```
-Primary Objects: tau and lepton kinematics (```PRI_tau_*```, ```PRI_lep_*```)
-Missing Transverse Energy (MET): ```PRI_met```, ```PRI_met_phi```, ```PRI_met_sumet```

-Jets: ```PRI_jet_num```, leading + subleading jet momenta and angles, ```PRI_jet_all_pt```

## Technologies Used
-Python 3
-Pandas, NumPy, Keras
-Matplotlib, Seaborn
-Scikit-Learn, Tensorflow

## How to Run the Project
1.  Clone the repository
    ```bash
    git clone [https://github.com/lvalencia232/ParticleEventClassification](https://github.com/lvalencia232/ParticleEventClassification.git)
    cd particle-event-classification
    ```
2.  Install dependencies
    ```bash
    pip3 install -r requirements.txt
    ```
3.  Abrir el notebook:
    ```bash
    jupyter notebook particle_event_class.ipynb
    ```
4. Create a new branch for every change
    ```bash
    git checkout -b feature/<feature-name>
    ```
5. Commit your changes
    ```bash
    git commit -m "Description of the update"
    ```
6. Push your branch
    ```bash
    git push origin feature/<feature-name>
    ```
7. Open a Pull Request and merge: After merging, delete the feature branch to keep the repository clean.
