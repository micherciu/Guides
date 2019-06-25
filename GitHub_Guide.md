# Guide of using CLI commands for GitHub 
<p align="center">
*what I commonly use*
</p>

0. To clone a repository just do:

**`# git clone "the_repository_you_are_intereseted_for"`**

1. Create a branch

**`# git checkout -b "the_new_branch"`**

2. Delete a specific branch
> !!! please note that you have to be in another branch.

**`# git branch -d "the_specific_branch"`**

3. Switching the branch

**`# git checkout "switch_the_branch"`**

4. Informations about the commits

**`# git log`**

5. Check the current status of local working directory 
> will show you which files are staged, unstaged, and untracked

**`# git status`**

6. Go to a specific tag (pointing out to a specific version release)

**`# git tag`**

7. Push modification to the remote repository 
> this is used just for the first time pushing

**`# git push -u origin master`**

> this can be used for the next changes

**`# git push`**

> this can be used to force to update the remote repository

**`# git push -f origin master `**

8. Add a file to the staging area

**`# git add "the_file_you_want_to_be_tracked"`**

9. Append a message to the modification/s

**`# git commit -m "commit_details"`**

10. Copy up to a specific commit to a branch

**`# git branch "the_branch" "the_hash_commit_(SHA)"`**

11. Bring those changes to the main branch

**`# git branch -f master "your_new_temp_branch"`**

...
