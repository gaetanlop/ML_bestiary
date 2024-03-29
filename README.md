# ML_bestiary

[Link teaser](https://youtu.be/2b8fL_hNo0g)

## Project Overview

One of the major problems faced by independent video game developers is the difficulty of recruiting designers. Indeed, some do not have the funds to hire a full-time designer.
However, they have a crucial role in the success of a video game since, for gamers, the bestiary is part of the quality guarantee of a good video game. It is in this context that we decided to work on this project. Our goal is to create an `artificial intelligence capable of generating new unseen monsters`. This project can allow the creators of independent video games who do not have the budget to hire designers to have monsters directly generated from an AI (or at least a designer could use these images to make different monsters).

Please click on the image below to see the teaser of the project:

<a href="https://youtu.be/2b8fL_hNo0g
" target="_blank"><img src="https://github.com/gaetanlop/ML_bestiary_all/blob/main/Images/Image_for_screen.PNG" 
alt="ML_bestiary_YT" width="480" height="400" border="10" /></a>

After showing this teaser to different independent video game developers, we found out that many where interested in the technology. We plan to work on it more in order to improve it (see the parts on improvements). That's why we still did not release all the codes. You can still find some samples of the code that we used in the `GANs` folder and the `Scraping` folder.

#### Roadmap

Step | Beginning | Number of days 
--- | --- | ---
Validate the interest of our POC with developers | 12/04/2020 | 7 
How to get the data | 12/15/2020 | 20
Scrap the different monsters |12/26/2021 | 30
Database cleaning | 01/10/2021 | 20
Looking for the most suitable gan model | 02/04/2021 | 30
Cloud environment management | 03/11/2021 | 5
Model training | 03/21/2021 | 30
Results analysis | 04/20/2021 | 10
Creation of a teaser | 05/04/2021` | 7

**Scraping:** In total we scrapped over 12000 monsters on 30 different websites among which famous video games like MapleStory, DeadCells, Binding Of Isaac, Dofus, Chrono and more.

**Data Cleaning:** In total we did three rounds of training. During the first one, we only removed images that do not look like monsters (errors from the scraping). During the second one, we removed the datasets with a totally different style of images. For the last one, we created repositories with images of the same type (ie labeling of the images into classes: humans, drakes ...).
* First cleaning: only images that do not look like monsters.
* Second cleaning: after the first GAN model. Delete datasets wrong style images.
* Third cleaning: after the second GAN model: CDCGAN. create repositories with images of same type (Labeling).

**Trying different architectures of Generative adversarial networks models:** The final architecture that we used is the StyleGAN 2 ADA developed by NVidia researchers in october 2020 ([github](https://github.com/NVlabs/stylegan2-ada) | [paper](https://arxiv.org/pdf/2006.06676.pdf))

**Model Training:** Our best model was trained during three days using Google Colab Pro.

## Successes of the project

One of the great successes of the project is to have obtained a neural network producing images of Pokemon of much better quality than what was previously done in towards data science articles in 2020 ([example of one article](https://towardsdatascience.com/how-to-create-unique-pok%C3%A9mon-using-gans-ea1cb6b6a5c2)).

In comparison, here is a selection of images obtained by our `neural network`:

![alt text](https://github.com/gaetanlop/ML_bestiary_all/blob/main/Images/Image_1_github.PNG "IMG1")

One of the achievements that we are also particularly proud of is that our `image generator` allows to generate new ideas of innovative Pokemons, it does not replace the artist but assists him in his creative process by proposing innovative forms to his imagination. Please find below an example of innovation of our image generator that can help the artist to innovate. The eyes of all the Pokemon existing today are placed on a smooth and more or less spherical surface of a head. On this picture we have a first eye on a smooth and more or less spherical surface but the second eye is placed on a hollow protuberance from which a limb comes out. Its shape and its location in relation to the first eye and the mouth allow us to accept this second eye while widening our vision of the properties of an eye and thus our artistic vision. Thus, our GAN helps to stimulate `artistic creativity`.

![alt text](https://github.com/gaetanlop/ML_bestiary_all/blob/main/Images/Image_2_github.PNG "IMG2")

Apart from the concrete results that we were able to achieve, it is above all, the experience that I have gained during the realization of this project that makes it a real success. I now have a better understanding of the strengths and limitations of the GAN architecture and I am now better able to define the training data needed for a successful `Image generation project`. The main idea that we have incorporated throughout the project is the importance of the distribution of the GAN training data. As a GAN allows to reproduce an image distribution of a certain population, if the sample used for training is not representative of the population, the GAN will not be able to reproduce it. For example, we found out that if the images provided to the GAN for its training could be separated into several groups, then during its training the GAN will produce images that can also be increasingly separated into distinct groups.

## Errors of the project

Our goal of generating monsters for independent game developers is not yet reached. Indeed, the quality of humanoids and dragons monsters is still too low and the diversity of images is still too low for our model to be used as it is by developers. The lack of homogeneity of the generated images of dragons and humanoids makes the original images too recognizable for a commercial exploitation. It is easy to distinguish the style of some video games in the generated images. Below, a comparison between a generated image (left) and an image from the training dataset (right). The generated image, through its proportions, orientation and textures is too easily identifiable as being inspired by the Dofus style from which the second image comes.

![alt text](https://github.com/gaetanlop/ML_bestiary_all/blob/main/Images/Image_3_github.PNG "IMG3")

#### Some errors that we made:

* Leave duplicates or near duplicates in the training dataset. This makes it the appearance of duplicate training images in the generator more likely (called mode collapse).
* Continue a training run for too long when the model has started to enter the `mode collapse` because it will not be able to get out of it and will instead sink into this error as the training continues.
* Save the neural model too regularly. This slows down the training and overloads the storage space.

## Room for improvement

After several months of work on this project, we believe that there are still many ways to improve our models. In this section, I will outline the four most important areas of improvements.

* Increase the number of monsters that we have collected to create our Generative Adversarial Networks. Indeed, the number of monsters in our database is strongly correlated to the performance of the project. We noticed that one of the main difficulties in training a Generative Adversarial Network (GAN) is the access to the data. In our
case, we had to retrieve a large number of monsters to train our AI. This task is crucial since it is from these monsters that our model will create new ones. Based on the results, it seems that we should go back to the scraping stage (one of the first steps in our road map) and continue to collect new monsters. This task is difficult since there is a finite number of images of video game monsters freely available on the Internet. Thus, productivity decreases as we collect monsters: the more monsters we scrape, the less we have left on the Internet and therefore the harder it is to find them.

* Create databases that share a similar design style: This is the most difficult area of improvement. Indeed, collecting images of monsters is a good thing but it is still necessary that the drawing style of the artist is the same as the monsters we have already collected. To deal with this, we could for example hire a designer to create monsters of the same style.

* Our AI is not yet directly usable on the Internet by anyone. Our files are on our computers and unusable by someone who does not know how to do Data Science. One of the
improvement would be to deploy the project on the cloud, and make it possible for video game creators to use it as they wish. This is not a difficult task. But we haven't done it since we want to make a finished product available, not deploy a relatively bad product. We want to continue to collect new images and maybe succeed in animating
our monsters (this is the subject of the last point) before making our model available.

* The last area of improvement is the one that would bring the most value to our project. Several developers have expressed a strong interest in our project, but each time they asked the same question: 

> Is it possible for this artificial intelligence to animate the monsters it has created?. For example, is it possible for it to make dragons fly or humanoids walk? 

This is the question that we would need to address after increasing the size of our database. The task is difficult but not impossible. Today, we are convinced that such an improvement on our project would drastically increase its value in the world of video games.

## Code and Resources Used

**Style GAN 2 ADA github repo:** https://github.com/NVlabs/stylegan2-ada

**Style GAN 2 ADA paper:** https://arxiv.org/abs/2006.06676

**Style GAN 2 ADA training lessons:** https://www.youtube.com/watch?v=DVXX0tmVyco
