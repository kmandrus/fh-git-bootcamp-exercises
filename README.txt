This repository is intended for use in the Git Tricks Bootcamp at Flatiron Health.


Instructions for Setup

    Always follow the instructions for a given exercise. The general instructions
    are included below for reference because the instructions for a given exercise 
    may not include the needed commands:

        1. Create a folder for the new exercise. Name it something descriptive.
               mkdir <folder_name>

        2. Navigate into your new folder, then clone the repo into it:
               cd <path/to/folder_name>
               git clone https://github.com/kmandrus/fh-git-bootcamp-exercises.git

        3. Create local versions of any branches needed for the exercise:
               git branch <branch_name>

        4. Set the local branches to track their remotes:
               git branch --set-upstream origin/<branch_name>

        5. Pull the remote branches into your local versions:
               git switch <branch_name>
               git pull
