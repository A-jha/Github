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

Using the SSH protocol, you can connect and authenticate to remote servers and services. With SSH keys, you can connect to GitHub without supplying your username and personal access token at each visit.

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

  ```
  eval "$(ssh-agent -s)"

  ```

- Step4 : Add your SSH private key to the ssh-agent
  ```
  ssh-add ~/.ssh/id_ed25519
  ```
- Step5 : Now open <br>
  home -> .ssh -> .pub
  - copy the text and paste to the github.
