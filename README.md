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

Once you are located in a proper file, you can start a working area. For that, you can initiate a new repository using the following command :

                    $ git init

You can also copy an existing remote repository into your local workspace using :

                    $ git clone copyherethewebaddressoftherepo

If you are collaborating with other people, you may prefer to use the pull command, which will update the repository you cloned before with other people's commits :

                    $ git pull copyherethewebaddressoftherepo


## Working, staging area and committing your work on you repo

If you want to add a file you've worked on and save it into your repository, you fill follow two steps.

1. You need to index your file, i.e. add it on the staging area (like a plane on a runway ran) using :

                    $ git add nameofmyfile

! Note that if you want to modify you file afterwards, you'll have to add it again (like you can't board new passengers when you're on the ran) !

If you need to add more than one file, you can do it using different options :

                    $ git add file1 file 2 file345
                    
or                  $ git add parentfolderbecauseIwantallthesefiles

or                  $ git add *    

that will search and add all modified files.

2. Ready for departure ! Now you will save your index into your repository, where your name and time of modification will be recorded. Please note that the default settings requires you to leave a comment (the "message") with your update, by adding -m after the commit command and your message bewteen quotation marks :

                    $ git commit -m "mymessage"

That's it !

## Share your files

### Connecting to distant repositories

To manage connections to remote repos ("tracked" repos), you will use first the 'remote'command. To make a new link, you will use :
                    $ git remote add typeheretheadressoftherepo
To display the repos you already track, use remote command alone or with -v to display the addresses of the repos :
                    $ git remote -v

to display the url of your links too.                     
  vous permet de créer, d'afficher et de supprimer

                       fetch     Download objects and refs from another repository
                       pull      Fetch from and integrate with another repository or a local branch
                       push      Update remote refs along with associated objects

### Find the rights directions

Instead of mentioning the https URL of the repo you want to link to, which will require a login, you can use an SSH key. To use it, you need to create on your own computer a key, that you will refer to github, so every connection you make later will be identified as yours / coming from you computer.

To create that key, type the following command on your gitbash :
                    ssh-keygen -o
You will be able to specify (or not) where you want to store your key and create a password - and your computer will generate a beautiful key. Afterwards, what you need to do is display your public key by (e.g)
                    cat C:/Users/Utilisateur/.ssh/id_rsa.pub
... and copy it into your SSH keys in your personal settings on Github.  




## Several tips
! There is a very useful index of git commands on https://git-scm.com/docs !

You can check the modifications in your working area using the following command :
                    $ git status

You can open a new branch in a directory using
                    $ git checkout -b "nameofthebranch"




## En deux mots

```
C'est quoi le principe ? Git est un outil qui permet de faire évoluer un projet :
1. en gardant une visibilité sur les différents états successifs du projet ou des modifications apportées aux éléments qui le composent ;
2. en offrant la possibilité d'intégrer des modifications d'éléments de manière progressive au projet global ;
3. de manière fluide et rapide grâce à un hachage des données.

Github est une structure en ligne qui permet à chaque développeur/écriveur d'héberger à distance le pendant de son dépôt local dans Git.
