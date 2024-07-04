# ChessMatch

This repository contains a chess player classification model created by Benjamín Varela and Eduardo Álvarez, undergraduate students in Data Science at Pontificia Universidad Católica de Chile, for the Data Mining course (IIC2433). The model is designed to classify players into one of the world chess champions based on their playing data.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Model](#model)
- [Additional Files](#additional-files)
- [Usage](#usage)
- [Contributors](#contributors)
- [License](#license)
- [Attribution](#attribution)

## Introduction

The idea of ​​the project was to create a model that can analyze a player's games and recommend the world champion with the most similar playing style, so that the player can learn from him.
It started as a simple final project, but then it became something more personal.

## Dataset

The dataset used in this project comes from the website https://www.pgnmentor.com/files.html, but it has been preprocessed to include only the moves of a single player and their name.

## Model

The model uses Sentence BERT to vectorize the chess game data into high-dimensional vectors.
To address class imbalance in the training dataset, SMOTE was applied for oversampling. These vectors are then classified using a support vector machine (SVM) to predict the player of individual games. Then, for each World Champion, a unique vector is created based on the confusion matrix to represent their playing style.

## Additional Files

Some files necessary for the project are too large to be included directly in this repository. You can download these files from our Google Drive:

[Download Additional Files](https://drive.google.com/drive/folders/1ihB4ttz64WtbODxvQUZ55f21bVLH3OUe?usp=drive_link)

## Usage

In the main file you can find all our research and model creation process, and also the results.

You can also use the model with your own games, to do this you need:
- Download the pgn file of your games, if you use lichess you can download it directly from the website and if you use chess.com you can use: https://www.openingtree.com/
- Download "svm_model_chess.pkl" from the drive.
- Finally you must run the main from where it says "To use the model run from here" and change the path to your file and put your username in the create_pred_vector function

(You must have sentence_transformers and python-chess installed in a python environment)
(We do not recommend using too many games, since the model takes approximately 1 minute per 100 games , at least for us)

## Contributors

[Benjamín Varela](https://github.com/212113114)

[Eduardo Álvarez](https://github.com/Aledgit)

## License

This project is available under a dual license:

-MIT License (for non-commercial use): See the LICENSE file for details.

-Commercial License (for commercial use): If you wish to use this software for commercial purposes, please contact the authors to obtain a commercial license.

## Attribution

Please ensure to provide appropriate credit when using or modifying this project. Include the following in any derived works:

Created by Benjamín Varela and Eduardo Álvarez, undergraduate students in Data Science at Pontificia Universidad Católica de Chile









