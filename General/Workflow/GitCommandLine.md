# Git Command Line Interface

_v.0.1.0_

---

## Other Resources

Git is a very common and popular open source tool and becuase of this their are hundreads of online guides on how to use the software.
Some pretty clear documentation for how to use the command line with git is available here: https://stackoverflow.com/documentation/git/218/getting-started-with-git#t=201706230435440234249

#### In-Depth Documentations

## Basic Commands

After working on some files in a repository there are a few basics commands that you should know to be able to push your code. The average workflow looks something like this:

    1. Work on Project.
    2. `git add <your files>`
    3. `git commit -m "message describing what you did"` 
    4. `git push`

Let's start with `git add`, add _stages_ files onto your next commit, it is important to make sure to stage any file whose changes you want to save so it is included to your commit. Any file that you do not stage will not be deleted but will also not be shared with other when you push your code. To stage files use the git add command, and then type any files that you want to add. If you are sure that you want to stage all files in your repository the command `git add -A` will do so. (make sure A is capitolized)
