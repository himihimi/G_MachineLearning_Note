首先我要掌握怎么在git上加图片.
那么我来试试相对路径

> http://blog.csdn.net/slaughterdevil/article/details/79255933


![avatar](./img_for_md/QQ20180307-001945@2x.png)

![avatar](img_for_md/QQ20180307-002151@2x.png)
![avatar](/img_for_md/QQ20180307-002151@2x.png)
![](/img_for_md/QQ20180307-002151@2x.png)


??为什么不显示???

<img src="img_for_md/QQ20180307-001945@2x.png" alt="图片名称"/>

himiMacBookPro:G_MachineLearning_Note himi$ git branch --set-upstream-to=origin/<branch> master
-bash: branch: No such file or directory
himiMacBookPro:G_MachineLearning_Note himi$ git branch --set-upstream-to=origin/master master
Branch master set up to track remote branch master from origin.
himiMacBookPro:G_MachineLearning_Note himi$
himiMacBookPro:G_MachineLearning_Note himi$ git pull
error: Your local changes to the following files would be overwritten by merge:
	.idea/vcs.xml
Please, commit your changes or stash them before you can merge.
Aborting
himiMacBookPro:G_MachineLearning_Note himi$ git stash
Saved working directory and index state WIP on master: f9f68de first commit
HEAD is now at f9f68de first commit
himiMacBookPro:G_MachineLearning_Note himi$
himiMacBookPro:G_MachineLearning_Note himi$ git pull

太蠢受不了
明天再搞