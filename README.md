# gitTest
This project is only build to do some exercise on Git command

#first command
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

Username for 'https://github.com': ChenCheress
Password for 'https://Cheress@github.com':

operation history:
I have a project named "gitTest" and has a master branch
1.create a branch "branchA" on bitbucket
2.Run --> git checkout -b "branchA" //it means create a local branch "branchA", it doesn't from the remote "branchA"
3.Do some changes and save at the local "branchA"
4.Run --> git add .
5.Run --> git commit -m "some description"
6.Run --> git push
  #here I got an error:
  fatal: The current branch dev has no upstream branch.
  To push the current branch and set the remote as upstream, use

  git push --set-upstream origin dev
7.When run command: git push --set-upstream origin dev, the changes was commit and been pushed to the origin dev branch, not "branchA"

#-------------------------Find my error in step2-------------------#

git checkout -b "branchA"  ---> git checkout "branchA"

git checkout -b "branchA"
//it means create a local branch "branchA" and switch to this local branch, it doesn't from the remote "branchA"

git checkout "branchA"
//it means checkout the remote branch "branchA", and won't lose the remote destidation, if you don't have a remote branch "branchA", then you need to create an connection from your local branch to the remote branchA

#---------------------------Resolution -----------------------------#


Run --> git push -u origin bugfix/branch

Branch bugfix/branch set up to track remote branch bugfix/branch from origin.

To https://github.com/ChenCheress/gitTest.git
 * [new branch]      bugfix/branch -> bugfix/branch
