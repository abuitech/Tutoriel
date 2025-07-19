# Logiciels à installer

## Visual Studio Code et ses extensions

* Visual Studio Code : https://code.visualstudio.com/

	* Raspberry Pi Pico de Raspberry Pi

	* CMake Tool de Microsoft



## CMake

* CMake version 3.xx ou plus : https://cmake.org/



## Git et quelques outils pratiques

* Git : https://git-scm.com/

* (optionel) TortoiseGit : https://tortoisegit.org/

* (optionel) Fork git : https://git-fork.com/



# Création d'un projet pour Pico

* Aller dans "Raspberry Pi Pico Project : Quick Access" en cliquant sur l'icon avec l'image du Pico dans la toolbar verticale à gauche

* Menu : General > New C/C++ Project

* Dans l'onglet "New Pico Project" (créé par le menu General > New C/C++ Project) :

	* Saisir le nom du projet dans "Name" de la section "Basic Settings"

	* Sélectionner le type de carte Pico, Pico 2, Pico W, etc

	* Saisir ou sélectionner (avec le bouton "Change") le chemin du répertoire

	* (optionel) Cocher "Console over UART" si on souhaite afficher des message sur une console TTY sur le PC via un adaptateur UART

	* (optionel) Cocher "Console over USB" si on souhaite afficher des message sur une console TTY sur le PC via USB

* Clique sur "Create" pour générer le projet



# Mettre le projet sous git et l'upload sur Github

* Initialiser le repository :

* Ouvrir un gitbash et aller dans le répertoir du projet

	* git init

	* git add *

	* git add .viscode/*

	* git add .gitignore

* Commit le projet

	* git commit -m "First commit"



* Créer un nouveau projet sur Github (https://github.com/)

	* Cliquer sur le bouton "New" (bouton vert sur le bandeau à gauche)

	* Saisir le nom du projet (le nom qu'on vient de donner au projet pico)

	* ne pas cocher "Add a README file" ni .gitignore



* Push le projet sur Github :

	* git remote add origin https://github.com/abuitech/Tutoriel.git

	* git branch -M main

	* git push -u origin main

__Note:__ si on n'avait créé un .gitignore ou un readme.md, la commande push échoue avec ce message d'erreur suivant

>! [rejected]        main -> main (fetch first)
>error: failed to push some refs to 'https://github.com/abuitech/Pico2Example.git'

dans ce cas, il faut utiliser l'option force (-f) : git push -u origin main

* Ajout d'un submodule (dans le répertoire courant) :

  	* git submodule add https://github.com/abuitech/PicoFATFS.git 

* Ajout d'un submodule dans un sous-répertoire spécifique :

  	* git submodule add https://github.com/abuitech/PicoFATFS.git path/to/directory

# Quelques liens utiles

* Getting started with Raspberry Pi Pico (installation et debugging) : https://datasheets.raspberrypi.com/pico/getting-started-with-pico.pdf
* Pico-series microcontrollers (documents de présentation et spécification des picos) : https://www.raspberrypi.com/documentation/microcontrollers/pico-series.html
* The C/C++ SDK : https://www.raspberrypi.com/documentation/microcontrollers/c_sdk.html
* Pico-examples (github officiels des exemples) : https://github.com/raspberrypi/pico-examples
* Pico-sdk (github officiel du sdk) : https://github.com/raspberrypi/pico-sdk
  
