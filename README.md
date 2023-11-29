![image](https://github.com/harsh123-baba/Git-Tutorial/assets/64320530/4055f0cf-359e-48a7-9318-ad53b1f4ddbe)# Git-Tutorial
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

####### In Git content is only stored once


## How Git handles directories
git has one more type of data  -> Tree
Tree -> stores information about directories & their content, tree contains pointers and other blobs trees.

-> git internally does a lot of optimization the objects are stored in compressed form.
-> It mainly stores data about the change  & algorithmically shows us the file with that change.

![image](https://github.com/harsh123-baba/Git-Tutorial/assets/64320530/fae605e4-3219-4640-a6e7-06763fbcbae0)


## let's talk about commits now.
commit is also stored as objects
every commit object pointes to a tree 
- commit object has data of 
  - Author & commiter
  - Date
  - Message
  - Parent

##### commit is stored like commit in objects and directory is stored like tree.

![x](https://github.com/harsh123-baba/Git-Tutorial/assets/64320530/c8b1b924-6b62-4c99-9d9d-f6581f024d88)


#### Approch to commit whole feature in one commit without fail.

if you forget to commit a file and after commit you realised that you forget to commit this that code then basically you will commit again that is not good practice so. 
`git commit --amend` 
command will not create other `commit` on `git log` you will find both commits binded in a single commit. 

### Working Area 
The files/chnages which are not in your staging area and may be currently not handled key git are in working area. These files/changes are also called untracked files

### Stagging area
files/changes which are surely going to be part of the next commit are in stagging area(i.e. on file/change where we do git add)
Stagging area is the place where git knows what will change between current and next commit.

### Repo area
All our commits exists



 


