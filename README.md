# ML_bestiary

* This repo contains all the datasets that we scrapped. It is use to create specific datasets. Do not remove anything from this repo.

## Web scraping websites

* Binding of Isaac: https://bindingofisaacrebirth.gamepedia.com/Bestiary (300 images)
* Deadcells: https://deadcells.gamepedia.com/Enemies (75 images)
* Children of Morta: https://childrenofmorta.gamepedia.com/Enemies (42 images)
* Enter the Gungeon: https://enterthegungeon.gamepedia.com/Cult_of_the_Gundead (105 images)
* Nexomon: https://pqube.co.uk/nexomon-extinction/category/nexopedia/page/3/ (350 images)
* Pokemon: https://www.kaggle.com/kvpratama/pokemon-images-dataset  (800 images)
* Dofus: https://www.dofus.com/fr/mmorpg/encyclopedie/monstres (1400 images)
* MapleStory: https://strategywiki.org/wiki/MapleStory/Bosses (1800 images)
* Ragnarok: https://ratemyserver.net/index.php?page=mob_db (700 images)
* Castaway: https://castaway.fandom.com/wiki/List_of_Monsters_(Castaway_1_%26_2)?fbclid=IwAR2616HP_h2Vu85SQ-lirU67M60rvd74kglM2WwDjiEVv6f5dGBT_hu1TpE (17 images)
* Moonlighter: https://moonlighter.gamepedia.com/Enemies (60 images)
* Dragon Quest: https://dragonquest.fandom.com/wiki/List_of_monsters_in_Dragon_Quest_XI_Bestiary (1200 images)
* Graveyardkeeper: https://graveyardkeeper.gamepedia.com/Monsters (12 images)
* Dontstarve: https://dontstarve.fandom.com/wiki/Monster (80 images)
* Dredmor: https://dungeonsofdredmor.fandom.com/wiki/Enemies (64 images)
* Bit-heroes: https://bit-heroes-france.fandom.com/fr/wiki/Familiers (100 images)
* Chrono: https://chrono.fandom.com/wiki/List_of_Chrono_Trigger_enemies?fbclid=IwAR2twdwGb4JQ3ZTk58Yjkj22H6rA5sbMs-En76o3rcdAZT0frN4Wt5-1cTw (130 images)

Total images scrapped: 12000 images on 16 websites

## Next step: Learn GAN architecture

* 11/01: Generator/ Discriminator Theory learnt
* 12/01: Made one example on Mnist but not working
* 14/01: DCGAN on mnist worked 50 epochs
* 15/01: DCGAN on fashion worked for 50 epochs
* 16/01: Generation of monsters from Binding of Isaac. Not too bad but problem of overfitting
* 17/01: dofus scraping done
* 17/01: Ragnarok scraping done
* 18/01: MapleStory scraping done
* 19/01: Moonlighter scraping done
* 20/01: Dragon QUest scraping done
* 24/01: Graveyardkeep scraping done
* 25/01: Dontstarve scraping Done
* Failed to do exiled kingdom scraping multiple times
* 26/01 : Bit-heroes and dredmor scraping
* 27/01 : Chrono scraping
* 28/01 : CLEANING



* 29/01 : Faire rosprites
* 01/02 : Reunion pour le Data Cleaning, on clean sommairement d'ici le 6 puis commencement du GAN.
* Ajouter tous les sites scrappés à la liste

* Semaine du 02/02: Sprint pour le cleaning de la bdd. Cleaning sommaire. Stratégie: tester avec le plus d'images possibles.
* First cleaning: only images that do not look like monsters
* Second cleaning: after the first gan model. Delete datasets wrong style images.
* Third cleaning: after the second gan model: CDCGAN. create repositories with images of same type. Labels.

* I need to put all the databases on this github repo and update the number of images and websites scrapped!





