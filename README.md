# DeepLearning2021

# Milestone 01

Welcome to the assignment of Sándor Gregus (YRVTLZ), Katalin Ócsai (EW9A0Z), and Mátyás Prechl (JR4JDJ)!

We decided to work on a larger and simpler database: CelebA. We have reviewed not only the recommended GAN literature (https://paperswithcode.com/paper/progressive-growing-of-gans-for-improved ) but also VAEs and beta VAEs.

In the first milestone we prepared a balanced training dataset for the later classificaton task. The balance of the dataset is proven to be essential as shown in the following documents:
* https://dl.acm.org/doi/10.5555/1622434.1622445
* https://www.kth.se/social/files/588617ebf2765401cfcc478c/PHensmanDMasko_dkand15.pdf

I.e. generally, the distribution of the training data has a huge impact on the performance of CNN. The balanced distribution yielded a significantly better performance than imbalanced one. The heavier the imbalance is, the worse the total classification performance. This kind of fragility when using imbalanced data in the CNN training algorithm can be eliminated by the proper selection of distribution of dataset.

We investigated some solutions for dataset generation and preprocession.
To discover the relationship between the attributes we plotted the correlation matrix between the values.

* https://www.kaggle.com/ky2019/starter-celebfaces-attributes-celeba-b5421ae1-e
* https://www.kaggle.com/saket0565/celebfaces-facial-attribute-recognition
* https://www.kaggle.com/bmarcos/image-recognition-gender-detection-inceptionv3
* https://www.kaggle.com/fkdplc/celeba-dcgan-for-generating-faces/notebook

This first milestone was implemented in DeepLearning2021_Milestone01.ipynb

# Milestone 2
In this milestone
1. we built a discriminative model for learning the labels of the database - DeepLearning2021_Milestone1_2.ipynb
2. a deep ganarative model (i.e. a variational autencoder) was trained to learn the features of the faces - DeepLearning2021Milestone02.ipynb

The discriminatve model used transfer learning based on an Inception v3 model pretrained on imagenet and the last layers were trained on the database with an early stopping callback. With the first naive model a pecision of 90% was reached. (for more details see the documentation later)

