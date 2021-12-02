# DeepLearning2021

# Milestone 01

Welcome to the assignment of ~~Sándor Gregus (YRVTLZ)~~ (unfortunately quitted), Katalin Ócsai (EW9A0Z), and Mátyás Prechl (JR4JDJ)!

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

# Milestone 02
In this milestone
1. we built a discriminative model for learning the labels of the database - DeepLearning2021_Milestone1_2.ipynb
2. a deep generative model (i.e. a variational autencoder) was trained to learn the features of the faces - DeepLearning2021Milestone02.ipynb

The discriminatve model used transfer learning based on an Inception v3 model pretrained on imagenet and the last layers were trained on the database with an early stopping callback. With the first naive model a pecision of 90% was reached. (for more details see the documentation later)

A deep generative model i.e. a variational autoencoder was built to learn the features of the faces. 
To discover the meaning of the latents a latent traversal was implemented with an 
The latent space of the variational autoencoder consisted of 64 dimension and some of them coded interpretable features of the faces. I.e.
* 23th dimension seems to code the factor for the color of the hair
* 27.th dimension seems to code the existence of bangs
* 28.th dimension seems to code the rotation of the face
* 29.th dimension seems to code the existence of sunglasses
* 61.th dimension seems to code the make-up

1.) Color of the hair:

![image](https://user-images.githubusercontent.com/24832770/144511184-0d8f90c7-3001-4ece-bb9d-6ed5b099c6f1.png)

2.) The existence of bangs

![image](https://user-images.githubusercontent.com/24832770/144511613-3b6ae2c1-de80-43f5-ba92-530fc50a6aa9.png)

3.) The rotation of the face

![image](https://user-images.githubusercontent.com/24832770/144511709-ba0a118e-9576-458f-9e8c-24167e98f921.png)

4.) The existence of sunglasses

![image](https://user-images.githubusercontent.com/24832770/144511940-4b93b5e7-a6ff-4169-8de3-fd6d22255a03.png)

5.) Color of the skin / the existence of the make-up 

![image](https://user-images.githubusercontent.com/24832770/144512260-8d880358-4224-4d72-b967-b1e20c75a873.png)





