# Image Classification challenge AN2DL Politecnico di Milano 2022
This is the model that I used in the [Image Classification challenge](https://web.archive.org/web/20221129163804/https://codalab.lisn.upsaclay.fr/competitions/8522) of the course "Artificial Neural Networks and Deep Learning" course held at Politecnico di Milano in 2022.

The challenge consisted on the classification of 8 different plant species from photos with the dimensions `(96, 96, 3)`. The model me and my team developed uses the transfer learning approach with `DensNet` as the base model.

We ended up acheiving an **accuracy of 86%**, you can check the results [here](https://codalab.lisn.upsaclay.fr/competitions/8522#results).

## Models details
For more details about the model check the [Report](ANNDL1-Report.pdf). Briefly, we used the following techniques:
1. Transfer Learning with `DenseNet` model with the "Weight Initialization" technique: the whole model was trained, in two phases. First, only the classification head with an high learning rate and then the whole model with a low learning rate.
3. Standard data augmentation (flip, rotate, zoom)
5. [Class weighting](https://www.tensorflow.org/tutorials/structured_data/imbalanced_data#class_weights) to fight the imbalance of the dataset


