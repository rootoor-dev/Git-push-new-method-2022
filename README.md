# Git-push-new-method-2022
Tutorial to push project on remote project using GIT and GITHUB !

# Github CLI with token authentication

> **GIT INFO**  
git config user.name "john-eod"  
git config user.email "john-eod@ivorycoast.ci"  

Since August 13, 2021, support for password authentication was removed on github.  
So we now use **token to push** some code to GitHub.  

## Initialize and push from local to github (online)
- Import from an existing online project  
- First create an online project on github. Let's call it "projectrepo".  
- Download it to our computer from a remote network  
- Using *git clone, curl, wget* are some possible ways. 
- see token generating steps

## Generate Token 
- Create an expirable **token** (preferably) here: [https://github.com/settings/tokens/new](https://github.com/settings/tokens/new)  
- check permissions such as :  
   - **repos**  
   - **read:repo_hook**  
   - **delete_repo**  
  
[**STEPS**]

```sh 

# git clone a remote network repo or git init a local project
Username for 'https://github.com': john-eod
Password for 'https://john-eod@github.com': [insert here token generated] 

git init projectname # or git clone url_repo
git add filename  # or "git add ." to add all modified files 
git commit -m "message or comment"
git remote set-url origin https://username:token@github.com/username/projectrepo.git
git status 
# information about branch : 'main' or 'master'. 
git push -u origin main # or master instead of main
```
[**OTHER METHOD**]

```sh
$ git config user.email "john-eod@ivorycoast.ci"
$ git config user.name "john-eod"
$ git clone https://github.com/john-eod/theproject.git
Username for 'https://github.com': john-eod
Password for 'https://john-eod@github.com': [insert here token]
$ git add .
$ git commit - m "initial commit" 
$ git status
$ git push
Username for 'https://github.com': john-eod
Password for 'https://john-eod@github.com': [insert here toke] 

```

## Add ".gitignore" file to the root of the project

```
# Adding gitignore file

```raw
touch .gitignore

## explanation of how to add content into .gitignore

*  --> is used as a wildcard match
/  --> is used to ignore pathnames relative to the ".gitignore file"
#  --> is used to add comments to a ".gitignore file"

example:
# ignore .gitignore itself
.gitignore
# ignore node_module folder and its content
node_modules
# ignore readme.txt file
readme.txt
# ignore all files with extension .docx
*.docx
# ignore files related to API keys
.env
# ignore SASS config files
.sass-cache
```
