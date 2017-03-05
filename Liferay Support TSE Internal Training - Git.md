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

4: 如何获取最新
  * git pull --rebase upstream master

5: 如何创建一个新的分支3
  * git checkout -b LPS-XZY master

6: 如何添加一个文件.
  * touch a.txt touch b.txt.

7: 如何加入文件 <-> 如何取消文件
  * git add a.txt b.txt
  * git reset a.txt b.txt

8: 如何放弃添加的文件
  * git stash

9: 如何提交文件 <-> 如何取消提交的commit.
  * git commit -m "a b txt".

10: 如何查看提交信息.
  *  a:引入工具 gitk
  *  b:引入工具 tig
  *  c:使用git log

11: 如何修改提交信息
  *  a:git reset HEAD^1
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
