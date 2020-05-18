# List of all the git commands used in this exercise 

### Step 1 (Start new Project)
1. Created and switched to folder project1
2. Initialize git using ---> git init
3. Added README.md and commit the changes on master branch. Commands used
   - git add .  (to add untraked README file)
   - git commit -m "Project started"

### Step 2 (Create new branch and push changes to remote)
1. Created and checkout to new brach "staging" ---> git checkout -b staging
2. Added new file test1 with content "Added new file test1 in Project1" 
3. Added and commit the changes --> git commit -a -m "This is first commit"
4. Push it to remote ---> git push -u origin HEAD

### Step 3 (Clone the repo in project2)
1. Created and switched to new folder project2
2. Clone the repo using ---> git clone < SSH key >
3. Go to test_project folder

### Step 4 (Add new commit on staging branch from Project2 and push to remote)
1. Added new content in test1 file "Added content in file test1 from Project2"
2. Checkout to staging branch ---> git checkout staging
2. Commit the changes  ----> git commit -a -m "This is my second commit"
3. Push to remote ---> git push -u origin HEAD

### Step 5 (Add new commit on staging brach from Project1 and tried to push to remote)
1. Added new content in test1 file "Added cntent in file from Project1"
2. Commit the changes ----> git commit -a -m "This is my third commit"
3. Tried to push to remote ---> git push origin HEAD
4. Git failed to push the changes because remote contains some changes that do not have locally

### Step 6 (Reset the commit, then pull the changes from remote and then repeat the step 5)
- Reset the commit ---> git reset --hard HEAD~1
- Pulled the changes from remote ---> git pull
- Repeat step 5 to add new commit to remote.
- This time git successfully pushed the changes to remote.


### Step 7 (merge staging into master)
1. Go to master branch --->  git checkout master
2. merge the staging into master ---> git merge staging
3. There is no merge conflicts so git successfully merge the staging into master


### Step 8 (Create new testing branch create new commit)
1. Created and checkout to testing branch ---> git checkout -b testing
2. Added new line in test file "A is alphabet"
3. Commit the changes ----> git commit -a -m "This commit is on testing branch"

### Step 9 (Change "A is alphabet" to "B is alphabet" and add new commit on testing branch )
1. Updated test file to convert "A is alphabet" to "B is alphabet"
2. Commit the changes ----> git commit -a -m "new commit on testing branch to convert A -> B"

### Step 10 (Repeat step 9 seven times)
1. Repeat step 9 seven times and each time increment alphabet ('A' to 'B', 'B' to 'C' ......)

### Step 11 (Push the changes to remote)
1. git push -u origin HEAD

### Step 12 (Checkout to master and add some new commits on it)
1. checkout to master ---> git checkout master
2. Added new line to testfile "1 is number"
3. commit the changes --> git commit -a -m "new commit on master to add 1 is a number"

### Step 13 (Repeat step 12 seven times)
1. Repeat step 12 seven times and each time increment number (1 to 2, 2 to 3 ....)

### Step 14 (Push the changes to remote)
1. git push origin HEAD

### Step 15 (Rebase testing with master locally)
1. checkout to testing
2. Rebase testing with master ---> git rebase master
3. While rebasing the testing with the master, git forced us to resolve the conflict of the testing branch with every commit of the master branch.
4. Master branch remains the same.

### Step 16 (Go to project 2 and merge testing into master)
1. go to project2 folder
2. pull the changes of remote ---> git pull
3. go to master ----> git checkout master
4. merge the testing into master --> git merge testing
5. Now the master branch has all the commits of testing branch and one extra merge commit( where I fixed the merge conflcts)
6. Testing branch remains the same.







