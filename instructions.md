# git add --patch

# git rebase

1. `mkdir demo`
2. `cd demo` and `git init`
3. Set up GitHub repo and configure remote.
4. Remind everyone of add, commit, push.
5. `touch a.txt`
6. `git add a.txt`
7. Edit file A with 'This is a change' and 'this is a conceptually different change'.
8. `git diff --patch` and '?' for help
9. Hit 's' a few times and settle on 'e'.

# git rebase

1. `vim a.txt` and enter 'This is file A'
2. `vim b.txt` and enter 'This is file B'
3. `git add a.txt` and `git commit -m "Initial commit."`
4. `git push origin master`
5. `git add b.txt` and `git commit -m "Add b.txt"`
6. Make a change to file B.
7. `git show HEAD`
8. Amend commit: `git add b.txt`, `git commit --amend`
9. `git show HEAD`
10. Make a change to file A. Add and commit.
11. `git log --oneline`
12. `git rebase -i --root`
13. Move last commit to second position and squash.
14. Edit commit message.
15. `git log --oneline` and `git show HEAD~1`
16. Try to explain what just happened (DAG rewritten)
17. `git checkout -b new-branch`
18. Make a change to file B. Add and commit.
19. `git log --oneline` and make a note of the commit hash.
20. `git checkout master`
21. `git cherry-pick <commit hash>`
22. Try to explain what just happened.
23. Mention issues with rewriting history.

# git reflog
1. `git reflog` shows all the commits that HEAD has pointed to in the past
2. `git reset --hard <some ref>`
3. `git log --oneline`
4. You probably don't need this, but when you do, you do.

# git fsck

1. `git clone git@github.com:vaibhavsagar/reactive-coursera.git`
2. `cd reactive-coursera`
3. `rm -rf .git other`
4. `git status`
5. `git init`
6. `git add -- '*.scala'`
7. `git reset --hard`
8. NEVER DO THIS!
9. `ls -R`
10. DESPAIR!
11. Fast forward a few months, read about `git fsck`
12. `git fsck` and notice that the files exist!
13. `git fsck --lost-found`
14. Inspect the contents of `.git/lost-found/other`
15. REJOICE!

