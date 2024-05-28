# Wildlife Intrusion Detection System

## Overview
This project aims to detect wildlife intrusions using machine learning models. We experimented with multiple architectures such as AlexNet and VGGNet and developed a front-end interface using Flask API. The dataset was collected by scraping the web for images of various animals and labeling them accordingly.

## Table of Contents
- [Introduction](#Introduction)
- [Dataset](#dataset)
- [Models](#models)
    - AlexNet
    - VGGNet
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Introduction
The Wildlife Intrusion Detection System is designed to automatically identify the presence of animals in restricted areas using image recognition. This system can help in monitoring and managing wildlife in and around sensitive zones such as farms, urban areas, and protected sites.

## Dataset
The dataset used in this project was collected by scraping images of animals from the web. These images were then labeled to create a comprehensive dataset suitable for training deep learning models.

## Models
### AlexNet
AlexNet is a convolutional neural network that achieved breakthrough performance in image classification tasks. In this project, we implemented AlexNet to classify images of animals.

The implementation details can be found in the following files:

- [AlexNet Notebook](./Training/Alexnet.ipynb)
- [AlexNet Script](./Alexnet.py)
### VGGNet
VGGNet is another convolutional neural network known for its simplicity and depth. We used VGGNet to compare its performance with AlexNet.

The implementation details can be found in the following files:

- [VGGNet Notebook](./Training/VGG_trn_new.ipynb)
- [VGGNet Script](./HyperParameterTuning/Vggnet.py)

## Installation
To run this project, you need to have Docker installed. Follow these steps to set up the environment:

Clone the repository:

```bash
git clone https://github.com/arshakshan/wildlife-intrusion-detection.git
cd wildlife-intrusion-detection
```

Build the Docker image:

```bash
docker build -t wildlife-detection .
```

Run the Docker container:

```bash
docker run -p 5000:5000 wildlife-detection
```

## Usage
Once the Docker container is running, you can access the Flask API to interact with the model. The API provides endpoints for uploading images and receiving predictions on the presence of wildlife.

To upload an image and get a prediction, use the following curl command:

```bash
curl -X POST -F 'file=@/path/to/your/image.jpg' http://localhost:5000/predict
```

## Results
The results of the experiments with different models are summarized as follows:

- AlexNet: [Link to Results Notebook](./Alexnet.ipynb)
- VGGNet: [Link to Results Notebook](./Training/VGG_trn_new.ipynb)

Comparative analysis and performance metrics are included in the respective notebooks.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request if you have suggestions or improvements.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

## Acknowledgements
We would like to thank all the contributors and open-source projects that helped in the creation of this project.
