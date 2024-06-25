# Git vs Git Hub
Git | Git Hub |
---| ----|
Its an actual s/w | Its a place to store files
Its the VCS | bitbucket, gitlab are similar to github
Its an offline s/w | It cannot work without internet


## Git Fundamentals
Pushing the code through command line
1. git init -> To initialize a repository  
2. git add path/files -> To stage the changes  
3. git status -> To check the file's current state  
4. git commit -m "message" -> savepoint with a message  
5. git log -> To Track the commits
To exit from git log press 'q'
6. git checkout hashvalue - to jump to particular commit
7. git checkout - --> it brings back to the previous head pointing commit
8. git switch - -> Switch to the previous checked out branch
9. git checkout master -> To bring back to master branch
10. git reset HEAD~ -> deletes last command
    - git reset --soft HEAD~n -> n is the number of top n commits should be deleted. Soft can leave the changes made and clears the log. Files are back to staged changes to edit the commit.
    - git reset --hard HEAD~n -> Clears the log too
11. git rebase -i HEAD~n -> Last n commits are rebased // It gives oldest to latest, i means interactive console 
    - pick
    - drop
    - squash  
- Don't touch the main branches like main, dev, stage so that there won't be any mess.
12. git rebase `<HEAD>` -> When the main/master is behind we will rebase so that history should be in straight line
- Why to keep it in straight line?  
It is advised to keep it in straight line so that searching the history where the bug got introduced is very easy compared to tree like structure.
13. git pull --rebase origin `<dev>` -> Checkout feature then do this to pull all the code in the dev branch
14. git branch -D branch_name -> Deletes a branch locally
15. git blame filename.ext
16. git push -> to branch which head points to
17. git pull -> pull from which branchname you give
18. git bisect -> to search in between the commits
19. Git revert commitid -> Can change the commit by creating new commit.

### Git Log
1. git log -> to see commits
2. git log -n -> n number of recent commits will be shown  
Filters
- --author==`<pattern>`
- -n `<n is number>`
3. git log -p -> patch (What code added or deleted), which lines modified in the files
4. git log -S -> pick-axe command
5. git log -S -p -> to track through the specific functions 
    - `/<word>` - Highlight search
    - `<space>` - Page down
    - `n` - Next match
    - `N` - Prev match
6. git log --graph -> To visualise 
### COMMIT
1. Why Commit is needed?
    - When there is logical change
2. Small Commits should made
3. Message should be proper

### Git Merge Flow
![git merge flow](image-2.png)

## Merging branches online
1. Clone the project from git 
2. Cut a feat branch from dev and then do the changes
3. Commit the changes and then push it to the online
4. After pushing, raise a PR by adding a reviewer
5. After review address the comments
6. After all the comments are addressed again push it to online
7. Mark PR as Resolve and then merge will be happend after approval

DevOps merge all the changes to the master
Tester merge to staging
Developers merge to dev

## Git Stashing 
1. git stash "name"- to store it temporarily
2. git stash apply "name"- to bring the stored content

## VIM
Vim is an editor which will only open in git bash command line
- How to open vim?
> vim filename
- Shortcut in vim
> verb + number + movement
// VIM tutor & Vim games
### Different verbs in VIM
1. Move up - k
2. MOve down - j
3. Move left - h
4. Move right - l
5. Delete - d
    - Delete one word - d + 1 (Where you want to delete a word)
    - Delete multiple words - d + n (n words are deleted)
    - Delete a line - d + d
    - Delete a para - d + ip (inside para)
    - Delete a selected word - d + iw (inside word)
    - Delete characters till a particular char - d + char(ex:a,b,c)
6. Save - w
7. Exit - q
    - Force quit - q!
8. To repeat recent command - .
9. Select - v (Visual Select)
10. Inside - i
11. Around - a
12. Cut - x
13. Copy - y (Yank)
    - Copy entire line - yy

![More vim commands](image.png)



## Key Terms 
- Configuration Management
- System code 
- Configure master branch to netlify for CI
    ### Audit
    - Commits - Digital sign
    - Blame - To track the files saved by whom.