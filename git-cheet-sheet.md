[Individual Developer (Standalone)] commands are essential for anybody who makes a commit, even for somebody who works alone.

If you work with other people, you will need commands listed in the [Individual Developer (Participant)] section as well.

People who play the [Integrator] role need to learn some more commands in addition to the above.

[Repository Administration] commands are for system administrators who are responsible for the care and feeding of Git repositories.

Individual Developer (Standalone)[[Individual Developer (Standalone)]]
A standalone individual developer does not exchange patches with other people, and works alone in a single repository, using the following commands.

git-init[1] to create a new repository.

git-show-branch[1] to see where you are.

git-log[1] to see what happened.

git-checkout[1] and git-branch[1] to switch branches.

git-add[1] to manage the index file.

git-diff[1] and git-status[1] to see what you are in the middle of doing.

git-commit[1] to advance the current branch.

git-reset[1] and git-checkout[1] (with pathname parameters) to undo changes.

git-merge[1] to merge between local branches.

git-rebase[1] to maintain topic branches.

git-tag[1] to mark known point.

Examples
Use a tarball as a starting point for a new repository.
$ tar zxf frotz.tar.gz
$ cd frotz
$ git init
$ git add . (1)
$ git commit -m "import of frotz source tree."
$ git tag v2.43 (2)
add everything under the current directory.

make a lightweight, unannotated tag.

Create a topic branch and develop.
$ git checkout -b alsa-audio (1)
$ edit/compile/test
$ git checkout -- curses/ux_audio_oss.c (2)
$ git add curses/ux_audio_alsa.c (3)
$ edit/compile/test
$ git diff HEAD (4)
$ git commit -a -s (5)
$ edit/compile/test
$ git reset --soft HEAD^ (6)
$ edit/compile/test
$ git diff ORIG_HEAD (7)
$ git commit -a -c ORIG_HEAD (8)
$ git checkout master (9)
$ git merge alsa-audio (10)
$ git log --since='3 days ago' (11)
$ git log v2.43.. curses/ (12)
create a new topic branch.

revert your botched changes in curses/ux_audio_oss.c.

you need to tell Git if you added a new file; removal and modification will be caught if you do git commit -a later.

to see what changes you are committing.

commit everything as you have tested, with your sign-off.

take the last commit back, keeping what is in the working tree.

look at the changes since the premature commit we took back.

redo the commit undone in the previous step, using the message you originally wrote.

switch to the master branch.

merge a topic branch into your master branch.

review commit logs; other forms to limit output can be combined and include --max-count=10 (show 10 commits), --until=2005-12-10, etc.

view only the changes that touch what’s in curses/ directory, since v2.43 tag.[Individual Developer (Standalone)] commands are essential for anybody who makes a commit, even for somebody who works alone.

If you work with other people, you will need commands listed in the [Individual Developer (Participant)] section as well.

People who play the [Integrator] role need to learn some more commands in addition to the above.

[Repository Administration] commands are for system administrators who are responsible for the care and feeding of Git repositories.

Individual Developer (Standalone)[[Individual Developer (Standalone)]]
A standalone individual developer does not exchange patches with other people, and works alone in a single repository, using the following commands.

git-init[1] to create a new repository.

git-show-branch[1] to see where you are.

git-log[1] to see what happened.

git-checkout[1] and git-branch[1] to switch branches.

git-add[1] to manage the index file.

git-diff[1] and git-status[1] to see what you are in the middle of doing.

git-commit[1] to advance the current branch.

git-reset[1] and git-checkout[1] (with pathname parameters) to undo changes.

git-merge[1] to merge between local branches.

git-rebase[1] to maintain topic branches.

git-tag[1] to mark known point.

Examples
Use a tarball as a starting point for a new repository.
$ tar zxf frotz.tar.gz
$ cd frotz
$ git init
$ git add . (1)
$ git commit -m "import of frotz source tree."
$ git tag v2.43 (2)
add everything under the current directory.

make a lightweight, unannotated tag.

Create a topic branch and develop.
$ git checkout -b alsa-audio (1)
$ edit/compile/test
$ git checkout -- curses/ux_audio_oss.c (2)
$ git add curses/ux_audio_alsa.c (3)
$ edit/compile/test
$ git diff HEAD (4)
$ git commit -a -s (5)
$ edit/compile/test
$ git reset --soft HEAD^ (6)
$ edit/compile/test
$ git diff ORIG_HEAD (7)
$ git commit -a -c ORIG_HEAD (8)
$ git checkout master (9)
$ git merge alsa-audio (10)
$ git log --since='3 days ago' (11)
$ git log v2.43.. curses/ (12)
create a new topic branch.

revert your botched changes in curses/ux_audio_oss.c.

you need to tell Git if you added a new file; removal and modification will be caught if you do git commit -a later.

to see what changes you are committing.

commit everything as you have tested, with your sign-off.

take the last commit back, keeping what is in the working tree.

look at the changes since the premature commit we took back.

redo the commit undone in the previous step, using the message you originally wrote.

switch to the master branch.

merge a topic branch into your master branch.

review commit logs; other forms to limit output can be combined and include --max-count=10 (show 10 commits), --until=2005-12-10, etc.

view only the changes that touch what’s in curses/ directory, since v2.43 tag.[Individual Developer (Standalone)] commands are essential for anybody who makes a commit, even for somebody who works alone.

If you work with other people, you will need commands listed in the [Individual Developer (Participant)] section as well.

People who play the [Integrator] role need to learn some more commands in addition to the above.

[Repository Administration] commands are for system administrators who are responsible for the care and feeding of Git repositories.

Individual Developer (Standalone)[[Individual Developer (Standalone)]]
A standalone individual developer does not exchange patches with other people, and works alone in a single repository, using the following commands.

git-init[1] to create a new repository.

git-show-branch[1] to see where you are.

git-log[1] to see what happened.

git-checkout[1] and git-branch[1] to switch branches.

git-add[1] to manage the index file.

git-diff[1] and git-status[1] to see what you are in the middle of doing.

git-commit[1] to advance the current branch.

git-reset[1] and git-checkout[1] (with pathname parameters) to undo changes.

git-merge[1] to merge between local branches.

git-rebase[1] to maintain topic branches.

git-tag[1] to mark known point.

Examples
Use a tarball as a starting point for a new repository.
$ tar zxf frotz.tar.gz
$ cd frotz
$ git init
$ git add . (1)
$ git commit -m "import of frotz source tree."
$ git tag v2.43 (2)
add everything under the current directory.

make a lightweight, unannotated tag.

Create a topic branch and develop.
$ git checkout -b alsa-audio (1)
$ edit/compile/test
$ git checkout -- curses/ux_audio_oss.c (2)
$ git add curses/ux_audio_alsa.c (3)
$ edit/compile/test
$ git diff HEAD (4)
$ git commit -a -s (5)
$ edit/compile/test
$ git reset --soft HEAD^ (6)
$ edit/compile/test
$ git diff ORIG_HEAD (7)
$ git commit -a -c ORIG_HEAD (8)
$ git checkout master (9)
$ git merge alsa-audio (10)
$ git log --since='3 days ago' (11)
$ git log v2.43.. curses/ (12)
create a new topic branch.

revert your botched changes in curses/ux_audio_oss.c.

you need to tell Git if you added a new file; removal and modification will be caught if you do git commit -a later.

to see what changes you are committing.

commit everything as you have tested, with your sign-off.

take the last commit back, keeping what is in the working tree.

look at the changes since the premature commit we took back.

redo the commit undone in the previous step, using the message you originally wrote.

switch to the master branch.

merge a topic branch into your master branch.

review commit logs; other forms to limit output can be combined and include --max-count=10 (show 10 commits), --until=2005-12-10, etc.

view only the changes that touch what’s in curses/ directory, since v2.43 tag.
