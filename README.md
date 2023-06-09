![LogoKDN-removebg](https://github.com/Leonard2310/KinDeNet/assets/71086591/c5179afd-2bd8-4ec7-8e93-67af16d8dd9d)

KinDeNet (Kinship Detection Network) is a project developed for Federico II University with the aim of creating a neural network capable of extracting the degree of relatedness or non-relatedness between two images. The project utilizes the 'Family in the Wild' dataset and implements a siamese neural network using the triplet loss technique. This network leverages the ResNet50 architecture of VGGFace.

## Project Description
The first step of the project involves training a siamese network with triplet loss to obtain optimized weights. These weights are then used to extract feature vectors from the images. These feature vectors capture the visual representations of individuals. 

In the second step, a two-input siamese network is utilized to further extract features using the weights obtained from the previous step. The extracted features are paired with the dataset labels and fed into a pipeline consisting of two classifiers—a binary classifier and a three-class classifier.

The binary classifier determines whether two individuals are related or unrelated, while the three-class classifier categorizes the degree of kinship (parent-child, siblings or grandparent-grandchild). This two-step approach allows the KinDeNet model to accurately recognize the degree of kinship between a pair of people.

In a different approach, we explored the use of Fine-tuning. Instead of separating the feature extraction and classification phases, we utilized the weights from the network trained with triplet loss to create a pipeline of two siamese networks, with the final output representing the degree of kinship between the pair of individuals.

This methodology demonstrated significant improvements in evaluation metrics. However, it is important to note that this approach is more time-consuming both in terms of execution and testing.

KinDeNet offers a robust solution for kinship detection, it opens up possibilities for various applications, such as family tree construction, and forensic investigations.

## Requirements
- Python (version 3.6 or higher)
- TensorFlow (version 2.12.0 or higher)
- Keras-Applications (version 1.0.8 or higher)
- Keras-Preprocessing (version 1.1.2 or higher)
- Keras-VGGFace (version 0.6 or higher)

The majority of experiments were performed on the Colaboratory cloud platform for deep learning, specifically using a T4 GPU with 12.7GB of memory.

The script will evaluate the model using the test dataset and print the evaluation metrics.

## Results
The model trained on KinDeNet has shown good performance in detecting the degree of kinship between images, achieving high accuracy. However, it is important to note that the results may vary depending on the dataset used and the training parameters set.

## Contributions
We welcome contributions and improvements to the KinDeNet project. If you would like to contribute, please submit a pull request. Make sure to discuss and plan proposed changes with the development team before starting the work.

## Authors
- [Leonardo Catello](https://github.com/Leonard2310) 
- [Lorenzo Manco](https://github.com/Rasbon99) 
- [Francesco Di Serio](https://github.com/fdiserio)

## License
This project is licensed under the [GNU General Public License v3.0]. Refer to the LICENSE file for more information.

## Acknowledgments
The KinDeNet project builds upon the following works and datasets:

- [Family in the Wild Dataset](https://github.com/visionjo/fiw)
- [VGGFace](https://github.com/rcmalli/keras-vggface)

