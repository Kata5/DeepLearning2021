# DeepLearning2021

Welcome to the assignment of ~~Sándor Gregus (YRVTLZ)~~ (unfortunately quit), Katalin Ócsai (EW9A0Z), and Mátyás Prechl (JR4JDJ)!

# Contributions
* Sándor Gregus would have been responsible for milestone 2 but he quitted on the 24/November without any contribution to the project.
* Mátyás Prechl would have been responsible for the visualization of the hiperparameter tuning but he could not contribute to MileStone3 at all.
* Katalin Ócsai contributed to all the three milestones (as it can be seen in list of commits).

** splitting function for test, training, validation data, some data discovery for the discriminative model
** the entire solution for generative model (VAE), latent traversal
** parameter optimalistion of VAE
** finding meaningful dimensions of VAE according to the laten traversal
** entire documentation (documentation.pdf, future planes,  belogs to her (as finally she was alone in mileStone 3)

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
* 16th dimension seems to code the factor for the color of the hair
* 26.th dimension seems to code the existence of bangs
* 2nd dimension seems to code the rotation of the face
* 12th dimension seem to code the width of face
* 9th dimension seems to code thickness of hair (not completely disentengled from hair color..)

1.) Color of the hair:

![image](https://user-images.githubusercontent.com/24832770/145726224-f1d19a1a-6cea-4af0-a45d-5f15bd8e2ece.png)
![image](https://user-images.githubusercontent.com/24832770/145726256-e8d1d576-f2fc-4fa6-b45c-0e9f68f2f2d7.png)


2.) The existence of bangs

![image](https://user-images.githubusercontent.com/24832770/145726278-612137db-7be9-4f6b-bbe3-4b49f56af677.png)
![image](https://user-images.githubusercontent.com/24832770/145726306-282c8d1f-4359-43da-ba48-30054c937825.png)


3.) The rotation of the face

![image](https://user-images.githubusercontent.com/24832770/145726362-2a7f2a90-b83d-4802-8517-bfe84554b3b5.png)

4.) The thickness of hair

![image](https://user-images.githubusercontent.com/24832770/145726458-57b7d5f9-36cb-44ed-b729-75aa4b176118.png)

5.) the width of face(being fat)

![image](https://user-images.githubusercontent.com/24832770/145726480-76172ed3-c35d-49a9-8cf8-96553c61507e.png)


# Documentation
Please find the details in https://github.com/Kata5/DeepLearning2021/blob/main/Documentation2.pdf



