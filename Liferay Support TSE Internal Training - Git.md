## Liferay Support TSE Internal Training - Git ##
* author: david zhang
* date:   2017-3-5
* version: 1.0

### Purpose ###
this artcile is to help our new TSE to have a whole idea how liferay uses git to manage the code. it will start from git basis to advance.




######Prepration
* How To Install Git
  https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

* How to fork and clone Liferay-Portal resource.
  https://github.com/liferay/liferay-portal

######  Part1：

1: how to fork and clone a remote repository ?
  * git clone https://github.com/daviddotzhang/liferay-docs.git

2: how to check which branch is in ?
  * git branch

3: how to check the code is latest ? as it is user remote, it might behind liferay remote.
  * git status

4: how to update the latest ?
  * git pull --rebase upstream master

5: how to create a new branch ?
  * git checkout -b LPS-XZY master

6: how to add a file <-> how to cancel it ?
  * touch a.txt touch b.txt.
  * git add a.txt b.txt
  * git reset a.txt b.txt

7: how to stash the files ?
  * git stash

8: how to commit a file <-> how to cancel it?
  * git commit -m "a b txt".

9: how to check the commit messages?
  *  a:using tool: gitk
  *  b:using tool: tig
  *  c:using command: log

10: how to cancel commits ?
  *  a:git reset HEAD^1
 
11: how to rebase commits ?
  *  b:git rebase -i

######  Part2

1: how to push user commits to user remote ?
  * git push -f orgin LPS-XZY.

2: how commits are merged into liferay portal ?
  * a: engineer 1 -> engineer 2 -> engineer 3 review
  * b: BC merge into liferay-portal.
	
3: how to use tool to send pull request?
  * git-pull-request

######  Part3：
1:  how to cherry fetch others' branch ?
  * git fetch upstream LPS-ABC.

2: how to cherry pick others commits ?
  * git cherry-pick and git merge.

3:  what are the differences between git cherry-pick and merge ?

######  Part4：
1:  how to beaufity git log messages ?

2: how to query commits containing word "hello" ?

3: how to check the commit messages of a special line ?

4: how to check the commit messages of a special code ?
