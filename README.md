# KinDeNet - Kinship Detection Network

KinDeNet is a project developed for the Federico II University with the aim of creating a neural network that can extract the degree of kinship or non-correlation between two images.

## Project Description

The KinDeNet project is based on the "Family in the Wild" dataset and implements a neural network that utilizes the triplet loss technique, using the ResNet50 architecture of VGGFace as the base for feature extraction. Additionally, a siamese network is implemented for image recognition.

Triplet loss is a technique used in image recognition learning that is based on the idea of creating triplets of images, consisting of an anchor image, a positive image, and a negative image. The goal of the network is to learn to minimize the distance between the anchor and the positive image, while maximizing the distance between the anchor and the negative image. This way, the network learns to discriminate between similar (related) and unrelated images.

The ResNet50 architecture of VGGFace is used as the feature extractor, as it has been proven to be very effective in face recognition. The extracted features are then used to calculate the triplet loss and train the network.

The siamese network is implemented for image recognition, creating two branches of the network that share the same weights. This allows the network to compare the features extracted from the two images and determine if they are related or unrelated.

## Installation Requirements

- Python (version 3.6 or higher)
- TensorFlow (version 2.0 or higher)
- Keras (version 2.3 or higher)
- NumPy
- Pandas
- Matplotlib


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

We thank the original authors for their contributions.

