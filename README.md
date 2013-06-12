# This is an exercise.

rsp_exercise の リポジトリコピーテスト用


# 以下コマンドログ
```
    git clone git@github.com:yuu-ito/rsp_exercise.git
Cloning into 'rsp_exercise'...
Enter passphrase for key '/root/.ssh/id_rsa':
...
    cd rsp_exercise/
    git st
# On branch master
nothing to commit, working directory clean
    git remote -v
origin  git@github.com:yuu-ito/rsp_exercise.git (fetch)
origin  git@github.com:yuu-ito/rsp_exercise.git (push)
    git remote rm origin
    git remote -v
    cd ..
    mv rsp_exercise/ rsp_exercise_copy
    cd rsp_exercise_copy/
    git remote add origin git@github.com:yuu-ito/rsp_copy.git
    git remote -v
origin  git@github.com:yuu-ito/rsp_copy.git (fetch)
origin  git@github.com:yuu-ito/rsp_copy.git (push)
    git push origin master
Enter passphrase for key '/root/.ssh/id_rsa':
To git@github.com:yuu-ito/rsp_copy.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'git@github.com:yuu-ito/rsp_copy.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first merge the remote changes (e.g.,
hint: 'git pull') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
    git pull origin master
Enter passphrase for key '/root/.ssh/id_rsa':
From github.com:yuu-ito/rsp_copy
 * branch            master     -> FETCH_HEAD
Auto-merging README.md
CONFLICT (add/add): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.
    git st
# On branch master
# You have unmerged paths.
#   (fix conflicts and run "git commit")
#
# Unmerged paths:
#   (use "git add <file>..." to mark resolution)
#
#       both added:         README.md
#
no changes added to commit (use "git add" and/or "git commit -a")
    more README.md
<<<<<<< HEAD
# This is an exercise.

=======
rsp_copy
========

rsp_exercise の リポジトリコピーテスト用
>>>>>>> 2ba2d7f70e1d5b1b91886d854804bf3450caed80
v README.md
    git st
# On branch master
# You have unmerged paths.
#   (fix conflicts and run "git commit")
#
# Unmerged paths:
#   (use "git add <file>..." to mark resolution)
#
#       both added:         README.md
#
no changes added to commit (use "git add" and/or "git commit -a")
    git add .
    git st
# On branch master
# All conflicts fixed but you are still merging.
#   (use "git commit" to conclude merge)
#
# Changes to be committed:
#
#       modified:   README.md
#
    git ci -m "merge README.md"
[master ae4857f] merge README.md
 Committer: yit <root@localhost.localdomain>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly:

    git config --global user.name "Your Name"
    git config --global user.email you@example.com

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

    git st
# On branch master
nothing to commit, working directory clean
    git push
warning: push.default is unset; its implicit value is changing in
Git 2.0 from 'matching' to 'simple'. To squelch this message
and maintain the current behavior after the default changes, use:

  git config --global push.default matching

To squelch this message and adopt the new behavior now, use:

  git config --global push.default simple

See 'git help config' and search for 'push.default' for further information.
(the 'simple' mode was introduced in Git 1.7.11. Use the similar mode
'current' instead of 'simple' if you sometimes use older versions of Git)

Enter passphrase for key '/root/.ssh/id_rsa':
Counting objects: 73, done.
Compressing objects: 100% (38/38), done.
Writing objects: 100% (71/71), 141.74 KiB, done.
Total 71 (delta 33), reused 67 (delta 32)
To git@github.com:yuu-ito/rsp_copy.git
   2ba2d7f..ae4857f  master -> master
    git st
# On branch master
nothing to commit, working directory clean
```

