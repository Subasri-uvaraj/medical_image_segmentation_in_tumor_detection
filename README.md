# MEDICAL IMAGE SEGMENTATION IN TUMOR DETECTION

## Project Overview
My project is used to monitor the tumor in the brain. This will be used to monitor how the medication works on the tumor for resolving.

## Table of Contents
- [Project Overview](#project-overview)
- [Installation](#installation)
- [Usage](#usage)
- [Model Architecture](#model-architecture)
- [Datasets](#datasets)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Installation
To set up the project, follow these steps:

1. Clone the repository:
    ```sh
    git clone https://github.com/YourUsername/YourRepository.git
    cd YourRepository
    ```

2. Install MATLAB on your computer.

3. Include the MRI or CT image of the tumor in the `data` directory of the project.

## Usage
To use the model for tumor detection:

1. Prepare your dataset and place it in the `data` directory.
2. Run the main script:
    ```matlab
    main_script.m
    ```

## Model Architecture
The model used for this project is based on the U-Net architecture. U-Net is a convolutional neural network specifically designed for biomedical image segmentation. It consists of an encoder (downsampling path) to capture context and a symmetric decoder (upsampling path) that enables precise localization. Skip connections between the encoder and decoder paths ensure that fine-grained information is retained throughout the network. The architecture can be visualized as follows:


Key components:
- **Encoder:** Several convolutional layers with ReLU activation, followed by max-pooling for downsampling.
- **Bottleneck:** Convolutional layers that capture high-level features.
- **Decoder:** Upsampling layers (e.g., transposed convolutions) that restore the image resolution.
- **Skip Connections:** Bridge between corresponding layers of the encoder and decoder to improve segmentation accuracy.

## Datasets
The dataset used for this project is the [Brain Tumor Segmentation (BraTS) dataset](https://www.med.upenn.edu/cbica/brats2018/data.html). The BraTS dataset contains multi-modal MRI scans (T1, T2, FLAIR, and T1Gd) with manually annotated tumor regions. Each scan is labeled with:
- **Enhancing Tumor (ET)**
- **Tumor Core (TC)**
- **Whole Tumor (WT)**

To access the dataset, follow the instructions on the BraTS website and download the data to the `data` directory in your project.

## Results
The model achieved the following results:
- Dice Coefficient: 0.85
- Jaccard Index: 0.75

Sample segmentation results are shown below:

![Sample Segmentation](path_to_sample_segmentation_image)

## Contributing
Contributions are welcome! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch:
    ```sh
    git checkout -b feature/YourFeature
    ```
3. Commit your changes:
    ```sh
    git commit -m 'Add YourFeature'
    ```
4. Push to the branch:
    ```sh
    git push origin feature/YourFeature
    ```
5. Open a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Acknowledgements
We would like to thank the contributors and maintainers of the BraTS dataset and the open-source libraries used in this project.



