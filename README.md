# git & github

## What is git?

- A free open source version control system.

## What is github?

- A website to host your repository online.

## What is version control?

- The management of changes to documnents, computer programs, large websites and other collection of information.

## Terms

- Directory - Folder
- Teminal - Interface for text command.
- CLI - Command line interface
- cd - change directory
- Code Editor - Word processor for writing code.
- Repository - Project or folder/place where your project is kept.

## GIT Commands

- clone - Bring a repository that is hosted somewhere like Github into folder on your local machine.
- add - track your file and changes in Git.
- Commit - Save your files in Git.
- push - Upload Git commits to remote repo like github.
- pull - Download changes from remote repo to your local machine, the opposite of push.

## How to Generate SSH Key ?

Using the SSH protocol, you can connect and authenticate to remote servers and services. With SSH keys, you can connect to GitHub without supplying your username and personal access token at each visit.<br>
`Basically github has a mathematical logic in your private key and based on that key it varifies your public key when you are using it.`

- Step1 :

  ```bash
  ssh-keygen -t ed25519 -C "youremail@gmail.com")
  ```

- Step2 :

  ```
  > Enter a file in which to save the key (/home/you/.ssh/id_ed25519): [Press enter]

  > Enter passphrase (empty for no passphrase): [Type a passphrase]

  > Enter same passphrase again: [Type passphrase again]
  ```

- Step3 :Start the ssh-agent in the background.

  ```bash
  eval "$(ssh-agent -s)"
  ```

- Step4 : Add your SSH private key to the ssh-agent
  ```bash
  ssh-add ~/.ssh/id_ed25519
  ```
- Step5 : Now open <br>
  home -> .ssh -> .pub
  - copy the text and paste to the github.
  - .pub stands for public

## Git Status

- it will show us the status of our repo.

```bash
git status
```

- status returned<br>

  <kbd>Example - </kbd>

  ````css
  On branch master
  Your branch is up to date with 'origin/master'.

      Changes to be committed:
      (use "git restore --staged <file>..." to unstage)
              modified:   README.md

      Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git restore <file>..." to discard changes in working directory)
              modified:   README.md
      ```
  ````

# Add repo from github to local

## Git Clone

```
    git clone ssh link of your repo
```

## Git add

- add all files and folder
  ```bash
  git add .
  ```
- add individual file
  ```bash
  git add <filename/filepath>
  ```

## git commit

- commit with message and description
  ```bash
  git commit -m "message" -m "Description"
  ```

## git push

- origin - An option set for us which basically stands for the location of our repository.

  ```bash
  git push origin master
  ```

- We can use upstream
  ```bash
  git push -u origin master
  ```
- After upstreaming we can push to master using
  ```bash
  git push
  ```

# How to Add local directory into github

- Step1 : Create a repository in your github account
- step2 :initialize git
  ```bash
  git init
  ```
- Step3 : Add you directory And files
  ```bash
  #to add all
  git add .
  # to add selected files
  git add <file_name>
  ```
- Step4 : Commit this with message and desc
  ```bash
  git commit -m "Maessage" -m "desc"
  ```

## Git Remote

- Step5 : Add the remote origin
  ```bash
  git remote add origin git@github.com:A-jha/PostgreSql.git
  ```
- Step5-1 : Check the remote repo where we connected this repo
  ```bash
  git remote -v
  ```
- Step6 : Push the repo
  ```bash
  git push origin master
  ```
