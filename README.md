# git-playground

📚 Learning and exploring Git.

---

This repository captures a _small_ amount of my personal notes, materials references, and code snippets about the Git
version control system.

## Notes

My personal favorite way to learn Git is to read the excellent _Pro Git_ book which is available to read online for free
at <https://git-scm.com/book/ru/v2>. I personally read it via <https://learning.oreilly.com/> or the O'Reilly app
because I have an O'Reilly subscription. 

## Submodules

I would like to learn about [Git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules). So, let's pick a project to
add to our Git repo as a submodule. Let's pick my own repo <https://github.com/dgroomes/dgroomes>. I added this
submodule by executing this command:

```
git submodule add https://github.com/dgroomes/dgroomes
``` 

When a Git repository is cloned with `git clone [url]` the operation does *not* clone sub-modules. It is necessary to
clone the sub-modules with an additional operation: `git submodule update --init` or to have done the initial clone of
the root repository with the option `--recurse-submodules`.

The repository is now under the directory `dgroomes/`.

(Wait I'm not sure this is true...) Annoyingly, when I do a `git pull` in this repository, it will pull the latest changes of the submodules. I don't want
to update my submodules when I do a `git pull` I only want to update my own clone of `git-playground` repository. Is
there a work around?
