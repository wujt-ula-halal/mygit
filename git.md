## git

### git安装

----------------------

#### 安装时:     

​	默认都是下一步   只有一条选择   Use git from git bash only..

#### 配置path环境变量

​	选择安装位置 **bin**目录

#### 配置git: 用户名 密码

```bash
git config --global user.name 'wujianting'
git config --global user.email 'wujiangting@navinfo.com'
```

#### 查看git配置

​	在C:\Users\当前用户\ .gitconfig文件下

#### 搭建git服务器(远程仓库) : 

​	统一的托管网站 (github, gitlab....)

#### 配置ssh

​	为了 在本地 和远程仓库之间进行 免秘钥登录, 可以配置 ssh

​	-在本地生成秘钥

```bash
ssh-keygen -t rsa -C wujianting@navinfo.com
```

​	该命令回车后一直回车

​	然后在github中找到settings ==> SSH and GPG keys  ==> New SSH key  title任意,在key中输入id_rsa.pub文件中的内容

​	然后可以测试ssh是否连通

```bash
ssh -T git@github.com
```

​	然后输入yes

​	如果successful了, 在.ssh中会生成一个known_hosts 文件

​	如果失败: 多尝试几次, 检查回车符等



### git应用

-------------

1. 创建一个文件夹
2. 初始化一个git项目

```bash
git init
```

3. 在github上创建一个项目,生成一个远程项目地址 ssh地址或https地址[git@github.com:wujt-ula-halal/mygit.git]()

4. 本地项目和远程项目关联

```bash
git remote add origin git@github.com:wujt-ula-halal/mygit.git
```

5. 第一次发布项目

```bash
git add .      // 文件--> 暂存区(.代表当前目录下所有文件)
git commit -m "注释内容"     // 暂存区 --> 本地分支 (默认master分支)
git push -u origin master    // 第一次提交 将本地分支 --> 远程分支
```

6. 从远程仓库复制代码

```bash
git clone git@github.com:wujt-ula-halal/mygit.git
```

7. 长期维护项目

```bach
git add .
git commit -m ""
git push origin master
```

8. 拉取最新代码

```bash
git pull
```
