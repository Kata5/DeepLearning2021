# DeepLearning2021

Welcome to the assignment of ~~Sándor Gregus (YRVTLZ)~~ (unfortunately quitted), Katalin Ócsai (EW9A0Z), and Mátyás Prechl (JR4JDJ)!

# Contributions
* Sándor Gregus would have been responsible for milestone 2 but he quitted on the 24/November without any contribution to the project.
* Mátyás Prechl would have been responsible for the visualization of the hiperparameter tuning but he could not contribute to MileStone3 at all.
* Katalin Ócsai contributed to all the three milestones (as it can be seen on commit list).
      *  splitting function for test, training, validation data, some data discovery for the discriminative model
      *  the entire solution for generative model (VAE), latent traversal
      *  parameter optimalistion of VAE
      *  finding meaningful dimensions of VAE according to the laten traversal
      *  entire documentation (documentation.pdf, future planes,  belogs to her (as finally she was alone in mileStone 3)

# Dataset
We decided to work on a larger and simpler database: CelebA. We have reviewed not only the recommended GAN literature (https://paperswithcode.com/paper/progressive-growing-of-gans-for-improved ) but also VAEs and beta VAEs.

# Reproduction of results:
For the discriminative model run the https://github.com/Kata5/DeepLearning2021/blob/main/DeepLearning2021_Milestone1_2.ipynb
For the generative model run the https://github.com/Kata5/DeepLearning2021/blob/main/DeepLearning2021Milestone03.ipynb 

Please find the results of VAE parameter optimalization  in https://github.com/Kata5/DeepLearning2021/tree/main/VAE_results folder. 
Latents were discovered by hand and the best latents were achieved at https://github.com/Kata5/DeepLearning2021/blob/main/VAE_results/vae_best.pt (Which is uploaded to Google drive so as to be able to download it from the ipynb file as well.)

# Milestone 01

In the first milestone we prepared a balanced training / test / validation dataset for the later classificaton task with a splitting function of the database.
Some basic data discovery was also performed.


# Milestone 02

In this milestone
1. we built a discriminative model for learning the labels of the database - DeepLearning2021_Milestone1_2.ipynb
2. a deep generative model (i.e. a variational autencoder) was trained to learn the features of the faces - DeepLearning2021Milestone02.ipynb (due to hardware error the version on the deadline became corrupted; but having a check on the version before can prove that the model was working before the deadline as well)

The discriminatve model used transfer learning based on an Inception v3 model pretrained on imagenet and the last layers were trained on the database with an early stopping callback. With the first naive model a pecision of 90% was reached. (for more details see the documentation later)


# Milestone 03

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





