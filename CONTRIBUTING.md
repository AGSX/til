# Contributing

1. Make a new branch on your git repository
2. Start making a new post by copying the `post-template.md.sample` file and removing `.sample` from the end of the filename.
3. Start writing on that new file on what you've learned for today
3. Push the new branch to the remote repository of this project. Note: Before pushing the new branch, make sure that you've updated your branch with master:

   ```
   (your-branch) $ git checkout master
   (master)      $ git pull origin master
   (your-branch) $ git checkout your-branch
   (your-branch) $ git rebase master
   ```   
4. Create a new pull request in Github merging your new branch to master. 
5. Grab cookies as it gets merged to master by the maintainer
