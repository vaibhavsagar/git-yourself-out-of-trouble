# git add --patch

1. `mkdir demo`
2. `cd demo` and `git init`
3. Set up GitHub repo and configure remote.
4. Remind everyone of add, commit, push.
5. `touch a.txt`
6. `git add a.txt` and `git commit -m "Initial commit."`
7. Make another change.
8. `git add a.txt` and `git commit -m "First change."`
7. Edit file A with 'This is a change' at the very top and 'this is a conceptually different change' at the very bottom.
8. `git add --patch` and '?' for help
9. Accept the first hunk.
10. `git status`
11. `git diff` and `git diff --staged`
12. Mention other subcommands that take a '--patch' command (`checkout` and `reset`).
13. Mention Fugitive and Magit.

# git rebase

1. `mkdir demo`
2. `cd demo` and `git init`
3. Set up GitHub repo and configure remote.
4. Remind everyone of add, commit, push.
5. `touch a.txt`
6. `git add a.txt` and `git commit -m "Initial commit."`
7. `git rebase -i --root`
8. Move last commit to second position and squash.
9. Edit commit message.
10. `git log --oneline` and `git show HEAD~1`
9. Make a change to b.txt.
11. Try to explain what just happened (DAG rewritten)
12. `git checkout -b new-branch`
13. Make a change to file B. Add and commit.
14. `git log --oneline` and make a note of the commit hash.
15. `git checkout master`
16. `git cherry-pick <commit hash>`
17. Try to explain what just happened.
18. Mention issues with rewriting history.

# git reflog
1. `git reflog` shows all the commits that HEAD has pointed to in the past
2. `git reset --hard <some ref>`
3. `git log --oneline`
4. You probably don't need this, but when you do, you do.

# git bisect
1. Clone sample repo with buggy HEAD
2. Explain git bisect.
3. `git bisect start HEAD <commit-hash>`

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
