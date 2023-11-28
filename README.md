# Git-Tutorial
### Begineers command
1. `git init` -> It intialize a new git repository. What is a repository ?
            It is a folder managed by git where we can track all the changes we are making in the project
2. `git status` ->  There can be a bunch of files that are not currently handled by git. 
            It means that changes done or to be done in those files are not managed by git yet. A file 
            which is in working area is considered to be not in the staging area. When we do `**git status**`
            and we see abunch if `untracked files` then these are actually called to be in the working area.
3. `git add <filename>`-> starts tracking your new changes for the next commit
4. `git commit -m <meesage>` -> this creates a new version based on your previous changes.
5. `git log` -> list downs all the commits of the repository. If you want to exit out of git log prompt
            press `q`.



### Advnaced GIT
`how git it internally working`
Internally git is `<key, value>` data store.
key is unique identifier.
`key` -> hash of data we want to store / 40 digits hexadecimal value for same data thsi hash will be same. 
`value` -> actual data / git stores compressed data in a blob and some other metadata in the header.
in git it content only stored once.
Tree structure of .git folder where actually all the data is begin stroed
![image](https://github.com/harsh123-baba/Git-Tutorial/assets/64320530/5b24738b-d32d-443b-8680-edb323a5e4a6)

in objects directory there is d3 directory so when we are hashing our key so 2 char from front wold be directory for the particular content.
![Screenshot from 2023-11-28 12-20-43](https://github.com/harsh123-baba/Git-Tutorial/assets/64320530/3095a22f-6036-47f4-b15a-2c463027abd6)


This is how value -> content is going to store in blob Data structure.





