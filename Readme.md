# Logiciels à installer
## Visual Studio Code et ses extensions
    * Visual Studio Code : https://code.visualstudio.com/
        ** Raspberry Pi Pico de Raspberry Pi
        ** CMake Tool de Microsoft

## CMake
    * CMake version 3.xx ou plus : https://cmake.org/

## Git et quelques outils pratiques
    * Git : https://git-scm.com/
    * (optionel) TortoiseGit : https://tortoisegit.org/ 
    * (optionel) Fork git : https://git-fork.com/

## Création d'un projet pour Pico
    * Aller dans "Raspberry Pi Pico Project : Quick Access" en cliquant sur l'icon avec l'image du Pico dans la toolbar verticale à gauche
    * Menu : General > New C/C++ Project
    * Dans l'onglet "New Pico Project" (créé par le menu General > New C/C++ Project) :
        * Saisir le nom du projet dans "Name" de la section "Basic Settings"
        * Sélectionner le type de carte Pico, Pico 2, Pico W, etc
        * Saisir ou sélectionner (avec le bouton "Change") le chemin du répertoire
        * (optionel) Cocher "Console over UART" si on souhaite afficher des message sur une console TTY sur le PC via un adaptateur UART
        * (optionel) Cocher "Console over USB" si on souhaite afficher des message sur une console TTY sur le PC via USB
    * Clique sur "Create" pour générer le projet

## Mettre le projet sous git et l'upload sur Github
    * Initialiser le repository :
        ** Ouvrir un gitbash et aller dans le répertoir du projet
        ** git init
        ** git add *
        ** git add .viscode/*
        ** git add .gitignore
    * Commit le projet
        ** git commit -m "First commit"

    * Créer un nouveau projet sur Github (https://github.com/)
        ** Cliquer sur le bouton "New" (bouton vert sur le bandeau à gauche)
        ** Saisir le nom du projet (le nom qu'on vient de donner au projet pico)
        ** ne pas cocher "Add a README file" ni .gitignore

    * Push le projet sur Github :
        ** git remote add origin https://github.com/abuitech/Tutoriel.git
        ** git branch -M main
        ** git push -u origin main

