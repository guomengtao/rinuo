1.下载安装git


2. 连接需要远程开发的合作项目

注意使用SSH仓库地址，可以免账号密码。


 git Clone SSH 地址
 
 
 3. ssh-keygen -t rsa -C “你的邮箱”

生成 私钥和公钥
windows的位置 在管理员 目录 

提供公钥


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
