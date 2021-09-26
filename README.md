# ML_bestiary

## Project Overview

One of the major problems faced by independent video game developers is the difficulty of recruiting designers. Indeed, some do not have the funds to hire a full-time designer.
However, they have a crucial role in the success of a video game since for gamers, the bestiary is part of the quality guarantee of a good video game. It is in this context that
we decided to work on this project. Our goal is to create an artificial intelligence capable of generating new unseen monsters. This project can allow the creators of independent video games who do not have the budget to hire designers to have monsters directly generated from an AI (or at least a designer could use these images to make different monsters).

Please find below a little teaser of the project:

<a href="https://youtu.be/2b8fL_hNo0g
" target="_blank"><img src="https://github.com/gaetanlop/ML_bestiary_all/blob/main/Images/Image_for_screen.PNG" 
alt="ML_bestiary_YT" width="480" height="400" border="10" /></a>

[![Image for the youtube video](https://github.com/gaetanlop/ML_bestiary_all/blob/main/Images/Image_for_screen.PNG)](https://youtu.be/2b8fL_hNo0g)



After showing this teaser to different independent video game developers, we found out that many where interested in the technology. We plan to work on it more in order to improve it (see the parts on improveemnts). That's why we still did not release all the codes. 

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

**Data Cleaning:** In total we did three rounds of training. During the first one, we only remoed images that do not look like monsters (errors from the scraping). During the second one, we removed the datasets with a totally different style of images. For the last one, we created repositories with images of the same type (ie labeling of the images into classes: humans, drakes ...).

**Trying different architectures of Generative adversarial networks models:** The final architecture that we re using is the StyleGAN 2 ADA developed by NVidia researchers in october 2020 ([github](https://github.com/NVlabs/stylegan2-ada) | [paper](https://arxiv.org/pdf/2006.06676.pdf))

**Model Training:** Our best model was trained during three days using Google Colab Pro.

## Success of the project

One of the great successes of the project is to have obtained a neural network producing images of Pokémon of much better quality than what was previously done in towards data science in 2020 ([example of one article](https://towardsdatascience.com/how-to-create-unique-pok%C3%A9mon-using-gans-ea1cb6b6a5c2)).

In comparison, here is a selection of images obtained by our neural network:

PUT THE IMAGES

One of the achievements that we are also particularly proud of is that our image generator allows to generate new ideas of innovative Pokémons, it does not replace the artist but assists him in his creative process by proposing innovative forms to his imagination. Please find below an example of innovation of our image generator that can help the artist to innovate. The eyes of all the Pokemon existing today are placed on a smooth and more or less spherical surface of a head. On this picture we have a first eye on a smooth and more or less spherical surface but the second eye is placed on a hollow protuberance from which a limb comes out. Its shape and its location in relation to the first eye and the mouth allow us to accept this second eye while widening our vision of the properties of an eye and thus our artistic vision. Our GAN thus helps to stimulate artistic creativity.

PUT THE IMAGE

Apart from the concrete results that we were able to achieve, it is above all, the experience that we have gained during the realization of this project that makes it a real success. We now have a better understanding of the strengths and limitations of the GAN architecture and we are now better able to define the training data needed for a successful Image generation project. The main idea that we have incorporated throughout the project is the importance of the distribution of the GAN training data. A GAN allows to reproduce an image distribution of a certain population. If the sample used for training is not representative of the population, the GAN will not be able to reproduce it. For example, we found that if the images provided to GAN for its training could be separated into several groups, then during its training
the GAN will produce images that can also be increasingly separated into distinct groups.

## Errors of the project

Our goal of generating monsters for independent game developers is not yet reached. Indeed, the quality of humanoid and dragon monsters is still too low and the diversity of images is still too low for our model to be used as is by developers. The lack of homogeneity of the generated images of dragons and humanoids generated makes the original images too visible for a commercial exploitation. It is easy to distinguish the style of some games in the generated images. Below, a comparison between a generated image (left) and an image from the training dataset (right). The generated image, through its proportions, orientation and textures is too easily identifiable as being inspired by the Dofus style from which the second image comes.

PUT THE IMAGE WITH TWO DRAGONS

#### Some errors that we made:

* Leave duplicates or near duplicates in the training dataset. This makes it the appearance of duplicate training images in the generator more likely (called
collapse mode)
* Continue a training run for too long when the model has started to enter the collapse mode because it will not be able tocollapse mode because it will not be able to get out of it and will instead sink into this error as the training.
* Save the neural model too regularly. This slows down the training and overloads the storage space.

## Room for improvements

After several months of work on this project, we believe that there are still many ways to improve our models. In this section, I will outline the four most important areas for improvement.

* Increase the number of monsters that we have collected to create our Generative Adversarial Networks. Indeed, the number of monsters in our database is strongly correlated to the performance of the project. We noticed that one of the main difficulties in training a Generative Adversarial Network (GAN) is the access to the data. In our
case, we had to retrieve a large number of monsters to train our AI. This task is crucial since it is from these monsters that our model will create new ones. At
12000 different monsters from more than 30 different websites (from 30 different video games). In our opinion, we should go back to the scraping stage (one of the first steps in our road map) and continue to collect new monsters. This task is difficult since there is a finite number of images of video game monsters freely available on the Internet.
Thus, productivity decreases as we collect monsters: the more monsters we scrape, the less we have left on the Internet and therefore the harder it is to find them.

* Create databases that share a similar design style: This is the most difficult area of improvement. Indeed, collecting images of monsters is a good thing but it is still necessary that the drawing style of the artist is the same as the monsters we have already collected. To deal with this, we could for example hire a designer to create monsters of the same style.

* Our AI is not yet directly usable on the Internet by anyone. Our files are on our computers and unusable by someone who does not know how to do Data Science. One of the
improvement would be to deploy the project on the cloud, and make it possible for video game creators to use it as they wish. This is not a difficult task. But we haven't done it since we want to make a finished product available, not deploy a relatively bad product. We want to continue to collect new images and maybe succeed in animating
our monsters (this is the subject of the last point) before making our model available.

* The last area of improvement is the one that would bring the most value to our project. Several developers have expressed a strong interest in our project, but each time the same question they asked the same question: "is it possible for this artificial intelligence to animate the monsters it has created?". For example, is it possible for it to make dragons fly or humanoids walk? It is on this question that we would need to address after increasing the size of our database. The task is difficult but not impossible. Today, we are convinced that such an improvement on our project would drastically increase its value in the world of video games.


* First cleaning: only images that do not look like monsters
* Second cleaning: after the first gan model. Delete datasets wrong style images.
* Third cleaning: after the second gan model: CDCGAN. create repositories with images of same type. Labels.


## Next step: Learn GAN architecture (best articles about gans)

Best articles for the moment: 
https://bmachin.medium.com/training-a-heavy-metal-artwork-generator-using-stylegan2-ada-1c1e30bc1e9b

https://medium.com/swlh/training-gans-with-limited-data-22a7c8ffce78

* 01/04/2021: watched https://www.youtube.com/watch?v=DVXX0tmVyco&fbclid=IwAR2BuSJHF23X2cKcCVgvaizbVGiA6kkvTM4v1Vw9TWfaTnTepGv8wkOgIAU
* 03/04/2021: Traitement des monstres etc, avoir un avis sur le legal. 
Inspirer des dessinateurs de monstres avec des monstres qui existent déjà. Comment on se positionne la dessus. Sens niveau droit d’auteur. 
La création humaine a produit trop peu de variétés. Effort incrémentale entre l’existant et ce qu’il faut pour faire tourner un gan.
CCL du projet : Objectif quel chance on a de combler le gap. Si marche pas, on n’est pas dans les bonnes conditions etc …
Question : pk investir ? pk forcer cette démarche là ? Créer un  nouveau marché : on desintermédie qqn ?
Se demander ce que ça me dit sur la réalité. Dans quel monde ideal pour que ça arrive et pk j’ai envie de me projeter dans ce monde idéal.


## Training resultsd after 2 days using style gan 2 ada

* A lot of overfitted images. Really looks like thze training set. Should try interpolation to see if it understood data distribution of our monsters.
* Should also do another cleaning to remove duplicated images.
* Another idea is to use this 2 day model as a pretrained model for our others gans (will savr time)
* Try to implement a gan on all the monsters.

## Second training

* To counter overfitted images, removed duplicates and cleaned images of monsters that does not look like monsters.
* it seems that if we train the model too much some leakage since the proba increases.

## Third Training

Using clean images trained on 128 by 128 pixels. Used the complex architecture with a gamma of 30. Also I created the neural net without transfer learning. Results seems promising because way elss overfitting than before.

## Fourth training

Pokemon + new pokemon + nexomon + dofus pets

https://github.com/PokeAPI/sprites
