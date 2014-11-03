app_frontendtools
=================
## SSH
1. Lists the files in your .ssh directory, if they exist`
`ls -al ~/.ssh

2. Create public key
`ssh-keygen -t rsa -C "your_email@example.com"`

3. Choose filename
`Enter file in which to save the key (/c/Users/you/.ssh/id_rsa): /c/Users/win7/.ssh/easingthemes@github [Press enter]`

4. Skip passphrase 
`[Press enter]`

5. start the ssh-agent in the background
ssh-agent -s
# Agent pid 59566
`ssh-add ~/.ssh/easingthemes@github`

6. Copies the contents of the id_rsa.pub file to your clipboard
`clip < ~/.ssh/easingthemes@github.pub`

7. Add key to GIT Host (Github, Bitbucket ...)

8. Test connection
`ssh -T git@github.com`

--- on error
`eval ssh-agent -s` 
`ssh-add ~/.ssh/easingthemes@github`

## Git

1. Init git repo
`git init`

2. Add remote
`git remote add github git@github.com:easingthemes/app_frontendtools.git`

3. check remotes:
`git remote -v`

4. Add all files
`git add .`

5. Commit
`git commit -m "commit message"`

6. First push
`git push -u github master`
