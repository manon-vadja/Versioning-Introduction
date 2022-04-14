# Versioning-Introduction

## What is it about ? 

## Git on my computer 

First, you need to install the software : just dowload it for free on 

Second - and that is very important ! some features are very useful to use your software properly, which you can adjust by entering commands in the Git Bash. 

You will need to : 
1. define the location of your repository(ies), by locating or creating a file first, and then initiating your new repository :

                    $ cd Documents
                    $ mkdir ProjetsBecode

There you can check your actual location with pwd command ! 
You can then initiate a new repository using the following command : 

                    $ git init



2. tell who you are and what your email is, so that your modifications have an author with
                                                 $ git config --global user.name "manon vadja" 
                                                 

Note : the use of --global makes your command effective on all your repositories. 


## En deux mots

```
C'est quoi le principe ? Git est un outil qui permet de faire évoluer un projet : 
1. en gardant une visibilité sur les différents états successifs du projet ou des modifications apportées aux éléments qui le composent ;
2. en offrant la possibilité d'intégrer des modifications d'éléments de manière progressive au projet global ;
3. de manière fluide et rapide grâce à un hachage des données.

Github est une structure en ligne qui permet à chaque développeur/écriveur d'héberger à distance le pendant de son dépôt local dans Git. 
