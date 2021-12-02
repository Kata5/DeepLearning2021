# DeepLearning2021



Welcome to the assignment of Sándor Gregus (YRVTLZ), Katalin Ócsai (EW9A0Z), and Mátyás Prechl (JR4JDJ)!

We decided to work on a larger and simpler database: CelebA. We have reviewed not only the recommended GAN literature (https://paperswithcode.com/paper/progressive-growing-of-gans-for-improved ) but also VAEs and beta VAEs.

In the first milestone we prepared a balanced training dataset for the later classificaton task. The balance of the dataset is proven to be essential as shown in the following documents:
* https://dl.acm.org/doi/10.5555/1622434.1622445
* https://www.kth.se/social/files/588617ebf2765401cfcc478c/PHensmanDMasko_dkand15.pdf

I.e. generally, the distribution of the training data has a huge impact on the performance of CNN. The balanced distribution yielded a significantly better performance than imbalanced one. The heavier the imbalance is, the worse the total classification performance. This kind of fragility when using imbalanced data in the CNN training algorithm can be eliminated by the proper selection of distribution of dataset.

We investigated some solutions for dataset generation and preprocession:

* https://www.kaggle.com/ky2019/starter-celebfaces-attributes-celeba-b5421ae1-e
* https://www.kaggle.com/saket0565/celebfaces-facial-attribute-recognition
* https://www.kaggle.com/bmarcos/image-recognition-gender-detection-inceptionv3
* https://www.kaggle.com/fkdplc/celeba-dcgan-for-generating-faces/notebook
