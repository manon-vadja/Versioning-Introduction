### my manual


## Git on my computer

First, you need to install the software : just dowload it for free on https://git-scm.com/downloads , and keep the default parameters while installing the software. Be sure to install as well the GitHub CLI, that will allow you another range of interactions with your github repos : 
 `sudo apt install gh `

Second, some features are very useful to use your software properly, which you can adjust by entering commands in the Git Bash.

You will need to :

1. Tell who you are and what your email is, so that your modifications have an author, by entering the following commands :
```
  $ git config --global user.name "Jane Doe"
  $ git config --global user.email   
```
Note : the use of --global makes your command effective on all your repositories.


2. Define the location of your repository(ies), by locating or creating a file first, using the following command:

                    $ cd Documents
                    $ mkdir ProjetsBecode

(There you can check your actual location with pwd command).

Once you are located in a proper file, you can start a working area. For that, you can initiate a new repository using the following command :

                    $ git init

You can also copy an existing remote repository into your local workspace using :

                    $ git clone copyherethewebaddressoftherepo



## Move your files from local to global repositories, and back ! 

If you want to add a file and save it into you repository, you fill follow two steps.

1. You add it on the staging area (like a plane on a runway ran) using :
`  $ git add nameofmyfile`

! Note that if you want to modify you file afterwards, you'll have to add it again (like you can't board new passengers when you're on the ran) !

2. Ready for departure ! Now you will save your file into your repository, where your name and time of modification will be recorded. You may also want to leave a comment with your update, by adding -m after the commit command :
`   $ git commit -m "I'm so proud I fixed this that I leave a comment about it" `

Of course, you will want to keep your local and remote repos up-to-date with the latest modifications. To do so, the pull and push commands will respectively send and call the repo including the latest commits : 

```
$ git pull copyherethewebaddressoftherepo
$ git push copyherethesameaddressoftherepo

```
You can also use the "fetch" command, instead of the pull command ; they are not totally the same, though they can be used in a similar way : 

fetch     Download objects and refs from another repository
pull      Fetch from and integrate with another repository or a local branch
push      Update remote refs along with associated objects

To see the links existing between your repo and another remote repo, you might use :
`$ git remote -v `

That will display the name of the remote repo linked to your current and properly gitted work directory. 



## Share and version your files

Now that we know how to get and send files from and to a remote repository, let's talk about the essential core of got, without which it wouldn't be more than a mere dropbox (sorry kitty) : versioning ! 
> Git 1) keeps in memory the history of your repo and 2) duplicate it in order to keep on working on a part of your project on a parallel workspace (called a "branch"). 

How did we do before, huh ? So we have our "main" workspace, the best and first one, stable and waterproofed, and around it "branches" on which you can test-and-fail-or-not improvements, experimentations, new features, etc - and eventually *merge* these new features to your good old main trunk. 

The mere command "branch" will show you (with the *) which branch you are actually working in : 
```
$ git branch 
*main
```
You can create a new branch by adding its name to the command : 
`$ git branch mynewworkspaceisabranch`

Or you can create AND locate in your new branch using
`$ git checkout -b "nameofthebranch" `

And relocate to the main branch afterwards if you want to (and back etc.) just typing:  
`$ git checkout main`



> So, that is how to add branches to your worktree. To keep your remote repo up-to-date with that new state of being, just commit and push! Or pull, if you created the branch on your remote repo and you want to update your local one, of course.  



Eventually, you will want to integrate your parallel work into your main workspace, aka "merge" your branch to your "main". 
To do so, first you will have to locate in the workspace you want to update, then you will merge your branch, as following : 
```
$ git checkout main
$ git merge mybranchthatworkssowell
```

## tips

You can check the modifications in your working area using the following command :
                    $ git status






## En deux mots

C'est quoi le principe ? Git est un outil qui permet de faire évoluer un projet :
1. en gardant une visibilité sur les différents états successifs du projet ou des modifications apportées aux éléments qui le composent ;
2. en offrant la possibilité d'intégrer des modifications d'éléments de manière progressive au projet global ;
3. de manière fluide et rapide grâce à un hachage des données.

Github est une structure en ligne qui permet à chaque développeur/écriveur d'héberger à distance le pendant de son dépôt local dans Git.


## Further notes 

### Add a local repo to GitHub using CLI

1. Gititialize your folder ! Locate into the root directory, and initialize your directory as a Git repo :
    git init -b main

2. Stage and commit all the files contained in the folder
    git add .
    git commit -m "contenu initial"
        
## bonnes pratiques

Sensitive data can be removed from a repo using 
    git filter-repo

