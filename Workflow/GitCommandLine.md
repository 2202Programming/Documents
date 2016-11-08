# Git Command Line Interface

_v.0.1.0_

---

## Other Resources

Git is a very common and popular open source tool and becuase of this their are hundreads of online guides on how to use the software. Since it would take me a couple of years to write a book that contains all the features of git, I will just go over the basics.

#### Basic

* GitHub Help: GitHubs help page contains information a

#### In-Depth Documentations

## Basic Commands

After working on some files in a repository their are a few basics commands that you should know to be able to push your code. The average workflow looks something like this.

    1. Work on Project.
    2. `git add`
    3. `git commit` 
    4. `git push`

Let's start with `git add`, add _stages_ files onto your next commit, it is important to make sure to stage any file so it is included to your commit. Any file that you do not stage will not be deleted but will also not be shared with other when you push your code. To stage files use the git add command, and then type any files that you want to add. If you are sure that you want to stage all files in your repository the command `git add -A` will do so. (make sure A is capitolized)
