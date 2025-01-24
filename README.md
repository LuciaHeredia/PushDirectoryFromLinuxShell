# Guide: Pushing a Directory from Linux Shell to Github 
1. Create a directory:
```
mkdir <folder-name>
```
2. Go inside the directory:
```
cd <folder-name>
```
3. You can create a README file:
```
touch README.md
```
4. Initializes that directory as a Git repository by creating a **.git** subdirectory that contains all the necessary Git metadata for the repository:
```
git init
```
5. Staging all changes in the current directory for the next commit:
```
git add .
```
6. Commit with a message:
```
git commit -m "your message"
```
7. In your Github account, create a new empty repository and copy the URL.
8. Add the Github repository URL as a remote repository to your local repository(your directory):
```
git remote add origin <URL>
```
9. Connect to Github using SSH:
- Generate SSH key:
  ```
  ssh-keygen -t ed25519 -C "<your_email@example>.com"
  ```
- Show and Copy SSH key:
  ```
  cat ~/.ssh/id_ed25519.pub
  ```
- Put SSH key in your Github account:
  - Settings -> SSH keys and GPG keys -> New SSH keys
10. Change the remote URL for your local repository, to **git@github.com**: <br/>
(Make sure you have the necessary SSH key set up on GitHub to authenticate with this new URL)
```
git remote set-url origin git@github.com:<username>/<repository>.git
```
11. Verify the change:
```
git remote -v
```
12. Push commited changes to Github: <br/>
(If **remote-branch-name** already exist, choose a different one)
```
git push -u origin <remote-branch-name>
```


*Author*: [LuciaHeredia](https://github.com/LuciaHeredia)
