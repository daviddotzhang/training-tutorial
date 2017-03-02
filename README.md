## This is an internal trainning for arthur ##
* [×] author: david zhang
* [×] date:   2017-3-2
* [×] version: 1

### Chapter1: Conceptions ###

* ##### What is the differences between LPS, LPE, LPP, LESA ? #####
Note: We started to use LPS (and in some cases other tickets) as the identifier for fixes so there's no 	need to create LPE tickets for DXP. The LPE tickets in the fixed   issues list are used for security (private / secure) tickets only.

* #####  What is the uses case of LPP task, L1 escalation, patch ? ######
    * [ ] Task: not sure this is a bug.
    * [ ] Patch: normally it is a bug and need a fix
    * [ ] L1 escalation:


* #####  What are the follow repositories for ? #####
-  https://github.com/liferay/liferay-portal/
-  https://github.com/liferay/liferay-plugins/
-  https://github.com/liferay/liferay-portal-ee/
-  https://github.com/liferay/liferay-plugins-ee/
-  https://github.com/liferay/com-liferay-journal/

#####  What are the follow tags for ? #####
-  fix-pack-base-6012,fix-pack-base-6110,fix-pack-base-6120
-  fix-pack-base-6130 ,fix-pack-base-6130-sp3, fix-pack-base-6130-sp4
-  fix-pack-base-6210, fix-pack-base-6210-sp7,fix-pack-base-6210-sp10, fix-pack-base-6210-sp13, fix-pack-base-6210-sp15
-  fix-pack-base-7010, fix-pack-de-1-7010, fix-pack-de-2-7010, fix-pack-de-3-7010, fix-pack-de-4-7010,  fix-pack-de-5-7010, fix-pack-de-6-7010, fix-pack-de-7-7010, fix-pack-de-8-7010, fix-pack-de-9-7010, fix-pack-de-10-7010, fix-pack-de-11-7010

#####  What can I download from the follow link ? #####
-  patches,hotfixes,fix-pack,vmware,patching-tool,softwares.
-  http://mirrors.dlc.liferay.com/files.liferay.com/
-  https://web.liferay.com/group/customer/dxp/
-  https://web.liferay.com/group/customer/products/portal/6.2/

#####  How to create a plugin fix snapshot ? #####
-  This one is a little longer, you can ask me for help if necessary.
-  https://grow.liferay.com/excellence/-/wiki/Grow/Support+Marketplace+App+Release+SOP#section-Sup port+Marketplace+App+Release+SOP-Purpose+of+this+page

#####  How to backport a fix ? #####
-  https://grow.liferay.com/documents/portlet_file_entry/20147/Backport%20guidelines%20-%20Basics.pdf/bd44fba5-437f-fde2-34e5-98e37128450e?status=0&download=true

#####  where can I get help - SME request ? #####
-  https://grow.liferay.com/people/Using+Jira+to+interact+with+the+SME+System/"

### Chapter2: What should I do if I get a new LPP ticket ? ###

##### If cse mentioned that if has been fixed in latest master. ####
- you can use keyword to search on google and jira to find the related LPS, you might be lucky to find a solution.

##### If I found LPS-ABC fixing customer’s issue, can I build a fix to the customer directly #####
- Of course no, It is a must that you need to test the fix, besides you also need to check if LPS-ABC is caused by LPS-DEF, if LPS-DEF depends on LPS-XYZ.

##### If cse mentioned that if it is not fixed yet in latest master ####
- For pull request of master, please send to Hugo.
- https://github.com/liferay/liferay-portal
- htps://github.com/hhuijser/liferay-portal

- For pull rquest of ee-7.0.x and ee-6.2.x, ee-6.1.x, please send to dusgtin.
- https://github.com/dustinryerson/liferay-portal-ee
- https://github.com/dustinryerson/liferay-portal-ee/tree/ee-7.0.x
- https://github.com/dustinryerson/liferay-portal-ee/tree/ee-6.2.x
- https://github.com/dustinryerson/liferay-portal-ee/tree/ee-6.1.x
    
####  Tips - chapter2 ####
- it is important to update the process on LPP tickets, this will help CSE to inform the latest status. Even if you justreproduced the issue, let CSE know it.
- For the pull request, it will be better to comment why you fix the issue in this way. Also pay attention to the source format.

### Chapter3: How to create a hotfix to the customer ? ###

##### First of all, you need to check with the from Patch Portal. ####
- if the customer has two versions in use, like sp10 and sp15, if yes, you need to confirm with CSE.

##### How to create a branch based on existing tags.  #####
- If customer is using DXP, for example fix-pack-de-11. 
  git checkout -b LPS-XXX fix-pack-de-11.
- If customer is using EE62, for example sp15. Now we have sp7,sp10,sp13,sp15.
  git checkout -b fix-pack-LPP-XXX-sp15 fix-pack-base-6210-sp15.

##### How to create a hotfix on Patch Portal ####
- https://patcher.liferay.com/group/guest/patching
- For DXP, the use LPS to create the hotfix, see example LPS-70751
- For EE62, the use LPS to create the hotfix, see example LPE-14727
### Chapter1: Conceptions ###

##### What is the differences between LPS, LPE, LPP, LESA ? #####
Note: We started to use LPS (and in some cases other tickets) as the identifier for fixes so there's no 	need to create LPE tickets for DXP. The LPE tickets in the fixed   issues list are used for security (private / secure) tickets only.

#####  What is the uses case of LPP task, L1 escalation, patch ? ######
* [ ] Task: not sure this is a bug.
* [ ] Patch: normally it is a bug and need a fix
* [ ] L1 escalation:


#####  What are the follow repositories for ? #####
-  https://github.com/liferay/liferay-portal/
-  https://github.com/liferay/liferay-plugins/
-  https://github.com/liferay/liferay-portal-ee/
-  https://github.com/liferay/liferay-plugins-ee/
-  https://github.com/liferay/com-liferay-journal/

#####  What are the follow tags for ? #####
-  fix-pack-base-6012,fix-pack-base-6110,fix-pack-base-6120
-  fix-pack-base-6130 ,fix-pack-base-6130-sp3, fix-pack-base-6130-sp4
-  fix-pack-base-6210, fix-pack-base-6210-sp7,fix-pack-base-6210-sp10, fix-pack-base-6210-sp13, fix-pack-base-6210-sp15
-  fix-pack-base-7010, fix-pack-de-1-7010, fix-pack-de-2-7010, fix-pack-de-3-7010, fix-pack-de-4-7010,  fix-pack-de-5-7010, fix-pack-de-6-7010, fix-pack-de-7-7010, fix-pack-de-8-7010, fix-pack-de-9-7010, fix-pack-de-10-7010, fix-pack-de-11-7010

#####  What can I download from the follow link ? #####
-  patches,hotfixes,fix-pack,vmware,patching-tool,softwares.
-  http://mirrors.dlc.liferay.com/files.liferay.com/
-  https://web.liferay.com/group/customer/dxp/
-  https://web.liferay.com/group/customer/products/portal/6.2/

#####  How to create a plugin fix snapshot ? #####
-  This one is a little longer, you can ask me for help if necessary.
-  https://grow.liferay.com/excellence/-/wiki/Grow/Support+Marketplace+App+Release+SOP#section-Sup port+Marketplace+App+Release+SOP-Purpose+of+this+page

#####  How to backport a fix ? #####
-  https://grow.liferay.com/documents/portlet_file_entry/20147/Backport%20guidelines%20-%20Basics.pdf/bd44fba5-437f-fde2-34e5-98e37128450e?status=0&download=true

#####  where can I get help - SME request ? #####
-  https://grow.liferay.com/people/Using+Jira+to+interact+with+the+SME+System/"

### Chapter2: What should I do if I get a new LPP ticket ? ###

##### If cse mentioned that if has been fixed in latest master. ####
- you can use keyword to search on google and jira to find the related LPS, you might be lucky to find a solution.

##### If I found LPS-ABC fixing customer’s issue, can I build a fix to the customer directly #####
- Of course no, It is a must that you need to test the fix, besides you also need to check if LPS-ABC is caused by LPS-DEF, if LPS-DEF depends on LPS-XYZ.

##### If cse mentioned that if it is not fixed yet in latest master ####
- For pull request of master, please send to Hugo.
- https://github.com/liferay/liferay-portal
- htps://github.com/hhuijser/liferay-portal

- For pull rquest of ee-7.0.x and ee-6.2.x, ee-6.1.x, please send to dusgtin.
- https://github.com/dustinryerson/liferay-portal-ee
- https://github.com/dustinryerson/liferay-portal-ee/tree/ee-7.0.x
- https://github.com/dustinryerson/liferay-portal-ee/tree/ee-6.2.x
- https://github.com/dustinryerson/liferay-portal-ee/tree/ee-6.1.x
    
####  Tips - chapter2 ####
- it is important to update the process on LPP tickets, this will help CSE to inform the latest status. Even if you justreproduced the issue, let CSE know it.
- For the pull request, it will be better to comment why you fix the issue in this way. Also pay attention to the source format.

### Chapter3: How to create a hotfix to the customer ? ###

##### First of all, you need to check with the from Patch Portal. ####
- if the customer has two versions in use, like sp10 and sp15, if yes, you need to confirm with CSE.

##### How to create a branch based on existing tags.  #####
- If customer is using DXP, for example fix-pack-de-11. 
  git checkout -b LPS-XXX fix-pack-de-11.
- If customer is using EE62, for example sp15. Now we have sp7,sp10,sp13,sp15.
  git checkout -b fix-pack-LPP-XXX-sp15 fix-pack-base-6210-sp15.

##### How to create a hotfix on Patch Portal ####
- https://patcher.liferay.com/group/guest/patching
- For DXP, the use LPS to create the hotfix, see example LPS-70751
- For EE62, the use LPS to create the hotfix, see example LPE-14727
