# Repository: Bitbucket   
is a web-based version control repository hosting service owned by Atlassian, for source code and development projects that use either Mercurial (since launch) or Git (since October 2011) revision control systems.   
Bitbucket offers both commercial plans and free accounts. It offers free accounts with an unlimited number of private repositories (which can have up to five users in the case of free accounts) as of September 2010.      
  
  https://bitbucket.org  

   
# Repository: GitHub  
is a web-based hosting service for version control using Git. It is mostly used for computer code. It offers all of the distributed version control and source code management (SCM) functionality of Git as well as adding its own features. It provides access control and several collaboration features such as bug tracking, feature requests, task management, and wikis for every project. 
GitHub offers plans for enterprise, team, pro and free accounts which are commonly used to host open-source software projects.   
  
  https://github.com  


# Delete a Folder

## root@vultr:/home/HEAAN# git config --global user.name "John-L-Smith"
## root@vultr:/home/HEAAN# git config --global user.name               
John-L-Smith
## root@vultr:/home/HEAAN# git config --global core.editor vi
root@vultr:/home/HEAAN# git config --global core.editor   
vi
root@vultr:/home/HEAAN/FHE# ls
EXPERIENCE  HEAAN  HELR  HElib	README.md  iDASH2017  iDASH2018
root@vultr:/home/HEAAN/FHE# cd HEAAN
root@vultr:/home/HEAAN/FHE/HEAAN# ls
HEAAN
HEAAN.rar
README.md
root@vultr:/home/HEAAN/FHE/HEAAN# rm -r HEAAN
root@vultr:/home/HEAAN/FHE/HEAAN# rm HEAAN.rar
## root@vultr:/home/HEAAN/FHE/HEAAN# git rm -r --cached HEAAN
## root@vultr:/home/HEAAN/FHE/HEAAN# git rm -r --cached HEAAN.rar
## root@vultr:/home/HEAAN/FHE/HEAAN# git commit -m 'delete HEAAN for it being a old version'
## root@vultr:/home/HEAAN/FHE/HEAAN# git push origin master
Username for 'https://github.com': John-L-Smith
Password for 'https://John-L-Smith@github.com': 

# Add a Folder
## root@vultr:/home/HEAAN/FHE/HEAAN# git clone https://github.com/snucrypto/HEAAN
root@vultr:/home/HEAAN/FHE/HEAAN# ls
HEAAN
README.md
........
## root@vultr:/home/HEAAN/FHE/HEAAN# git add HEAAN/
## root@vultr:/home/HEAAN/FHE/HEAAN# git commit -m 'upload the newest HEAAN library with its .zip file 20181206'
## root@vultr:/home/HEAAN/FHE/HEAAN# git push origin master
Username for 'https://github.com': John-L-Smith
Password for 'https://John-L-Smith@github.com': 
root@vultr:/home/HEAAN/FHE/HEAAN# zip -r HEAAN.zip HEAAN
root@vultr:/home/HEAAN/FHE/HEAAN# ls
HEAAN
HEAAN.zip
README.md
........
## root@vultr:/home/HEAAN/FHE/HEAAN# git add HEAAN.zip
## root@vultr:/home/HEAAN/FHE/HEAAN# git commit -m 'upload the newest HEAAN library with its .zip file 20181206'
## root@vultr:/home/HEAAN/FHE/HEAAN# git push origin master
Username for 'https://github.com': John-L-Smith
Password for 'https://John-L-Smith@github.com': 
Counting objects: 4, done.
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 921.01 KiB | 0 bytes/s, done.
Total 4 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/John-L-Smith/FHE
   b5b509b..f784ad9  master -> master

# Recover a just deleted file
## root@vultr:/home# git reset --hard HEAD^
HEAD is now at 7f7274f Update 4U.htm
## root@vultr:/home# ls
4U.htm ... ... img
## root@vultr:/home# git commit -m 'git reset --hard HEAD^ (4U.htm)'
On branch master
Your branch is behind 'origin/master' by 1 commit, and can be fast-forwarded.
  (use "git pull" to update your local branch)
nothing to commit, working tree clean
## root@vultr:/home/github.io# git add 4U.htm
## root@vultr:/home/github.io# git commit -m 'git reset the deleted file 4U.htm'
## root@vultr:/home/github.io# git push origin master
 ! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'https://github.com'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
## root@vultr:/home# git push  -f origin master
 + 6e5015d...7f7274f master -> master (forced update)

