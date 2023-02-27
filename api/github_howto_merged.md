1.下载安装git


2. 连接需要远程开发的合作项目

注意使用SSH仓库地址，可以免账号密码。


 git Clone SSH 地址
 
 
 3. ssh-keygen -t rsa -C “你的邮箱”

生成 私钥和公钥
windows的位置 在管理员 目录  （直接使用Git的Bash面板，写linux命令。避免再windows的cmd里面写windows命令不一致）

提供公钥

         1、 查看本地是否存在SSH密钥
         命令：ls -al ~/.ssh

         如果在输出的文件列表中发现id_rsa和id_rsa.pub的存在，证明本地已经存在SSH密钥，请执行第3步

         2、 生成SSH密钥
         命令：ssh-keygen -t rsa -C "自己的Email地址"

         注意：执行完成后会有一些列提示输入密码的指令，直接回车即可

         3、 查看SSH公钥
         命令：cat /Users/电脑用户名/.ssh/id_rsa.pub

         复制打印出来的信息，在GitLab或者GitHub的SSH Keys中进行相应设置即可

         4. 项目里加入 自己的账号 ，自己邮箱去验证（此次为验证）


3和4需测试 是否任一一种方法都可以。

5. 生成自己的分支再merge操作

        1、使用命令查看当前所属分支

        git branch
        1


        2、拉取项目最新的代码

        git pull
        1


        3、将A分支的代码合并至B分支上

        //首先切换分支到想合并的分支上
        git checkout B

        git merge A
        1
        2
        3
        4
        4、添加至本地仓库，提交一气呵成

        git add .

        git commit -m "A分支代码合并至B分支上"

        git push
 

6. git仓库审核收到的merge申请


7.合并后，git上的项目再加到服务器，上线。 测试通过
