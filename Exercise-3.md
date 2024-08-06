# Exercise 3

In this phase of the project, we want to switch from `merge` to `rebase` when integrating our own changes with those of our team mates.

You can do this manually by running `git pull --rebase` instead of a regular `git pull`. This will invoke the usual *fetch*, and then rebase your local changes on top of the fetched changes instead of doing the normal *merge*.

You will however probably soon forget to add the `--rebase` switch, so instead we want to configure Git to do this automatically.

Run: `git config pull.rebase true` in your repository to configure *rebase* as the default strategy for this repo, or `git config --global pull.rebase true` if you want to adopt this behaviour for all repositories tht you work with.

## Development

Once you have configured *rebase*, continue working on the house. You will probably keep getting conflicts, but as you have learned, the "workflow" for resolving them is now a bit different.

When a conflict occurs, the rebase is interrupted. 

To resolve the conflict:

* edit the conflicted files, leaving them in their desired state
* stage each fixed file `git add <file>`
* continue the rebase with `git rebase --continue`
* If you are rebasing multiple commits, you might get additional conflicts. If so, repeat the above steps until you are all done.

In case you mess up, you can do a `git rebase --abort` which will clean up everything and put you back where you were before the rebase so you can start over.
