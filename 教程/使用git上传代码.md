# 使用git上传代码

1. 选择Git Bash

2. 初始化本地仓库

```git
git init
```

3. 将项目文件添加到缓存中

```git
git add .
```

**表示添加目录下的所以文件到缓存库，如果只添加某个文件，只需把 . 换成你要添加的文件名 **

4. 将缓存中的文件commit到git库

```git
git commit -m "添加你的注释，一般是更改的信息"
```

5. 关联远程库(首次)

``` git
git remote add origin + 服务器地址(如https://)
```

6. 将最新的修改推送到远程库

```git
git push -u origin master
```

