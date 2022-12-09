Git Tricks Bootcamp:  Rebasing Examples

This repository is intended for use in the Git Tricks Bootcamp. 

Instructions for setup: 
    1. Clone the repo onto your local machine 
       (git clone https://github.com/kmandrus/gitbc-interactive-rebase.git)
    2. Create local versions of the scuba_store_squash_ff and first_aid_no_ff 
       branches (git checkout -b <branch_name>)
    3. Set the local branches to track their remotes 
       (git branch --set-upstream origin/<branch_name>)
    4. Pull in the remote branches to your local versions (git pull). Remember,
       to switch to the branch before pulling!

This repo contains two files: 
    shopping_list.txt - fictional shopping list for a scuba trip
    first_aid_supplies.txt - first aid supplies for a scuba trip
and three branches: 
    main 
    first_aid_no_ff - intended to be merged as is with a merge commit 
    scuba_store_squash_ff - intended to be squashed, rebased, and fast-forward merged 

First, take some time to investigate the contents of each branch and their git histories.
When you're ready, to start the exercise, do the following: 

    1. Merge the 'first_aid_no_ff' branch into main as is. If done successfully, there 
       should be a merge commit and no conflicts. Investigate main's new history using
       'git log --graph --oneline'. What is this command showing you? Why is the
       'add sun protection' commit mixed in with the 'first_aid_no_ff' branch's commits?

    2. Switch to the 'scuba_shopping' branch and perform a standard rebase against the 
       local main branch, like so: 'git rebase main'. Resolve and merge conflicts as they
       arise. Opt to keep everything on the shopping-list from both branches. Examine the
       branch's new history to make sure it looks right.

    3. Now start an interactive rebase using 'git rebase main -i'. This will allow you to
       edit commit messages, squash commits, and much more. Read the instructions that pop
       up to squash the commits on your branch together and change your new squashed commit's
       message to something more appropriate. Double check the branch's history to ensure
       everything went smoothly. 

       Note: we could have combined steps (2) and (3) by running 'git rebase main -i' straight
       away. We split it into two steps to keep the process simple.

    4. Finally, switch back to main and merge in 'scuba_store_squash_ff' using this command:
       'git merge scuba_store_squash_ff --ff-only'. While git merge will do a fast-forward
       commit whenever possibly by default, specifying the '--ff-only' flag will cause the
       merge to fail if it's unable to fast-forward merge. 

       Investigate main's history one last time. Do you prefer the history created by a 
       squashed, fast-forward merge or a regular merge better? Which workflow do you prefer?

    Congrats! You now know how to perform a squashed, fast-forward merge.
