"# packages" 
How to upload large files to github:

https://medium.com/junior-dev/how-to-use-git-lfs-large-file-storage-to-push-large-files-to-github-41c8db1e2d65 


step 1: Download and Install Git-lfs ( Git Large File Storage ) from (here)[https://git-lfs.com/].

Step 2: Setup Git lfs for your user account with:
```
git lfs install.
```
Step 3: If you have already tried to commit large files and got the error then you must first undo the commit, use git reset — soft HEAD~1 otherwise ignore this step.
```
git reset --soft Head~1
```
Step 4: Select the file types that you want Git-lfs to manage using the command git lfs track “*.csv” , this creates a .gitattributes file.
```
git lfs track "<path/to/large/file.txt>"
```
Step 5: Add the .gitattributes file along with other files which need to be committed and push the changes.
```
git add .gitattributes <path\to\large\file.txt>
git commit -m "Adding large files to git lfs
git push
```