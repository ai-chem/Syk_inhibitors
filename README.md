# Integrating QSAR Modelling with Reinforcement Learning for Novel Syk Inhibitor Discovery

**Spleen tyrosine kinase (Syk)** is an intracellular protein expressed in various immune cells, playing a crucial role in inflammatory reactions. Its hyperactivation is associated with numerous autoimmune, allergic, and inflammatory diseases, making Syk an *attractive therapeutic target*.

**Immune thrombocytopenia**, a rare autoimmune disorder, is one condition where new Syk inhibitors are particularly needed. Despite the development of several Syk inhibitors, including the approved drug Fostamatinib, challenges persist in achieving optimal efficacy and safety profiles.

To address these challenges, computational methods and machine learning approaches have been increasingly utilized in drug discovery. This study introduces a novel approach using generative models based on reinforcement learning to obtain novel Syk inhibitors molecules. Moreover our approach demonstrates a methodology for adapting generative algorithms to design inhibitors against specific therapeutic targets.



# Project implementation

<div align="middle"><img src="Data/Pipeline (2).svg" style="width : 100%; min-width : 300px; "/></div>  

## Data collection
An open database of medicinal molecules (**ChEMBL**), were used as data sources for collecting the dataset. `all_mols.csv`

## Data processing
After initial processing presented in the file `Data_processing.ipynb` the dataset contained $3{,}152$ inhibitor molecules with a known $IC_{50}$ value, a key indicator of the effectiveness of a molecule.

**Morgan fingerprints** were chosen as the main molecular descriptors. The dataset prepared for training, with loaded descriptors, is presented in the Data folder `df_fp.csv`.

## QSAR model
The process of model training is presented in the file `Predicted_model.ipynb`.

## Inhibitors generation
Evaluation of the generated molecules and generation approaches is presented in the file `Generation_analysis.ipynb`.

## Promising inhibitors
Analysis of the properties of the obtained molecules, as well as their comparison with ChEMBL inhibitors is presented in the file `Property_analysis.ipynb`.

# Syk Inhibitor IC50 Predictor: A SMILES-based Tool for Drug Discovery

The notebook `IC50_predictor.ipynb` provides an interactive tool for predicting the $IC_{50}$ values of potential Syk inhibitors based on their SMILES representation.
