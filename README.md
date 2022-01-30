# ser-transfer

We present here the models that were designed for a Brazilian Portuguese Speech Emotion Recognition shared task (https://sites.google.com/view/ser2022/home?authuser=0) by a team composed of participants from FFLCH-USP, ICMC-USP, and EESC-USP:
Caroline Alves, Bruno Carlotto, Bruno Dias, Anátale Garcia, Bruno Gianesi, Renan Izaias, Maria Luiza de Morais, Paula de Oliveira, Vinícius G. Santos, Rafael Sicoli, Flaviane R. Fernandes Svartman, Sandra Aluisio and Sidney Leal.

The task given was to classify brazilian portuguese audios in neutral, non-neutral female or non-neutral male.

Two datasets were used: the small training set made available by the task (with samples extracted from the C-ORAL-BRASIL I corpus http://www.c-oral-brasil.org/)  as well as the CETUC dataset (with audios selected from the CETEN-Folha corpus https://www.linguateca.pt/cetenfolha/index_info.html).

Two architectural approaches were devised: one using a sequential transfer learning method in which the frozen layers of a first network designed to classify gender trained on the CETUC dataset was used on a second network which classifies the training set as neutral, non-neutral female or non-neutral male.

The second approach used a multitask architecture, in which a larger network simultaneously tries to solve both the gender classification of the CETUC data and the three classes classification of the training dataset using shared middle layers.

The models from each architecture differ in the usage of data augmentation, feature selection and the addition of auxiliary data extracted from the training set via the PRAAT software.
