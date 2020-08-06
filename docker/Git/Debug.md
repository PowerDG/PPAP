

## 提交冲突

https://blog.csdn.net/weixin_42288182/article/details/96568718



主要原因是git仓库上已经存在readme文件，故在提交时可能会存在冲突，这时您需要选择的是保留线上的文件或者舍弃线上的文件：

#### 解决办法：

1、如果您舍弃线上的 文 件，则在推送时选择强制推送，强制推送需要执行下面的命令：
 `git push origin master -f`

2、如果您选择保留线上的readme文件,则需要先执行

```
git pull origin master
```



## Authentication failed for 解决办法



## Permission denied

https://blog.csdn.net/double_lee3/article/details/90241989

开了另外一个账户，导致在git add .的时候会出现"Permission denied"的错误，这是由于公钥失效的问题导致的，要重新添加一个公钥进去。









先进去ssh文件位置cd~/.ssh，然后重新创建公钥ssh-kengen -t rsa -C "你的邮箱"，然后一路enter下去，最好换个名字，我的是123456随意，



