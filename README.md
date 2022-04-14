# Versioning-Introduction

## What is it about ?



## Git on my computer

First, you need to install the software : just dowload it for free on https://git-scm.com/downloads , and keep the default parameters while installing the software.

Second, some features are very useful to use your software properly, which you can adjust by entering commands in the Git Bash.

You will need to :

1. Tell who you are and what your email is, so that your modifications have an author, by entering the following commands :

                    $ git config --global user.name "Jane Doe"
                    $ git config --global user.email   

Note : the use of --global makes your command effective on all your repositories.


2. Define the location of your repository(ies), by locating or creating a file first, using the following command:

                    $ cd Documents
                    $ mkdir ProjetsBecode

(There you can check your actual location with pwd command).


To start a working area, you can then initiate a new repository using the following command :

                    $ git init

You can also copy an existing remote repository into your local workspace, e.g. something you want to collaborate on github, using :

                    $ git clone copyherethewebaddressoftherepo


## Move your files from local to global repositories

If you want to add a file and save it into you repository, you fill follow two steps.

1. You add it on the staging area (like a plane on a runway ran) using :

                    $ git add nameofmyfile

! Note that if you want to modify you file afterwards, you'll have to add it again (like you can't board new passengers when you're on the ran) !

2. Ready for departure ! Now you will save your file into your repository, where your name and time of modification will be recorded. You may also want to leave a comment with your update, by adding -m after the commit command :
                    $ git commit -m "I'm so proud I fixed this I leave"

##Share your files

                       fetch     Download objects and refs from another repository
                       pull      Fetch from and integrate with another repository or a local branch
                       push      Update remote refs along with associated objects

## tips

You can check the modifications using the following command :
                    $ git status




## En deux mots

```
C'est quoi le principe ? Git est un outil qui permet de faire évoluer un projet :
1. en gardant une visibilité sur les différents états successifs du projet ou des modifications apportées aux éléments qui le composent ;
2. en offrant la possibilité d'intégrer des modifications d'éléments de manière progressive au projet global ;
3. de manière fluide et rapide grâce à un hachage des données.

Github est une structure en ligne qui permet à chaque développeur/écriveur d'héberger à distance le pendant de son dépôt local dans Git.
