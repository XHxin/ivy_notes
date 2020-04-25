# Git入门



## 拉取项目

1. 拿到一个项目的Git地址，例如https://github.com/XHxin/demo-spring-cloud.git

2. 确定使用的开发**分支**，例如现在master分支是开发分支。

3. 拉取代码

   1. 确定把项目放在你本地哪个文件夹下面，在该文件夹中右键打开Git 命令窗口

      ![image-20200424194558590](C:\Users\13019\AppData\Roaming\Typora\typora-user-images\image-20200424194558590.png)

   2. 使用git clone -b 命令克隆代码

      ![image-20200424194821733](C:\Users\13019\AppData\Roaming\Typora\typora-user-images\image-20200424194821733.png)

4. 使用Idea打开刚刚拉取到的项目

   1. ![image-20200424194929255](C:\Users\13019\AppData\Roaming\Typora\typora-user-images\image-20200424194929255.png)

   2. 选中刚刚拉取到的项目，打开

      ![image-20200424195101982](C:\Users\13019\AppData\Roaming\Typora\typora-user-images\image-20200424195101982.png)

   3. 



## gitignore文件

.gitignore文件的作用是把一些无用的文件过滤调，git不会再管理这些无用的文件，如下图，项目里加入gitignore文件之前会有绿色框框中的无用文件，加入gitignore文件之后这些文件就被过滤了。![image-20200424201034728](C:\Users\13019\AppData\Roaming\Typora\typora-user-images\image-20200424201034728.png)

## Git指令

- git status

  - **在项目所在的文件夹下面打开git 命令窗口**，打开窗口后第一时间就是执行git status，看看当前文件的状态。

    ![image-20200424200622893](C:\Users\13019\AppData\Roaming\Typora\typora-user-images\image-20200424200622893.png)

  - 看到有红色的，代表那些文件还没有添加到本地缓冲区，这个时候就要使用git add命令把修改的文件添加到本地缓冲区。

- git add

  - git add命令后面加上你要add的文件，可以不输入完整的文件名，因为**git会做前缀匹配**。
  - ![image-20200424201508892](C:\Users\13019\AppData\Roaming\Typora\typora-user-images\image-20200424201508892.png)
  - git add命令把修改/新增/或删除掉的文件加入本地缓冲区，加入本地缓存区之后的文件会变成绿色，绿色的文件是待commit的。

- git commit

  - git commit命令是提交本地缓冲区中的文件，但是注意，git commit的代码还没有被推算到远程仓库中。commit的时候有必要加上一些注释
  - ![image-20200424202041448](C:\Users\13019\AppData\Roaming\Typora\typora-user-images\image-20200424202041448.png)
  - git commit之后，你需要做的是先拉取（git pull）远程仓库中的代码，拉取别人的代码如果没冲突可以直接push，如果有冲突就要先**解决冲突**。

- git pull

  - 执行git pull命令如下，红框部分标识这个文件里有冲突。有可能是一个文件中有多个冲突，也有可能是多个文件有冲突。

    ![image-20200424220528919](C:\Users\13019\AppData\Roaming\Typora\typora-user-images\image-20200424220528919.png)

  - 冲突如下，这样代表一个冲突，中间用“============”分隔，上面部分是你自己的代码，下面部分是别人的代码。这可能需要双方确认保留谁的。

    ![image-20200424220254755](C:\Users\13019\AppData\Roaming\Typora\typora-user-images\image-20200424220254755.png)

  - 在代码中解决冲突

    ![image-20200424220913976](C:\Users\13019\AppData\Roaming\Typora\typora-user-images\image-20200424220913976.png)

  - 解决完冲突之后要把冲突的文件重新add、commit，这个时候再pull，然后再push上去（**Push之前一定要先pull**）。

    ![image-20200424221217526](C:\Users\13019\AppData\Roaming\Typora\typora-user-images\image-20200424221217526.png)

  - git pull命令执行之后可能会出现如下界面，这个时候输入冒号+q+!，然后点击确认就可以了

    ![image-20200424222324222](C:\Users\13019\AppData\Roaming\Typora\typora-user-images\image-20200424222324222.png)

    如果显示“--插入--”，就先按一下“Esc”建，再输入“:q!”

    ![image-20200424222433547](C:\Users\13019\AppData\Roaming\Typora\typora-user-images\image-20200424222433547.png)

- git push

  - ![image-20200424221503255](C:\Users\13019\AppData\Roaming\Typora\typora-user-images\image-20200424221503255.png)



