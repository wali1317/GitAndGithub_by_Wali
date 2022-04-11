#Git and GitHub Assignment

2. One empty git repository "GitAndGithub_by_Wali" was created in my GitHub account and made it public.
   https://github.com/wali1317/GitAndGithub_by_Wali.git
3. This repository was cloned to the local machine following this command:    
   $ git clone https://github.com/wali1317/GitAndGithub_by_Wali.git   
   
   Cloning into 'GitAndGithub_by_Wali'...
   
   warning: You appear to have cloned an empty repository.
4. Branch was checked by the following command. It shows that I am in main branch.
   
   $ git status
   
   On branch main
   
   No commits yet
   
   nothing to commit (create/copy files and use "git add" to track)
5. Two files Git.text and GitHub.text was created in this main branch:
   
   $ touch Git.text GitHub.text
6. Then these two files are filled up by writing something about git and GitHUb. Text was added by IntelliJ IDEA.
This can be also done by nano, vi or vim test editor.
7. Then a README.md file created by following command:
   
   $ touch README.md
8. Then I have seen the changes by the following command:
   
   $ git status
   
   On branch main
   
   No commits yet
   
   Untracked files:
      
       (use "git add <file>..." to include in what will be committed)
       Git.text
       GitHub.text
       README.md

   nothing added to commit but untracked files present (use "git add" to track)
9. By the following way the changes were pushed to remote:
   
   $ git add .
   
   $ git commit -m "Initial save"
   
   [main (root-commit) 360a9a0] Initial save
   
   3 files changed, 49 insertions(+)
   
   create mode 100644 Git.text
   
   create mode 100644 GitHub.text
   
   create mode 100644 README.md
   
   $ git status
   
   On branch main
   
   Your branch is based on 'origin/main', but the upstream is gone.
      
       (use "git branch --unset-upstream" to fixup)

   nothing to commit, working tree clean
   
   $ git push origin main
   
   Enumerating objects: 5, done.
   
   Counting objects: 100% (5/5), done.
   
   Delta compression using up to 8 threads
   
   Compressing objects: 100% (5/5), done.
   
   Writing objects: 100% (5/5), 1.72 KiB | 1.72 MiB/s, done.
   
   Total 5 (delta 0), reused 0 (delta 0), pack-reused 0
   
   To https://github.com/wali1317/GitAndGithub_by_Wali.git
   
   * [new branch]      main -> main
10. A folder "temp" is added in local directory and some files are added to that directory.

    $ mkdir temp

    $ cp /d/Personal/Ship* temp/

    $ cp /c/Users/My\ PC/Videos/Debut/Deb* temp/

    $ ls temp/

    'Debut 1.avi'  'Debut 2.avi'  'Debut 3.avi'   Ship1.jpg   Ship2.jpg
11. A local file .gitignore added to local.
12. In the local file, temp folder was declared so that the folder do not store in repository:
    
    $ echo "temp" > .gitignore
13. Local changes was observed by following command, where no changes were found in regard of temp folder:
    
    $ git status

    modified:   README.md
    
    Untracked files:
    
    .gitignore
14. Again pushed all changes to remote. Where temp folder were not being uploaded:
    
    $ git add .
    
    $ git commit -m "Pushed without temp folder"

    $ git push origin main
15. A feature branch "differences" is added, checked at was set to the current branch as the differences branch:
    
    $ git branch differences

    $ git branch

    differences

    main
    
    $ git checkout differences
16. Git.text and GitHub.text files were updated writing the features of Git and GitHub.
17. Another file "difference.text" was added along with the writing of the differences between git and GitHub.
18. Then README.md file updated with git commands, usage and answers.
19. Changes were observed by the following command:
    
    $ git status

    On branch differences

    Changes not staged for commit:

    (use "git add <file>..." to update what will be committed)
    
    (use "git restore <file>..." to discard changes in working directory)
        
        modified:   Git.text

        modified:   GitHub.text

        modified:   README.md

    Untracked files:
    
    (use "git add <file>..." to include in what will be committed)
        
        difference.text

    no changes added to commit (use "git add" and/or "git commit -a")
20. All changes pushed by differences branch :
    
    $ git add .

    $ git commit -m "Updated Git.text, GitHub.text, README.md; Added difference.text by difference branch"

    $ git push origin differences
21. New changes were not committed in main branch.
22. Then feature brunch were merged into main branch by the following command:
    
    $ git merge differences
23. Now all the changes that was made by differences branch are also committed in the main branch.
24. Then all changes were pushed to the remote:
    
    $ git push origin main
25. Then README.md file was updated
26. One contributor was invited named Rashid1501 and given the "differences" clone link
    https://github.com/wali1317/GitAndGithub_by_Wali.git.
    
    After moving into "https://github.com/wali1317/GitAndGithub_by_Wali.git" link, contributor have clicked 
    "Fork" and choose his account to be forked.
    
    Now, he could see GitAndGithub_by_wali repository in his (Rashid15011) GitHub. Then he cloned the repo for 
    "differences" branch through following command:
    
    $ git clone --single-branch --branch differences https://github.com/Rashid1501/GitAndGithub_by_Wali.git
    When he entered in the clonned directory, found himself in "differences" branch. It was also confirmed that
    no other branch is available except "differences" by the following command:
    
    $ git branch
    * differences
27. Then the contributor made changes in Git.text and GitHub.text with the follwing line
    "These lines are updated by Rashid1501".
28. Now some lines are added and removed in Git.text file in "main" branch.  
    
    $ nano Git.text
    
    $ git add .
    
    $ git commit -m "Updated Git.text for conflicting check"
   
    [main 10ca834] Updated Git.text for conflicting check
    
    1 file changed, 3 insertions(+), 2 deletions(-)
    
    $ git push origin main
29. My contributor "Rashid1501" made some changes and pulled the request to me. From that pull request I did 
    found no conflict with "differences" branch. So, I merged it.
30. In the "wali1317/GitAndGithub_by_Wali" window I created a pool request. There I declared main as basic 
    branch and compared with "differences" branch.
31. Here I found one conflict. It was telling can't automatically merge.
32. Conflict was solved in the following way:
    
    Clicked create pull request. I corrected the lines of the document and clicked Mark as resolved. And finally
    committed the merge. Now it shows everything is OK.
33. Then the README.md file was updated.
34. Pushed the changes by
    
    $ git add README.md
    
    S git commit -m "Final Update"
    
    S git push origin main
35. Change found correct in remote directory.
   