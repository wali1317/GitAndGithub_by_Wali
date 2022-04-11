1. Ome empty git repository "GitAndGithub_by_Wali" was created in my GitHub account and made it public.
   https://github.com/wali1317/GitAndGithub_by_Wali.git
2. This repository was cloned to the local machine following this command:
   $ git clone https://github.com/wali1317/GitAndGithub_by_Wali.git
   Cloning into 'GitAndGithub_by_Wali'...
   warning: You appear to have cloned an empty repository.
3. Branch was checked by the following command. It shows that I am in main branch.
   $ git status
   On branch main
   No commits yet
   nothing to commit (create/copy files and use "git add" to track)
4. Two files Git.text and GitHub.text was created in this main branch:
   $ touch Git.text GitHub.text
5. Then these two files are filled up by writing something about git and GitHUb. Test was added by IntelliJ IDEA.
This can be also done by nano, vi or vim test editor.
6. Then a README.md file created by following command:
   $ touch README.md
7. Then I have seen the changes by the following command:
   $ git status
   On branch main
   No commits yet
   
   Untracked files:
      (use "git add <file>..." to include in what will be committed)
         Git.text
         GitHub.text
         README.md

   nothing added to commit but untracked files present (use "git add" to track)
8. By the following way the changes were pushed to remote:
   
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
9. A folder "temp" is added in local directory and some files are added to that directory.
    $ mkdir temp
    $ cp /d/Personal/Ship* temp/
    $ cp /c/Users/My\ PC/Videos/Debut/Deb* temp/
    $ ls temp/
    'Debut 1.avi'  'Debut 2.avi'  'Debut 3.avi'   Ship1.jpg   Ship2.jpg
10. A local file .gitignore added to local.
11. In the local file, temp folder was declared so that the folder do not store in repository:
    $ echo "temp" > .gitignore
12. Local changes was observed by following command, where no changes were found in regard of temp folder:
    $ git status
    modified:   README.md
    Untracked files:
    .gitignore
13. Again pushed all changes to remote. Where temp folder were not being uploaded:
    $ git add .
    $ git commit -m "Pushed without temp folder"
    $ git push origin main
14. A feature branch "differences" is added, checked at was set to the current branch as the differences branch:
    $ git branch differences
    $ git branch
    differences
  * main
    $ git checkout differences
15. Git.text and GitHub.text files were updated writing the features of Git and GitHub.
16. Another file "difference.text" was added along with the writing of the differences between git and GitHub.
17. Then README.md file updated with git commands, usage and answers.
18. Changes were observed by the following command:
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
19. All changes pushed in differences branch:
    $ git add .
    $ git commit -m "Updated Git.text, GitHub.text, README.md; Added difference.text by difference branch"