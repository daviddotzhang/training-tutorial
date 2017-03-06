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

1: 如何推送到USER远端
  * git push -f orgin LPS-XZY.

2: 如何提交到Liferay远端.
  * a:提交给工程师1 -> review -> 提交给工程师2 review
  * b:BC merge into liferay-portal.
	
3: 如何使用工具，直接提交
  * git-pull-request

######  Part3：
1: 如何拽取别人的提交信息
  * git fetch upstream LPS-ABC.

2: 如何把别人的信息获取到自己的branch
  * git cherry-pick and git merge.

3: git cherry-pick and git merge区别

######  Part4：
1: 如何美化 git log 提交信息

2: 如何查询提交信息中含有 "hello" 的 commit

3: 如何查询一段代码的提交信息

4: 如何查询一个关键字的提交信息
