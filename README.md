# Integrating QSAR Modelling with Reinforcement Learning for Novel Syk Inhibitor Discovery

**Spleen tyrosine kinase (Syk)** is an intracellular protein expressed in various immune cells, playing a crucial role in inflammatory reactions. Its hyperactivation is associated with numerous autoimmune, allergic, and inflammatory diseases, making Syk an *attractive therapeutic target*.

**Immune thrombocytopenia**, a rare autoimmune disorder, is one condition where new Syk inhibitors are particularly needed. Despite the development of several Syk inhibitors, including the approved drug Fostamatinib, challenges persist in achieving optimal efficacy and safety profiles.

To address these challenges, computational methods and machine learning approaches have been increasingly utilized in drug discovery. While previous studies have employed virtual screening, pharmacophore modeling, and molecular docking to identify potential Syk inhibitors, this study introduces a novel approach using generative models based on reinforcement learning. The FREED++ deep reinforcement learning method is used to generate new candidate structures, with machine learning methods employed to evaluate promising molecules. This innovative approach not only applies state-of-the-art generative models to Syk inhibitor design but also demonstrates a methodology for adapting generative algorithms to design inhibitors against specific therapeutic targets.

# Project implementation

An open database of medicinal molecules (**ChEMBL**), were used as data sources for collecting the dataset. After initial processing presented in the file `data_preprocessing.ipynb` the dataset contained $3{,}152$ inhibitor molecules with a known $IC_{50}$ value, a key indicator of the effectiveness of a molecule.

**Morgan fingerprints** were chosen as the main molecular descriptors. 
Подготовленный для обучения предказательной модели датасет, с выгруженными дескрипторами представлен по ссылке.

Процесс обучения моделей  is presented in the file `manual_patterns.ipynb`. final model - ляля


## Generative model

Since the therapeutic effect of a molecule is largely determined by its affinity for the target protein, a generation method using **molecular docking** was chosen. To do this, we used the `Freed++` model. This model was chosen due to its fast and efficient generation method, as well as its versatility for a variety of proteins.

The results of using this model have already led to the first potential inhibitors. Of course, we still have to improve our results by expanding the capabilities of the predictive model to more accurately assess the generated molecules, as well as using different approaches in working with `Freed++`.

