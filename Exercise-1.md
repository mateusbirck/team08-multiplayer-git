# Exercise one

In this first phase of the project, we want to get used to the push and pull cycle, without bothering with conflicts. To do this, everyone will be working on their own file.
But we still want to work on the same "code base" to experience how git behaves, so everyone on the team should be working on the `main` branch. (This repo has a `main` branch instead of the git-default `master`).

**Note:** We want to make sure that we are using `merge` and not `rebase` for this exercise. If you already have your machine configured to use `rebase` by default, you should override this setting for this exercise by running `git config pull.rebase false` inside the repository.

## Steps (for everyone)

1. Create a file in your team repo: `<my-name>.txt`
1. Add some information about yourself in this file, like e.g.
   * Your name
   * Your favourite colour
   * Your favourite food
  but do this in smaller individual changes.
1. For each change, make a Commit with a good commit message and push your changes to the teams remote repository.
1. Keep your local master up-to-date once your team is finished by using `git pull` (or `git fetch` followed my `git merge`)

Repeat step 2-4 adding even more info to you file, like maybe your favorite dad-jokes.

> Note: Remember that Git will only let you push changes if your local branch is up to date with what is on the remote. If others on your team have pushed changes in the mean time, your `git push` will get "rejected". Then you will have to update your local repository (as in step 4 above) and try to push again.

When this is completed, tell your instructor, so the games can continue 🎉
