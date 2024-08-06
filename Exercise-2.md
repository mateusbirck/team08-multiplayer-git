# Exercise two

In this part of the "project" we actively want to enjoy the fun and pain of getting and resolving conflicts. To do this, we will now all be working on the same file.

**Note:** We want to make sure that we are using `merge` and not `rebase` for this exercise. If you already have your machine configured to use `rebase` by default, you should override this setting for this exercise by running `git config pull.rebase false` inside the repository.

* As a team, collaborate on building an ASCII art house in a file named exactly `house.txt`
* The house obviously needs features like:
  * Walls
  * A roof
  * A door
  * Windows
  * Maybe a chimney
  * A garden or yard?
  * Any extras you want

* As in any good software project, limit yourself to one feature per commit. Remember good commit messages so your team mates know which features you added. Remember to share your changes every time.

* If you get a merge conflict, you will have to resolve this. Remember to enjoy this process :smile: and the added bonus that conflict markers look a bit like ascii-art.

* Continue improving your house until the instructor introduces the next part of the exercise. Each team member should have contributed a few improvements to the house, and resolved at least one conflict.

## Tip

To resolve a conflict:

* edit the conflicted files, leaving them in their desired state
* stage each fixed file `git add <file>`
* finalize the merge commit with `git merge --continue`
