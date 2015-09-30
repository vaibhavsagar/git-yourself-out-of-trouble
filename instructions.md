# git rebase

1. `mkdir demo`
2. `cd demo` and `git init`
3. `vim a.txt` and enter 'This is file A'
4. `vim b.txt` and enter 'This is file B'
5. `git add a.txt` and `git commit -m "Initial commit."`
6. `git add b.txt` and `git commit -m "Add b.txt"`
7. Make a change to file B.
8. `git show HEAD`
10. Amend commit: `git add b.txt`, `git commit --amend`
11. `git show HEAD`
12. Make a change to file A. Add and commit.
13. `git log --oneline`
14. `git rebase -i --root`
15. Move last commit to second position and squash.
16. Edit commit message.
17. `git log --oneline` and `git show HEAD~1`
18. Try to explain what just happened (DAG rewritten)

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
